# auto-validation-form.js
##### A library used to verify registration/login form.

## Installation and Uasge 

#### Server-side usage
##### Install the library with ```npm install auto-validation-form```
#### Usage
##### In app.js
```
import { Validator } from './node_modules/auto-alidation-form/validator.js';

var form =  new Validator('#idForm', '.classNameFormGroup', '.classNameErrorMessage'); 
```
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
```

#### Client-side usage
#### Install
```
<script type="module" src="./app.js"></script>
```

