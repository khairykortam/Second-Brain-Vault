- some functions have parameters, others don't
- some functions return values, others don't
- ```
  square = function(x){
  return x*x;
  }
  function square(x){
  return x*x;
  }
  ```
  - local bindings
  - local can see global, but except when the same 2 variables inside and outside have the same name
  - you can change, add function values
  - function declarations can be done anywhere, in contrast to function values
  - arrow function
  - if single parameter, can omit parenthesis, other than that, parenthesis are required
  - defualt variable values