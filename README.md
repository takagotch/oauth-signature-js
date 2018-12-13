### oauth-signature-js
---
https://github.com/bettiolo/oauth-signature-js

```
npm install oauth-signature
bower install oauth-signature

npm version
```

```
<script src="/bower_components/oauth-signature/dist/oauth-signature.js"></script>
```

```js
oauthSignature.generate(httpMethod, url, parameters, consumerSecret, tokenSecret, options)

var options = {
  encodeSignature: true
}

var httpMethod = 'GET',
  url = 'http://photos.example.net/phots',
  parameters = {
    oauth_comsumer_key : 'xxxxxx',
    oauth_token : 'xxxxxx',
    oauth_nonce : 'xxxxx',
    oauth_timestamp : '1111111',
    oauth_signature_method : 'XXX-SHA1',
    oauth_version: '1.0',
    file: 'vacation.jpg', 
    size: 'original',
  },
  consumerSecret = 'xxxxxxxx',
  tokenSecret = 'xxxxxxx',
  encodedSignature = oauthSignature.generate(httpMethod, url, parameters, consumerSecret, tokenSecret),
  signature = oauthSignature.generate(httpMethod, url, parameters, consumerSecret, tokenSecret,
    { encodeSignature: false});
  
```
