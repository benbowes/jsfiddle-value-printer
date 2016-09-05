# jsfiddle-value-printer
For printing values in the result panel... for when you don't want to open the inspector to see a console.log.

```javascript
<script>
  // printResult function purely for jsFiddle
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
