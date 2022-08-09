# auto-validation-form.js
##### A library used to verify registration/login form.

## Contributors
### So much appreciate for Mr.Sơn Đặng - Founder of "Cộng Đồng Học Lập Trình F8", Mr.Hữu Lộc 

## Installation and Usage 

#### Server-side usage
##### Install the library with ```npm install auto-validation-form```
```
npm install auto-validation-form
```

#### Client-side usage
#### Install
```
<script type="module" src="./app.js"></script>
```
#### Usage
##### In app.js
```
import { Validator } from './node_modules/auto-alidation-form/validator.js';

var form =  new Validator('#idForm', '.classNameFormGroup', '.classNameErrorMessage'); 
```
##### Rules: 

| Rules's name     | Uses                                                                |
| ---------------- |:-------------------------------------------------------------------:|
| required         | Is input required?                                                  |
| email            | Verify email is correct.                                            |
| min              | Minimum characters for input.                                       |
| max              | Maximum characters for input.                                       |
| confirmPassword  | Verify input "Re-enter password".                                   |
| checked          | Is type="radio" and type="checkbox" of input required?              |

##### How to use rules?
###### You just need to add our predefined rules attribute, then add a value to that attribute depending on your needs.

##### Can I use more than one rule in input tag?

###### Absolutely yes! If you want to use one more rule, you just need to add the rule name directly to the value of the "rules" attribute in the input tag, then separate the values ​​with a "|".

##### Example:
###### index.html
```
<form action="" method="POST" class="form" id="register-form">
    <div class="title">Welcome</div>
    <div class="subtitle">Let's create your account!</div>

    <div class="form-group">
        <input id="fullname" name="fullname" class="input" rules="required" type="text" placeholder=" " />
        <label for="fullname" class="placeholder">Full name</label>
        <span class="form-message"></span>
    </div>

    <div class="form-group">
        <input id="email" name="email" class="input" rules="required|email" type="text" placeholder=" " />
        <label for="email" class="placeholder">Email</label>
        <span class="form-message"></span>
    </div>

    <button type="text" class="submit">Submit</button>
</form>
```
###### app.js
```
Validator('#register-form', '.form-group', '.form-message');
// Validator('#idForm', '.classNameFormGroup', '.classNameErrorMessage');
```



