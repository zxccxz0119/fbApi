# FBApi
Demo: 
<a href="https://zxccxz0119.github.io/example/fbapi.html" target="_blank">https://zxccxz0119.github.io/example/fbapi.html</a>

## Getting Started
```html
<script src="https://zxccxz0119.github.io/assets/fbapi.js"></script>
```

## Usage
```html
<button onClick="login">login & get info</button> 
<button onClick="fbapi.share('https://zxccxz0119.github.io/')">share</button>
```
```js
var fbapi = new FBApi({
  appId: 'your_appid',
  version: '', // default is 'v6.0'
})

function login(){
  fbapi.login().then(()=>{
      return fbapi.getProfile()
  }).then((res) => {
      console.log(res)
  })
}
```

## feature
### checkStatus
```js
fbapi.checkStatus()
```

### login
```js
fbapi.login()
```

### getProfile
```js
fbapi.getProfile()
```

### share
`alertOpen` is `boolean`, default is `true`.
```js
fbapi.share(link,alertOpen)
```

