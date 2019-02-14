### i18-node
---
https://github.com/mashpie/i18n-node

```
npm install i18 --save
npm test

DEBUG=i18n:* node app.js
DEBUG=i18n:warn,i18n:error node app.js
```

```js
var express = require('express'),
  i18n = require("i18n");

i18n.configure({
  locales:['en', 'de'],
  directory: __dirname + '/locales'
});

var greeting = i18n.__('Hello');

app.configure(function(){
  app.use(i18n.init);
});

app.get('/de', function(req, res){
  var greeting = res.__('Hello');
});







i18n.configure({
  logDebugFn: function (msg) {
    console.log('debug', msg);
  },
  
  logWarnFn: function (msg) {
    console.log('warn', msg);
  },
  
  logErrorFn: function(msg){
    console.log('error', msg);
  }
});

var greetings = [];
for(var i=0; i < greetings.length; i++) {
  console.log( __(greetings[i]) );
};

app.use(epress.static(__dirname + '/www'))
app.use();
app.use();

i18n.configure({
  locales:[],
  directory: __dirname + '/locales'
});

i18n.configure({});

i18n.configure({
  locales:[],
  fallbacks:{},
  defaultLocale:'',
  cookie: '',
  queryParameter: '',
  directory; '',
  directoryPermissions: '',
  autoReload: true,
  updatefiles: false,
  syncFiles: false,
  indent: "",
  extension: '',
  prefix: '',
  objectNotation: false,
  logDebugFn: function (msg) {
    console.log('debug', msg);
  },
  logWarnFn: function (msg) {
    console.log('warn', msg);
  },
  logErrorFn: function (msg) {
    console.log('error', msg);
  },
  register: global,
  api: {
    '__': 't',
    '__n': 'tn'
  },
  preserveLegacyCase: true
});
```

```
<%= __('Hello') %>
${__('Hello')}

```

```
{
  "": "",
  "": "",
  "": "",
  "": "",
  "": {},
  "": {},
  "": "",
  "%s dog": {
    "one": "Ein Hnd",
    "other": "[0] KeinHund|[2,5] Ein paarHunde|[6,11] Viele Hunde|[12,36] Dutzende Hunde|Ein Rudel von %s Hunden"
  }
}

```


