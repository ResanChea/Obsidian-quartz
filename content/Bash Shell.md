---
{"dg-publish":true,"permalink":"/bash-shell/","title":"Bash Shell","tags":["Coding"]}
---

# Bash Shell
```bash
for filename in *.md; do text=$(head -1 "$filename" | cut -c 3- | sed -e 's/[^A-Za-z0-9 ().,:;_-]//g' | sed -e 's/\ \ / /'); mv "$filename" "$text".md; done
```

```bash
# to add [[]] to each cover image
	sed -i 's/Cover\ Image:\ \(.*.jpg\)/Cover\ Image:\ \[\[\1\]\]/'
```

# Renaming Files with Bash


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/action-aids-child-sponsorship/#db4b92" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



```bash
for filename in *.jpg
do text=$(tesseract "$filename" stdout | grep "LRP")
	cp "$filename" renamed/"$text".jpg
done

## | cut -f2 -d":"| to only pick the second field to rename
##	cut -c  == means skip the first and move to the second character
## head -1 is used to only output the first line, isn't needed in this case
for filename in *.png
do text=$(tesseract "$filename" stdout | grep "KH" | awk '{print $2} | cut -c 2-)
cp "$filename" renamed/"$text".png
done
```

</div></div>
