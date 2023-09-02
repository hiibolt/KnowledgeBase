- ## i
  | $i^1 = \sqrt{-1}$ | $i^2 = -1$ | $i^3 = -\sqrt{-1}$ | $i^4 = 1$ |
  Accordingly, this applies to any sqrt, given you take modulo 4 of said power
- # Representations
	- ## Cartesian
	  $$x = a + bi$$
	  
	  *a* and *b* are real numbers.
	  
	  **Rust Implementation:**
	  ```rust
	  #[derive(Clone)]
	  pub struct ComplexNumber {
	  	pub a: f32,
	      pub b: f32
	  }
	  impl std::fmt::Debug for ComplexNumber {
	      fn fmt ( &self, f: &mut std::fmt::Formatter<'_> ) -> std::fmt::Result {
	          let operator: &str = if self.b.signum() == 1.0 { "+" } else { "-" };
	  
	          write!(f, "({} {} {}i)", self.a, operator, self.b )?;
	  
	          Ok(())
	      }
	  }
	  ```
	- ## Polar
	  $$x = re^{i\theta}$$
	  $$or$$ $$x = r (\cos{\theta}+i\sin{\theta})$$
	  Guaranteed by [Euler's Formula](https://en.wikipedia.org/wiki/Euler%27s_formula#Proofs). 
	  
	  *r* and $\theta$ are real numbers, with $\theta$ being measured in radians.
	  
	  **Rust Implementation:**
	  ```rust
	  #[derive(Clone)]
	  pub struct ComplexPolarNumber {
	      r: f32,
	      theta: f32
	  }
	  impl std::fmt::Debug for ComplexNumber {
	      fn fmt ( &self, f: &mut std::fmt::Formatter<'_> ) -> std::fmt::Result {
	          let operator: &str = if self.b.signum() == 1.0 { "+" } else { "-" };
	  
	          write!(f, "({} units, {} rads)", self.r, self.theta )?;
	  
	          Ok(())
	      }
	  }
	  ```
- ## Common Operations Implemented in Rust
	- ### Addition
	  ```rust
	  impl Add for ComplexNumber {
	      type Output = Self;
	  
	      fn add ( self, to_add: Self ) -> Self {
	          Self { a: self.a + to_add.a, b: self.b + to_add.b }
	      }
	  }
	  impl AddAssign for ComplexNumber {
	      fn add_assign ( &mut self, to_add: Self ) {
	          self.a += to_add.a;
	          self.b += to_add.b;
	      }
	  }
	  ```
	- ### Subtraction
	  ```rust
	  impl Sub for ComplexNumber {
	      type Output = Self;
	  
	      fn sub ( self, to_sub: Self ) -> Self {
	          Self { a: self.a - to_sub.a, b: self.b - to_sub.b }
	      }
	  }
	  impl SubAssign for ComplexNumber {
	      fn sub_assign ( &mut self, to_sub: Self ) {
	          self.a -= to_sub.a;
	          self.b -= to_sub.b;
	      }
	  }
	  ```
	- ### Multiplication
		- #### Scalar
		  ```rust
		  impl Mul<f32> for ComplexNumber {
		      type Output = Self;
		  
		      fn mul ( self, to_mul: f32 ) -> Self {
		          Self { a: self.a * to_mul, b: self.b * to_mul }
		      }
		  }
		  impl MulAssign<f32> for ComplexNumber {
		      fn mul_assign ( &mut self, to_mul: f32 ) {
		          self.a *= to_mul;
		          self.b *= to_mul;
		      }
		  }
		  ```
		- #### Complex
		  $$(a + bi)(c + di)$$
		  $$ac + (bc)i + (ad)i - bd$$
		  $$(ac - bd) + (bc + ad)i$$
		  ```rust
		  impl Mul<ComplexNumber> for ComplexNumber{
		      type Output = Self;
		  
		      fn mul ( self, to_mul: Self ) -> Self {
		          let a = self.a;
		          let b = self.b;
		          let c = to_mul.a;
		          let d = to_mul.b;
		  
		          Self {
		              a: a * c - b * d,
		              b: b * c + a * d
		          }
		      }
		  }
		  impl MulAssign<ComplexNumber> for ComplexNumber {
		      fn mul_assign ( &mut self, to_mul: ComplexNumber ) {
		          let a = self.a;
		          let b = self.b;
		          let c = to_mul.a;
		          let d = to_mul.b;
		  
		          self.a = a * c - b * d;
		          self.b = b * c + a * d;
		      }
		  }
		  ```
	- ### Division
		- #### Scalar
		  ```rust
		  impl Div<f32> for ComplexNumber {
		      type Output = Self;
		  
		      fn div ( self, to_div: f32 ) -> Self {
		          Self { a: self.a / to_div, b: self.b / to_div }
		      }
		  }
		  impl DivAssign<f32> for ComplexNumber {
		      fn div_assign ( &mut self, to_div: f32 ) {
		          self.a /= to_div;
		          self.b /= to_div;
		      }
		  }
		  ```
		- #### Complex
		  ```rust
		  impl Div<ComplexNumber> for ComplexNumber {
		      type Output = Self;
		  
		      fn div ( self, to_div: ComplexNumber ) -> Self {
		          if self.a == 0f32 && to_div.b == 0f32 {
		              panic!("Denominator cannot be zero!");
		          }
		  
		          let a = self.a;
		          let b = self.b;
		          let c = to_div.a;
		          let d = to_div.b;
		      
		          Self {
		              a: ( a * c + b * d ) / ( c.powi(2) + d.powi(2) ),
		              b: ( b * c - a * d) / ( c.powi(2) + d.powi(2) )
		          }
		      }
		  }
		  impl DivAssign<ComplexNumber> for ComplexNumber {
		      fn div_assign ( &mut self, to_div: ComplexNumber ) {
		          if self.a == 0f32 && to_div.b == 0f32 {
		              panic!("Denominator cannot be zero!");
		          }
		  
		          let a = self.a;
		          let b = self.b;
		          let c = to_div.a;
		          let d = to_div.b;
		      
		          self.a = ( a * c + b * d ) / ( c.powi(2) + d.powi(2) );
		          self.b = ( b * c - a * d) / ( c.powi(2) + d.powi(2) );
		      }
		  }
		  ```
	- ### Complex Modulus
	  ```rust
	  pub fn modulus ( &self ) -> f32 {
	      ( self.a.powi(2) + self.b.powi(2) ).sqrt()
	  }
	  ```
	- ### Complex Exponents (E)
	  Reasoning:
	  $$e^{a+bi}$$
	  $$e^a*e^{bi}$$
	  $$e^a*(\cos{b}+i\sin{b})$$
	  $$e^a\cos{b}+e^a*i\sin{b}$$
	  ```rust
	  pub fn exp ( &mut self ) -> &Self {
	      self.a = self.a.exp() * self.b.cos();
	      self.b = self.a.exp() * self.b.sin();
	  
	      self
	  }
	  ```
	- ### Complex Conjugation
	  ```rust
	  pub fn conjugate ( &mut self ) -> &Self {
	      self.b *= -1f32;
	      self
	  }
	  ```
	  **Note:** `c1.b *= -1` is valid code despite c1 being a pointer because of ((64bae2cf-9355-4d13-b07e-b8395181c451))
	- ### Cartesian to Polar Conversion
	  ```rust
	  pub fn to_polar ( &self ) -> ComplexPolarNumber {
	      let r = self.modulus();
	      let theta = ( self.b ).atan2( self.a );
	      ComplexPolarNumber {
	          r,
	          theta
	      }
	  }
	  ```
	  *Note: Usage of `atan2` can be explained [here](64bc0c17-0344-47a9-a52e-136c9d836679)*
	- ### Polar Complex Multiplication
	  ```rust
	  pub fn mult ( &mut self, to_mult: ComplexPolarNumber ) -> &Self {
	      let mut r     = self.r * to_mult.r;
	      let mut theta = self.theta + to_mult.theta;
	  
	      if r < 0f32 {
	          r *= -1f32;
	          theta += std::f32::consts::PI;
	      }
	      while theta > std::f32::consts::PI {
	          theta -= std::f32::consts::TAU;
	      }
	      while theta < -std::f32::consts::PI {
	          theta += std::f32::consts::TAU;
	      }
	  
	      self.r = r;
	      self.theta = theta;
	  
	      self
	  }
	  ```
	  *Note: See [constants](64bc2af1-3770-4b2f-93a0-1e239cb31e47) in Rust
	- ### Arbitrary Complex Exponents
	  Notably, the math side of this requires you to switch only the base to polar format. In total honestly, that doesn't really make sense visually. However, makes sense logically, so I'm not going to question it.
	  ```rust
	  pub fn arbitrary_exp ( &mut self, to_exp: ComplexNumber ) -> &Self {
	      let base_as_polar = self.to_polar();
	  
	      let r = base_as_polar.r;
	      let theta = base_as_polar.theta;
	  
	      if r == 0f32 {
	          // prolly unnessecary but i'm tired
	          self.a = 0f32;
	          self.b = 0f32;
	  
	          return self;
	      }
	  
	      let c = to_exp.a;
	      let d = to_exp.b;
	  
	      self.a = ( c * r.ln() - d * theta ).exp() * ( c * theta + d * r.ln() ).cos();
	      self.b = ( c * r.ln() - d * theta ).exp() * ( c * theta + d * r.ln() ).sin();
	  
	      self
	  }
	  ```