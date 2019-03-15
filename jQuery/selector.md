### selector

```javascript
$('[attribute|="@"]'); // has prefix @, delimeted by '-'
// '@aa' -> (x), '@' -> (o), '@-aa' -> (o);

$('[attribute*="@"]'); // contains @

$('[attribute~="@"]'); // contains word @, delimeted by space

$('[attribute$="@"]'); // end with @

$('[attribute="@"]'); // equal with @

$('[attribute!="@"]'); // not equal with @

$('[attribute^="@"]'); // start with @

$('[attribute]'); // has attribute

$('[attribute1="@"][attribute2="!"]'); // multiple attribute selector
```

