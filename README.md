# Custom theme for slack desktop app

Custom theme for slack desktop app basing on [Wesbos `cobalt2` theme](https://github.com/wesbos/Cobalt2-Slack). For best alround theme,
use `Cobalt2` theme for the sidebar

## Usage on Mac

* cd `/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static`
* open `/ssb-interop.js`
* Add the below piece of code in the very end of the file

```javascript
document.addEventListener('DOMContentLoaded', function() {
  $.ajax({
    url: 'https://avdkishore.github.io/slack-custom-theme/index.css',
    success: function(css) {
      $("<style></style>").appendTo('head').html(css);
    }
  });
});
```
* Restart slack

> Note: This process needs to be followed whenever slack is updated
