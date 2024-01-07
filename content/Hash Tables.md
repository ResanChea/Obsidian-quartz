---
{"dg-publish":true,"permalink":"/hash-tables/","title":"Hash Tables"}
---

# Hash Tables
Hash tables or hash maps is a fundamental element in (parent:: [[Coding\|coding]]).
Hash tables are made with Hash Functions. By converting the input search-item into an index number using a [[Hash Algorithm\|Hash Algorithm]]
>[!example]
>```javascript
>int index = (input-string, max-hash) => {
>	for(let i=0; i<input-string.length; i++) {
>		//Turn each letter into a number and add them to one variable to get unique number (hashing algorithm)
>		int num += input-string.charCodeAt(i);
>	}
>	return index;
>}
>```
