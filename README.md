# html-imports-safari-bug
Reproducing bug with html imports and safari.

Initially reported here:
http://stackoverflow.com/questions/29291578/difficulty-using-html-import-for-javascript-dependencies-with-polymer-on-firefox

## Steps to Reproduce
Run with
`python -m SimpleHTTPServer`

Navigate to [localhost:8000](http://localhost:8000) in Chrome and Safari.

Click on button. You will see an error in Safari's console `ReferenceError: Can't find variable: _` but no error in Chrome.

## Workaround
In `lodash.html`, remove the `type="application/javascript"` from the `<script>` tag.
