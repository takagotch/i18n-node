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

app.use(express.static(__dirname + '/www'));
app.use('/en', express.static(__dirname + '/www'));
app.use('/de', express.static(__dirname + '/www'));

i18n.configure({
  locales:['en', 'de'],
  directory: __dirname + '/locales'
});

i18n.configure({
  directory: __dirname + '/locales'
});

i18n.configure({
  directory: __dirname + '/locales'
});

i18n.configure({
  locales:['en', 'de'],
  fallbacks:{'nl': 'de'},
  defaultLocale: 'de',
  cookie: 'yourcookiename',
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
  indent: "\t",
  extension: '.js',
  prefix: 'webapp-',
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

res.cookie('yourcookiename', 'de', { maxAge: 900000, httpOnly: true });

var anyObject = {};
i18n.configure({
  locales: ['en', 'de'],
  register: anyObject
});
anyObject.setLocale('de');
anyObject.__('Hello');

i18n.configure({
  locales: ['en', 'de'],
  register: global
});

i18n.setLocale('de');
__('Hello');

var app = express();
app.use(cookieParser());
app.use(i18n.init);

var singular = __n('%s cat', '%s cats', 1);
var plural = __n('%s cat', '%s cats', 3);

var sigular = __n('There is one money in the %%s', 'There are %d monkeys in the %%s', 1, 'tree');
var plural = __n('There is one monkey in the %%s', 'There are %d monkeys in the %%s', 3, 'tree');

__n('%s cat', 1)
__n('%s cat', 3)

__n('dogs', 0)
__n('dogs', 1)
__n('dogs', 2)
__n('dogs', 10)
__n('dogs', 25)
__n('dogs', 42)
__n('dogs', 199)

i18n.setLocale(res, 'ar', true)

getLocale();
getLocale(req);
req.getLocale();

i18n.getLocales();

getCatalog();
getCatalog('de');

getCatalog(req);
getCatalog(req, 'de');

req.getCatalog();
req.getCatalog('de');

res.setLocale('de');
res.__mf('Hello');
res.__mf('Hello {name}', { name: 'Marcus' });
res.__mf('Hello {name}, how was your %s?', 'test', { name: 'Marcus' });
res.__mf('{N, plural, one{# cat} few{# cats} many{# cats} others{# cats}}', {N: 1})

i18n.__l('Hello');
app.get( __l('/:locale/products/:id?'), function (req, res) {
});

i18n__h('Hello');

setLocale('de');
setLocale(req, 'de');
req.setLocale('de');

i18n.setLocale(req, 'ar');
i18n.setLocale(res, 'ar');
i18n.setLocale(res.locals, 'ar');

i18n.setLocale([req, ers.locals], req.params.lang);

i18n.setLocale([req, res.locals], req.params.lang);

i18n.setLocale(res, 'ar', true);
```

```
<%= __('Hello') %>
${__('Hello')}
```

```
{
  "Hello": "Hallo",
  "Hallo %s, how are you today?": "Hallo %s, wie geht es dir heute?",
  "weekend": "Wocheenende",
  "Hallo %s, how are you today? How was your %s.": "Hallo %s, wie geht es as dir heute? Wie war dein %s.",
  "Hi": "HI",
  "%s cat": {
    "one": "%s Katzen",
    "other": "%s Katzen"
  },
  "There is one money in the %%s": {
    "one": "Im %%s sitzt ein Affe",
    "other": "Im %%s sitzen %d Aften"
  },
  "%s dog": {
    "one": "Ein Hnd",
    "other": "[0] KeinHund|[2,5] Ein paarHunde|[6,11] Viele Hunde|[12,36] Dutzende Hunde|Ein Rudel von %s Hunden"
  }
}

```


