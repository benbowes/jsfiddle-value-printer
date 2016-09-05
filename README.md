# jsfiddle-value-printer
For printing values in the result panel... for when you're too lazy to open the inspector to view console.log() output.

### In the HTML window...
```javascript
<h3>Results</h3>
<pre class="results"></pre>
<script>
  var index = 0;
  var printResult = function(msg) {
    index++;
    var result = '<p class="results__result">';
    result += '<span class="results__result-index">' + index + ': </span>'; 
    result += JSON.stringify(msg, null, 2) + ';'
    result += '</p>';
    document.querySelector('.results').innerHTML += result;
  }
</script>
```

### In the CSS window...
```css
body {
  font-family: sans-serif;
  padding: 1em;
}

.results {
  padding: 0.5em 1em;
  background: #fff;
  display: block;
}

.results__result:not(:last-child) {
  border-bottom: 1px solid #f1f1f1;
}

.results__result {
  padding: 1em;
}

.results__result-index {
  color: #ccc;
}

```
