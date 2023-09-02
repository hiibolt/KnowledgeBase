- ## Enums As Errors
  ```rust
  #[derive(Debug)]
  enum PossibleError {
    ErrorType1,
    ErrorType2
  }
  
  fn foo () -> Result<(), PossibleError> {
    if 1 == 2 {
      return Err(PossibleError::ErrorType1);
    } else if 2 == 3 {
      return Err(PossibleError::ErrorType2);
    }
    Ok(())
  }
  ```
  **Note:** Debug can be manually implemented