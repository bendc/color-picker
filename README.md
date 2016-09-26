# Usage

Insert the custom element and the library in your document:

```html
<!doctype html>
<title>Example</title>

<color-picker></color-picker>

<script src=color-picker.js></script>
```

Listen for the `color-change` event to get the selected color:

```javascript
const picker = document.querySelector("color-picker");

picker.addEventListener("color-change", () => {
  const { state } = picker;
	console.log(state); // => object containing the current rgb, hsb and hex values
});
```

Please note this component is based on the [Shadow DOM v1
spec](http://w3c.github.io/webcomponents/spec/shadow/) which might require a
[polyfill](https://github.com/webcomponents/shadydom) for older browsers.
