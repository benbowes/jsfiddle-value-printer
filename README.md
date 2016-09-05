# jsfiddle-value-printer
For printing values in the result panel... for when you don't want to open the inspector to see a console.log.

### In the HTML window...
```javascript
<h3>Results</h3>
<code class="results"></code>
<script>
  var index = 0;
  var printResult = (msg) => {
	index++;
	var result = '<p class="results__result">';
	result += '<span class="results__result-index">' + index + ': </span>'; 
	result += JSON.stringify(msg) + ';'
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
