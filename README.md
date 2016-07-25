# BindIt.js

Simple data binding for modern browsers

## Example

```html
<div bind-it-to="name.first"></div>
<div bind-it-to="age"></div>
<input type="text" bind-it-to="name.last" bind-it-with="value" />
<div>
    <span bind-it-to="name.first" bind-it-with="makeItBold"></span> <span bind-it-to="name.last" bind-it-with="makeItBold"></span>
</div>
  
<script>
  function makeItBold(value) {
    this.innerHTML = `<b>${value}</b>`;
  }

  const state = {
    name: {
      first: 'Jane',
      last: 'Smith'
    },
    age: 21
  };
  
  let context = bindIt(state);  
</script>
```

![image](https://cloud.githubusercontent.com/assets/3384072/17116307/1ca305f6-52af-11e6-81c6-767266f63718.png)
