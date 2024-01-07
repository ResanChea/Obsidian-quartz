---
{"dg-publish":true,"permalink":"/obsidian/","title":"Obsidian","tags":["Note-Taking"]}
---

# Obsidian
## Callout Feature [^1]
>[!bug]
> This is the example here.
```markdown
> [!INFO] 
> Here's a callout block. 
> It supports **markdown** and [[Internal link|wikilinks]].
```
- Unique Themes  
	- note
	-   abstract, summary, tldr
	-   info, todo
	-   tip, hint, important
	-   success, check, done
	-   question, help, faq
	-   warning, caution, attention
	-   failure, fail, missing
	-   danger, error
	-   bug
	-   example
	-   quote, cite

- [[Mods of Obsidian\|Mods of Obsidian]]

# References
[^1]: [Use callouts - Obsidian Help](https://help.obsidian.md/How+to/Use+callouts)

# Tags
- Only use a tag on notes if you can think of a use case where you need to search up all cases of that tag
	- For example using the tag `#concepts` does not help with much becuase I would never search up all concepts at once for any use other than for looking cool

```js
let i = "";
fetch('https://www.googleapis.com/customsearch/v1?key=AIzaSyBI6Qa_CJ5vf81XKJ_Fbd8EmxYsEFWa9m8&cx=017576662512468239146:omuauf_lfve&q=lectures')
  .then(response => response.json())
  .then(data => i = data.items[1].pagemap.cse_image[0].src);

console.log( await i);

```

<p><span><img src="https://images.unsplash.com/photo-1671726203449-34e89df45211?ixid=M3wzMzQyNzd8MXwxfHNlYXJjaHwxfHxDb21wdXRlcnxlbnwwfHx8fDE3MDQ1NTY4ODd8MA&amp;ixlib=rb-4.0.3" referrerpolicy="no-referrer"></span></p>

```js
let keyword = "Banana";
var i;

let globalData = fetch(`https://www.googleapis.com/customsearch/v1?key=AIzaSyBI6Qa_CJ5vf81XKJ_Fbd8EmxYsEFWa9m8&cx=017576662512468239146:omuauf_lfve&q=${keyword}`)
    .then((response) => response.json())
    .catch(error => console.error)
const link = await globalData;
dv.paragraph(`<img src="${link.items[1].pagemap.cse_thumbnail[0].src}">`);
```


