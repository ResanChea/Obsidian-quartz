---
{"dg-publish":true,"permalink":"/js-image-web-scraping-project/"}
---

# JS Image Web-Scraping Project

<p><span><img src="https://images.unsplash.com/photo-1565817292726-56c96f34355b?ixid=M3wzMzQyNzd8MHwxfHNlYXJjaHwxfHxPYnNpZGlhbnxlbnwwfHx8fDE3MDQ1NTY4Njl8MA&amp;ixlib=rb-4.0.3" referrerpolicy="no-referrer"></span></p>

```js
let keyword = "Laptop";
let apikey = "PAvZP9jtaLvN46_EcWUw161Vh7Rjj9aBxtGAnZOc2Ck";
let globalData = fetch(`https://api.unsplash.com/search/photos?query=${keyword}&client_id=${apikey}`)
    .then((response) => response.json())
    .catch(error => console.error)
const link = await globalData;
dv.paragraph(`![](${link.results[0].urls.raw})`);
```