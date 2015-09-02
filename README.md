# Changing the input password bullet

### This repo provides instructions & a simple demo showing how to replace the input password bullet in Webkit browsers.

* Go to [Fontello](http://fontello.com/), or equivalent site.
* Choose or upload an icon.

    ![fontello-select-glyph](https://cloud.githubusercontent.com/assets/136959/9632072/7b3650c6-514a-11e5-94ca-c41baf55c774.png)

* Select "Customize Codes" tab.
* Change the glyph destination to U+"2022" to replace the bullet symbol.

    ![fontello-customize-code](https://cloud.githubusercontent.com/assets/136959/9632061/6cab24dc-514a-11e5-89b4-29043b6d781c.png)

* Download webfont.
* Include the font files on your site, and include the following css (Note, the `0000` will change depending on the glyph & glyph destination)

```css
/* Use the css below to change the password input symbol */
@font-face {
	font-family: 'fontello';
	src: url('./font/fontello.eot?0000');
	src: url('./font/fontello.eot?0000#iefix') format('embedded-opentype'),
	url('./font/fontello.woff?0000') format('woff'),
	url('./font/fontello.ttf?0000') format('truetype'),
	url('./font/fontello.svg?0000#fontello') format('svg');
	font-weight: normal;
	font-style: normal;
}

input[type="password"] {
	font-family: "fontello";
	font-style: normal;
	font-weight: normal;
	speak: none;

	/* For safety - reset parent styles, that can break glyph codes*/
	font-variant: normal;
	text-transform: none;

	/* Font smoothing. That was taken from TWBS */
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	/* Uncomment for 3D effect */
	/* text-shadow: 1px 1px 1px rgba(127, 127, 127, 0.3); */

	/* add spacing to better separate each image */
	letter-spacing: 2px;
}
```

* [Check out the demo](http://mottie.github.io/input-password-bullet/) (reminder, this method only works in Webkit browsers)

    ![password-input-typing](https://cloud.githubusercontent.com/assets/136959/9646930/d1b4e70c-519d-11e5-811a-57fea2b6519c.gif)
