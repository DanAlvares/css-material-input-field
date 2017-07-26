# CSS Material Input Field
An simple Angular material-like input field created using CSS only. Easily extensible for disabled states, other input types etc. 

Check out the demo on [JSFiddle](https://jsfiddle.net/dmalvares/05sL63g2/13/)

## HTML
```html
<div class="custom-input">
  <input id="EmailAddress" type="email" placeholder=" " />
  <label for="EmailAddress">Email Address</label>
</div>
```

## CSS
```css
.custom-input {
  position: relative;
}
input[type=email] {
  background: transparent;
  border: none;
  border-bottom: solid 1px #ccc;
  padding: 5px;
  transition: padding 0.4s;
}
input[type=email]:placeholder-shown + label {
  color: #aaa;
  font-size: 14px;
  left: 5px;
  top: 5px;
}
label,
input[type=email]:focus + label{
  color: #4476bd;
  font-size: 12px;
  left: 2px;
  pointer-events: none;
  position: absolute;
  top: 2px;
  transition: top 0.4s, left 0.4s, font-size 0.4s;
}
input[type=email]::placeholder{
  color: transparent;
}
input[type=email]:focus,
input[type=email]:not(:placeholder-shown) {
  border-bottom: solid 1px #4476bd;
  outline: none;
  padding: 20px 5px 5px;
}
```
