```js
const iframe = document.createElement('iframe');
document.body.appendChild(iframe);

const token = JSON.parse(iframe.contentWindow.localStorage.token);
console.log('Token:', token);
const tempInput = document.createElement('input');
tempInput.value = token;
document.body.appendChild(tempInput);
tempInput.select();
document.execCommand('copy');
document.body.removeChild(tempInput);

iframe.remove();
```
