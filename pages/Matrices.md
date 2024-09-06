# Matrix
A 2D array of values with a defined number of rows and values

**Rust Implementation:**
```rust
struct Matrice {
    value: Vec<Vec<ComplexNumber>>,
    rows: usize,
    cols: usize
}
impl Matrice {
    fn new(value: Vec<Vec<ComplexNumber>>) -> Self {
        if !value.iter().all(|i| i.len() == value[0].len()) {
            panic!("Matrix is not two-dimensional! Ensure all rows are equal in length.");
        }
        let rows = value.len();
        let cols = value[0].len();
        Self {
            value,
            rows,
            cols
        }
    }
}
impl std::fmt::Debug for Matrice {
    fn fmt ( &self, f: &mut std::fmt::Formatter<'_> ) -> std::fmt::Result {
        write!(f, "{}x{}\n", self.rows, self.cols );
        for row in &self.value {
            write!(f, "{}\n", row.into_iter().map(|i| format!("{} +{}i", i.a, i.b)).collect::<Vec<String>>().join(", ") );
        }
        Ok(())
    }
}
```
- ## Operations
	- ### Matrix Addition
	  ```rust
	  pub fn add ( &mut self, to_add: Matrice ) -> &Self {
	      if self.rows != to_add.rows || self.cols != to_add.cols {
	          panic!("Matrix size {}x{} doesn't match the base size {}x{}", to_add.rows, to_add.cols, self.rows, self.cols);
	      }
	      for row in 0..self.value.len() {
	          for col in 0..self.value[row].len() {
	              self.value[row][col].add(to_add.value[row][col].clone());
	          }
	      }
	  
	      self
	  }
	  ```
	- ### Scalar Multiplication
	  ```rust
	  pub fn scalar_mult ( &mut self, to_mult: f32 ) -> &Self {
	      for row in 0..self.value.len() {
	          for col in 0..self.value[row].len() {
	              self.value[row][col].scalar_mult(to_mult);
	          }
	      }
	  
	      self
	  }
	  ```
	- ### Matrix Multiplication
	  $$M_{m\cdot n}\times N_{n\cdot r}$$
	  
	  Remember:
	  \begin{equation}
	  \begin{bmatrix}
	  a & b
	  \end{bmatrix} \text{ is represented by } M_{1\times 2\}end{equation}
	  $$\text{and}$$
	  \begin{equation}\begin{bmatrix}
	  c \\
	  d
	  \end{bmatrix} \text{ is represented by } N_{2\times 1}\end{equation}.
	  
	  To multiply the two, you would recieve:
	  \begin{equation}
	  M \times N = 
	  \begin{bmatrix}
	  ac+bd
	  \end{bmatrix}
	  \end{equation}
		- #### Rust Matrix Multiplication Implementation
		  ```rust
		  pub fn matrix_mult ( self, to_mult: Matrice ) -> Self {
		      if self.cols != to_mult.rows {
		          panic!("Number of columns in the base matrix must match the number of columns in the second row!");
		      }
		  
		      let mut end_result = Matrice::from_dimensions( self.rows, to_mult.cols );
		  
		      for r in 0..end_result.value.len() {
		          for c in 0..(end_result.value[r].len()) {
		              let row: Vec<ComplexNumber> = end_result.value[r].clone();
		              let col: Vec<ComplexNumber> = end_result
		                  .value
		                  .clone()
		                  .into_iter()
		                  .map(|i| i[c].clone())
		                  .collect();
		  
		              let dot_product: ComplexNumber = row
		                  .clone()
		                  .into_iter()
		                  .enumerate()
		                  .map(|(ind, mut i)| { // Multiply each row by element of equivalent index in each intersecting column
		                      i.mult(col[ind].clone());
		                      i
		                  })
		                  .reduce(|total: ComplexNumber, i: ComplexNumber| { // Add each element of the now row to create the final dot product
		                      total.clone().add(i.clone()).clone()
		                  })
		                  .expect("Should never happen given the matrices make it past first check")
		                  .clone();
		  
		  
		              end_result.value[r][c] = dot_product;
		          }
		      }
		  
		      end_result
		  }
		  ```
	- ### Determinant
	  ```rust
	  pub fn determinant ( &self ) -> f32 {
	      if self.cols != 2 || self.rows != 2 {
	          todo!();
	      }
	      let a = self.value[0][0];
	      let b = self.value[0][1];
	      let c = self.value[1][0];
	  
	      (a * d) - (b * c)
	  }
	  ```
	- ### Transpose
	  ```rust
	  pub fn transpose ( &mut self ) -> &Self {
	      let mut ret = Matrix::from_dimensions( self.cols, self.rows );
	  
	      for r in 0..self.rows {
	          for c in 0..self.cols {
	              ret.value[c][r] = self.value[r][c].clone();
	          }
	      }
	  
	      *self = ret;
	      self
	  }
	  ```
	- ### Conjugate
	  ```rust
	  pub fn conjugate ( &mut self ) -> &Self {
	      for r in 0..self.rows {
	          for c in 0..self.cols {
	              self.value[r][c].conjugate();
	          }
	      }
	      self
	  }
	  ```
	- ### Adjunct
	  ```rust
	  pub fn adjunct ( &mut self ) -> &Self {
	      self.transpose();
	      self.conjugate()
	  }
	  ```
	  **Note:** `self.transpose()` and `self.conjugate()` are valid code despite both being pointers because of ((64bae2cf-9355-4d13-b07e-b8395181c451))
	- ### Dot Products
	  **Note:** Both don't necessarily have to use references, but I see edge cases where it'd be helpful to do without consuming the base and argument.
		- #### Inner Product
		  ```rust
		  pub fn inner_product ( &self, to_mul: &Self ) -> ComplexNumber {
		      if self.cols != 1 || to_mul.cols != 1 {
		          panic!("Both matrices must have only one column!");
		      }
		  
		      (self.clone().adjunct().clone() * to_mul.clone()).value[0][0].clone()
		  }
		  ```
			-
		- #### Outer Product
		  ```rust
		  pub fn outer_product ( &self, to_mul: &Self ) -> Self {
		      if self.cols != 1 || to_mul.cols != 1 {
		          panic!("Both matrices must have only one column!");
		      }
		  
		      (self.clone() * to_mul.clone().adjunct().clone())
		  }
		  ```
	- ### Normalize
	  ```rust
	  pub fn normalize ( &mut self ) -> &Self {
	      if self.cols != 1 {
	          todo!(); // impl according to https://mathforums.com/t/how-do-i-normalize-a-matrix.18218/
	      }
	      let norm = self.inner_product( &self ).a.sqrt();
	  
	      for r in 0..self.value.len() {
	          self.value[r][0] /= norm;
	      }
	  
	      self
	  }
	  ```
	  **Note:** Could probably implement for $$n * m$$ size matrices according to [this](https://mathforums.com/t/how-do-i-normalize-a-matrix.18218/)