---
{"dg-publish":true,"permalink":"/css/","tags":["Coding"]}
---

# CSS

- To learn CSS, you must learn the fundamental instead of using a premade framework
	- By learning the 'Box Model'
		- Every item should be seen as a box within another box

- Best practices in learning CSS
	- Use firefox since it has better dev tools

## Layouts
- Flexbox: `display: flex`
	- To align items to center
		- use `justify-content: center;` for verticle align
		- use `align-items: center;` for horizontal align
- Grid


- Variables: can be established, used, and overrided in css
	```css
	:root {
		--text-color: rgb(255, 0, 0);
	}

	p {
		--text-color: green; /*override	*/
		color: var(--text-color);
	}

	h1 {
		color: var(--text-color);	
	}

	h2 {
		color: var(--text-color);	
	}
	```
	

- To keep a pop up window after mouse moves to child of the button use
	```css
	button:focus-within {}
	```





>[!tip] To align vertically and horizontally you have to use flex
>```css
>display: flex;
>justify-content: center;
>align-items: center;
>```


## Responsive Design (Mobile) Methods

### 1. Media Queries
```css
@media only screen and (min-width: 768px) {
	/*Code*/
}
```

### 2. Clamp
```css
article {
	width: clamp(200px, 50%, 600px);
							/*Min  preferred Max*/
}
```
- Set the min-value (for mobiles), prefered (looks good on both), or max (for desktop)
	- Use this instead of media queries

## Link Stylesheet

```html
<link rel="stylesheet" href="mystyle.css">
```

```css
@import url('https://fonts.googleapis.com/css2?family=Epilogue:ital,wght@1,900&display=swap');
```