<h1 class="capitalize">COMD2451</h1>
<h2 class="capitalize center">Basic Responsive Site Navigation</h2>

---

<section class="section">
    <h2 class="sentence">The nav element: basic HTML markup</h2>

As ***discussed*** in the `slide deck` [COMD2451 Sectioning HTML Documents, Adding external style sheets](https://github.com/interglobalmedia/sectioning-html/blob/master/sectioning-html.md), the `nav element` can be ***placed within*** the `header element` at the ***top*** of the `HTML document`:

```html
<nav>
    <ul>
        <li>
            <a href="index.html">Home</a>
        </li>
        <li>
            <a href="portfolio.html">Portfolio</a>
        </li>
        <li>
            <a href="resume.html">Résumé</a>
        </li>
        <li>
            <a href="about.html">About</a>
        </li>
        <li>
            <a href="contact.html">Contact</a>
        </li>
    </ul>
</nav>
```

It's ***even better*** if we ***wrap*** the `nav element` in a `header element` ***like so***:

```html
<header>
    <nav>
    <ul>
        <li>
            <a href="index.html">Home</a>
        </li>
        <li>
            <a href="portfolio.html">Portfolio</a>
        </li>
        <li>
            <a href="resume.html">Résumé</a>
        </li>
        <li>
            <a href="about.html">About</a>
        </li>
        <li>
            <a href="contact.html">Contact</a>
        </li>
    </ul>
</nav>
</header>
```

The ***above*** are the ***pages*** you will ***end up*** with for your `portfolio site` by the ***end*** of the `course`.

</section>

---

<section class="section">
	<h2 class="sentence">Adding a header element to wrap around the nav element</h2>

***First*** we **need** to ***add*** a `header element` to the ***top*** of the `body` of the `HTML document`. It will ***wrap around*** the `nav element`. We are ***doing*** this ***because*** we will be ***adding*** `additional content` to the `"header" area` of ***each*** of our `HTML pages`. So ***now*** the ``"header area"`` ***containing*** the `navigation menu` should ***look*** like ***this***:

```html
<header>
	<nav>
	    <ul>
	        <li>
	            <a href="index.html">Home</a>
	        </li>
	        <li>
	            <a href="portfolio.html">Portfolio</a>
	        </li>
	        <li>
	            <a href="resume.html">Résumé</a>
	        </li>
	        <li>
	            <a href="about.html">About</a>
	        </li>
	        <li>
	            <a href="contact.html">Contact</a>
	        </li>
	    </ul>
	</nav>
</header>
```

</section>

---

<section class="section">
	<h2 class="sentence">Populating the header area with other markup</h2>

***Now*** we ***have*** to **populate** the `header area` with the ***other markup*** that ***resides outside*** of the `navigation menu`. We have ***added*** the `header` so that we can ***group*** `related elements` in ***one place***. This ***also*** makes it ***even more*** `semantic` ***for*** the `browser` and `search engines`.

We are ***going*** to be ***adding*** an `a` (`anchor`) `element` ***which*** will ***contain*** our ***text-based*** `logo`, and we will ***add*** a `button element` ***below*** the `a element` for our ***responsive*** `hamburger menu`, ***which*** will ***only appear*** in `screen widths` ***less than*** `< 900px`.

The `header area` ***should*** `look like` the ***following*** now:

```html
<header>
	<a href="#">MDC</a>
	<button></button>
	<nav>
	    <ul>
	        <li>
	            <a href="/home">Home</a>
	        </li>
	        <li>
	            <a href="/portfolio">Portfolio</a>
	        </li>
	        <li>
	            <a href="/resume">Résumé</a>
	        </li>
	        <li>
	            <a href="/about">About</a>
	        </li>
	        <li>
	            <a href="/contact">Contact</a>
	        </li>
	    </ul>
	</nav>
</header>
```

</section>

---

<section class="section">
	<h2 class="sentence">Adding classes and/or ids to the header area</h2>

We ***still*** `need` to ***add*** `classes` to our `header area` ***markup*** so that we `can` ***style*** it ***more specifically*** based on ***which classes*** `target` ***which elements***. As `HTML markup` becomes ***more complex***, and we ***add*** `more elements` ***within*** `different sections` and `different sections` with ***more*** `elements` that ***may need*** to be ***displayed*** in ***different ways*** and ***possibly*** even `different states`, we ***have*** to ***start applying*** `classes` to ***these*** `elements`. In ***certain cases***, we ***may apply*** `ids`.

***Here***, we will be ***applying*** a `class` to the `header`, a `class` to the `a element` ***containing*** the `logo`, a `class` to the `button` ***containing*** the `hamburger menu`,  and a `class` to the `nav element`, a `class` (the ***same one***) to the `a elements` ***inside each*** `li element` ***within*** the ***unordered list*** (`ul`) ***inside*** the `nav element`.

***This*** is what it ***should*** look like:

```html
<header class="header">
	<a href="#"
	   class="logo">MDC</a>
	<button class="hamburger" aria-label="Right-Align"></button>
	<nav class="navbar">
		<ul>
			<li>
				<a class="menu-link"
				   href="index.html">Home</a>
			</li>
			<li>
				<a class="menu-link"
				   href="portfolio.html">Portfolio</a>
			</li>
			<li>
				<a class="menu-link"
				   href="resume.html">Résumé</a>
			</li>
			<li>
				<a class="menu-link"
				   href="about.html">About</a>
			</li>
			<li>
				<a class="menu-link"
				   href="contact.html">Contact</a>
			</li>
		</ul>
	</nav>
</header>
```

</section>

---

<section class="section">
    <h2 class="sentence">Creating the styles folder for the main.css file the <code>main.css</code> file</h2>

If we ***simply added*** `HTML markup` for the `header/nav element` ***without*** any ***styling***, ***all*** the **content** would be ***aligned*** to the ***left*** of the `HTML page `by ***default***. ***Naturally***, we ***don't want*** our `page` to ***look*** like ***that***!

<aside>
    Note: Show students what this would look like.
</aside>

In ***order*** to ***rectify*** this, we ***first*** `need` to ***create*** an ***external*** `style sheet` in ***which*** we can ***add*** our `CSS` for ***all*** of our ***pages***.

To ***do*** this, ***inside*** of the `Brackets` ***code editor*** and at the ***root*** of our `project folder`, we ***create*** a ***new*** `main.css` ***file***.

***First***, we ***have*** to ***click*** on the `File tab` in the `Brackets` ***navigation menu***, and ***select*** `New`. As a ***result***, the `Brackets` ***code editor*** `window` should ***look*** something like ***this***:

<div>
    <img src="images/creating_new_file_brackets.png" alt="Creating a new file in Brackets">
</div>

A ***new*** `file` ***entitled*** `Untitled-1` ***should appear*** to the ***left*** of the `Brackets` ***code editor*** `window`.

***Next***, ***right click*** on `Untitled 1`, and ***select*** *`"Save As"`* ***from*** the ***file drop down***. As a ***result***, the ***following*** should ***appear***:

<div>
    <img src="images/file_save_as_brackets.png" alt="File Save As command in Brackets">
</div>

In the *`"Save As"`* **input field**, ***type*** `main.css`. You will ***also see*** that the `file` will be ***saved*** in the ***folder*** that you are ***currently*** in, so ***make sure*** that you are ***saving*** the `file` in the ***right location***!

***After*** you have ***named*** the `file` ***inside*** the *`"Save As"`* **input field**, ***click*** on the *`Save`* **button**.

***Now***, when you ***look*** to the ***left*** of your `Brackets` ***code editor*** `window`, you ***should see*** your ***newly*** `created` `main.css` ***file***.

`Cut` and `paste` ***any*** `CSS` you have ***placed*** in the `style element` ***inside*** the `head element` of your `index.html` ***into*** your ***new*** `main.css` ***external*** `style sheet`.

The `same process` ***applies*** if you are **now using** the `Atom` **code editor**.

</section>

---

<section class="section">
    <h2 class="sentence">Adding the external style sheet to the <code>index.html</code> head element</h2>

***Now*** we ***have*** to ***add*** the ***external*** `style sheet`, `main.css`, to the `head element` in our `index.html` ***file*** `using` the `link element`.

Our `link element` ***should*** be ***placed*** `below` the `title element`, and it should ***look*** something ***like*** the ***following***:

```html
<link rel="stylesheet" href="main.css">
```

Our ***next step*** will be to ***place*** this `main.css` file ***into*** a ***new*** `folder` ***entitled*** `styles` ***located*** at the ***root*** of our `project folder`.

</section>

---

<section class="section">
    <h2 class="sentence">Creating the styles folder for the main.css file</h2>

***Now*** we ***have*** to ***create*** a ***new*** `folder` ***called*** `styles` ***inside*** the ***root*** of our `project folder`.

In ***order*** to ***do*** that, ***inside*** the `Brackets` ***code editor*** `opened` ***from*** our `project folder` (***almost*** the `identical process` to ***our steps*** for ***creating*** the `main.css` ***file***), and ***right-click*** on the `main.css` ***file***. A ***drop down*** will ***appear***. ***Select*** `new folder`. As a ***result***, the ***following*** should ***appear*** to the ***left*** of your `Brackets` ***code editor*** `window`:

<div>
    <img src="images/create_new_folder_brackets.png" alt="Creating a new folder with Brackets">
</div>

***Right-click*** on `Untitled 1` (or ***whatever number*** `shows up` ***for*** you), and ***select*** `Rename`. ***Rename*** the ***folder*** `styles`.

***Next***, ***drag*** the `main.css` ***file*** into the ***new*** `styles folder`.

The `same process` ***applies*** if you are **now using** `Atom`.

</section>

---

<section class="section">
    <h2 class="sentence">Creating an images folder for the images from Project 1</h2>

`Update 3.9.21`: We are ***not going*** to be **using** `Unsplash` **images** in our `portfolio site`, so this `slide` should ***only*** be **used** as a **general reference**!

Your `project folder` should  ***already contain*** `images` you ***used*** for `Project 1`. This will ***only apply*** to `Unsplash images` you may have ***downloaded*** from your `collection` ***saved there*** (if that's the way you ***wanted*** to ***go***).  

***Now*** we ***want*** to ***organize*** our `folder` ***even more*** by ***adding*** a ***new*** `images folder` in ***which*** we will ***place*** those `images`.

***Follow*** the ***same*** `steps` ***made*** for ***creating*** the `styles folder `for the `main.css` ***external*** `style sheet`. The ***only difference*** will ***be*** that ***this folder*** should be ***called*** *`"images"`*.

***After*** you have ***created*** the ***folder***, ***drag*** the `images` ***into*** it.

Since we are ***only using*** `Creative Commons` **images** in our `portfolio.html` **page** for `Project 1`, `this step` ***does not apply*** at this time. But it is ***still good*** for you to **know** ***how*** to ***do*** it!

</section>

---

<section class="section">
    <h2 class="sentence">Adding a CSS reset</h2>

***Before*** we ***add*** any ***styling*** to the `HTML elements`, we ***add*** a `CSS reset` to the ***top*** of the `main.css` ***file***.

***What*** is a `CSS reset`? The `idea` ***behind*** a `CSS reset` is to ***deal*** with ***inconsistencies*** `across browsers`.

I have ***found*** that the ***best*** `CSS reset` is the ***most*** `minimal`. That's ***because*** we ***want*** to be ***able*** to ***add*** our ***own*** `styling` to our `HTML elements` ***using*** our ***own*** `CSS selector` ***rule sets***. Buy `using` a ***large amount*** of `CSS` we ***don't*** necessarily ***even want*** to ***use*** in the ***end***, we are ***loading*** our ***project*** with ***extraneous*** and ***potentially*** `unused` *`CSS`*, ***thereby*** *`slowing down`* the ***loading*** of our `site pages` (***mentioned previously*** when we ***discussed*** `internal` ***vs*** `external style sheets`).

The ***following*** is the `CSS reset` I ***usually add*** to my `external style sheets` at the ***top*** of the ***page***:

```css
* {
	box-sizing: border-box;
    margin: 0;
    padding: 0;
	/* to fix the way Safari 14+ reads certain Google Fonts incorrectly */
	-webkit-locale: auto;
  	white-space: normal;
}
```

***Apparently***, ***according*** to `CSS Tricks`, in their ***article*** entitled [Reboot, Resets, and Reasoning](https://css-tricks.com/reboot-resets-reasoning/), the `approach` ***right above*** is a ***favorite*** amongst ***developers***!

For the **purpose** of ***my*** `portfolio site`'s **use** of ***certain fonts***, ***specifically*** the `default monospace`, I **had** to ***add*** the **property declarations** `-webkit-locale: auto;` and `white-space: normal;` to the `universal selector` **rule set** so that `Safari 14+` would **recognize** a ***default*** `monospace font`.

The `-webkit-locale` is the `-webkit` **prefixing** of the `locale` **CSS property**. The `locale` **CSS property** is a **set** of `language-` or `country-based` **preferences** for a `user interface`. A `program` ***draws*** its `locale setting`s from the `language` of the `host system`. Among ***other things***, `locales` **represent** `paper format`, `currency`, `date format`, and `numbers` ***according*** to the `protocols` in the ***given region***.

**According** to [Wikipedia's Locale page](https://en.wikipedia.org/wiki/Locale),

> (In computer software) Locale can refer to a set of parameters that defines the user's language, region and any special variant preferences that the user wants to see in their user interface—usually a locale identifier consists of at least a language identifier and a region identifier.

The `white-space property` **sets** how the `white space` ***inside*** an `element` is **handled**. When the `white-space property` is set to the `value` of `normal`, **sequences** of `white space` are `collapsed`. `Newline characters` in the `source` are ***handled*** the **same** as ***other*** `white space`. `Lines` are `broken` as **necessary** to ***fill*** `line boxes`. So there **must be** something about `white-spaces` ***not*** being handled **properly** by `Safari 14+`, **resulting** in the ***improper rendering*** of ***some*** `Google Fonts`. ***Some developers*** in **threads** on `Github` think that it's a `Google` **issue**. I ***personally think*** it is a `Safari 14+` **issue**. ***Why then*** did `Firefox` have ***no problems*** `recognizing` the ***same default*** `monospace font`?

We will `discuss` (`discussed`) ***more about*** the `box-sizing` ***property declaration*** when we ***get*** to the `CSS Box System`.

</section>

---

<section class="section">
	<h2 class="sentence">Styling the header logo for larger screens</h2>

The ***first thing*** in our `navigation menu` we ***have*** to ***style*** for ***larger screens*** is the `header logo`.

We ***will*** be ***using*** the `.header` ***class*** we ***applied*** to the the `header element` and the `.logo` ***class*** we ***applied*** to the `anchor element`.

I ***add*** the ***following*** `CSS` to my `main.css` ***file*** `right below` the ***desktop*** `rule set` for my `hamburger` ***class***:

```css
/* Logo Styling */
.header {
    margin-top: 2rem;
}

.header .logo {
	/* background: #f79ece; */
	font-size: 1.75rem;
	height: 76px;
	letter-spacing: 0.07rem;
    text-align: center;
    text-decoration: none;
	vertical-align: bottom;
    width: 93.44px;
}
/* End Header Logo Styling */
```

I ***targeted*** the `header element` by its `.header` ***class*** with the `margin-top: 2rem` ***property declaration***. This ***moved*** the `header` ***down*** from its ***normal*** `margin-top` ***flow*** `down` by `2rem`.

***Next***, I became ***more specific*** about ***how*** I ***targeted*** `styling` the `anchor element` with the class of `.logo`, ***because*** it is ***not*** the ***only*** `element` ***inside*** the `header`. I **had** to ***make sure*** that I was ***specifically targeting*** it and ***not*** any other `element` ***inside*** the `header`.

I ***applied*** the `font-size: 1.75rem;` to ***set*** the ***desired*** `font-size` of the `anchor element` with the **class** of `.logo`. It ***should*** be ***larger*** than the `font-size` of the `a elements` ***inside*** the `navigation menu`.



I ***applied*** the `text-align: center;` ***property declaration***, because I ***wanted*** to ***center*** the `logo text` ***inside*** the `anchor element`'s `"box"`.

I ***applied*** the `text-decoration: none;` ***property declaration*** so that there ***would*** be ***no*** `underlining` ***under*** the `logo text`.

***Next***, I ***added*** the `vertical-align: bottom:` ***property declaration*** to ***place*** my `logo text` ***more towards*** the `bottom` of its `"box"`.

***Next***, I ***had*** to ***specify*** a `fixed width` and `height` to the `logo` ***so that*** its `size` would ***remain*** the ***same*** no matter the ***size*** of the `viewport`. I did ***not*** want it to ***fluidly change*** its `dimensions` with the ***change*** in `viewport size` in ***any way***.

</section>

---

<section class="section">
    <h2 class="sentence">Styling the nav element: desktop</h2>

***Next***, we are ***going*** to ***add*** `styling` for the `nav element`, ***placing*** it in the `main.css` ***file***.

```css
nav {
    width: 100vw;
    /* background: #D6EFFF; */
	background: transparent;
}
```

In the **production version** of my **portfolio site**, I **place** this `rule set` ***below*** the `@media rule` for the `section @media query` of `max-width: 799px`. Here, the ***above*** `rule set` ***should*** be ***placed below*** the `universal selector` (`*`) `rule set`. You can ***refer*** to the `external stylesheet` **located inside** the `styles folder` at the `root` of this `slide deck directory`.

***First*** we `target` the `width property` on the `CSS nav selector` ***with*** a ***value*** of `100vw`. Just as `vh` is a `length unit` in `CSS` (as are `px`, `em`, `rem`, and `100%`, for ***example***),  `vw` is ***also*** a `length unit`. But ***it***, like `vh`, is a `relative length unit`. It is *`relative`* to `1%` of the` viewport width`. This ***means*** that `1vw` is ***equivalent*** to `1%` of the `viewport width`. `100vw` is ***equivalent*** to `100%` of the `viewport width`.

***Again***, `relative length units` are ***great*** for `responsive design`. `Absolute length units` are ***not***. That is ***because*** `absolute length units` are ***fixed*** (they ***don't adapt*** to the ***change*** in the `viewport size`), and will ***appear exactly*** as the ***expressed dimension*** (i.e., `50px`).

***Other*** `relative length units`:

`em`: `em` is ***calculated*** as `1em = 2in`. So `1.5em` ***would be*** `3in`. And so on. `em` ***depends*** on the `font` on the ***page***, and ***may*** be ***different*** for ***each*** `element` in the `document`. The `em` is ***simply*** the `font size`.

***According*** to `W3C` in their article ***entitled*** [EM, PX, PT, CM, IN…](https://www.w3.org/Style/Examples/007/units.en.html),

> Expressing `sizes`, such as `margins` and `paddings`, in `em` ***means*** they are ***related*** to the `font size`, and if the `user` has a ***big font*** (e.g., on a ***big screen***) or a ***small font*** (e.g., on a `handheld device`), the `sizes` will be in ***proportion***. `Declarations` such as `text-indent: 1.5em` and `margin: 1em` are ***extremely common*** in `CSS`.
-- <cite>[EM, PX, PT, CM, IN…](https://www.w3.org/Style/Examples/007/units.en.html) -- W3C</cite>

***As for*** the `background: #D6EFFF;` ***declaration***, it ***adds*** a `light blue` ***background*** to the `navigation menu`.

`rem`: ***stands*** for the `root em`. It is the `font size` of the `root element` of the `document`. The `root element` of the `document`, is you ***guessed*** it, the `html element`. ***Unlike*** `em`, which ***may*** be ***different*** for ***each element***, the `rem` is `constant` ***throughout*** the `document`. `1rem` is ***equivalent*** to `16px`.

</section>

---

<section class="section">
    <h2 class="sentence">Styling the ul element with Flexbox: desktop</h2>

The ***way*** we ***will*** be ***styling*** the `ul element` for ***desktop*** is *`interesting`*, and I think ***really cool***.

```css
ul {
    display: flex;
    justify-content: flex-end;
	/* added in my production styling of the ul for the desktop navigation */
	margin-top: -2rem;
    margin-bottom: 1.5rem;
}
```

***Here***, we `target` the `ul element selector` ***with*** a `display: flex` (`property`) `declaration`. What ***does*** this ***new*** `CSS` ***refer*** to, ***do***, and ***mean***?


The `Flexible Box Module`, ***aka*** `Flexbox`, was ***designed*** as a ***one-dimensional*** `layout model`, ***and*** as a `method` that ***provided*** `distribution` of ***space*** between ***items*** and ***powerful*** `alignment capabilities`.

So ***what*** does `one-dimensional` ***mean*** as ***relates*** to `Flexbox`? It ***means*** that `Flexbox` ***deals*** with `layout distribution` ***one dimension*** at a ***time***. In ***other*** words, ***either*** as a `row` or a `column`.

When we ***target*** a `CSS selector` ***with*** the `CSS property` ***declaration*** `display: flex`, it ***means*** that we are ***spatially distributing*** it `horizontally`, ***via*** the `row dimension`. `CSS selectors` are ***targeted*** via the `row dimension` by ***default***. If we ***wanted*** to ***target*** a `selector` ***via*** the `column dimension`, we would ***have*** to ***target*** the `selector` ***with*** the `flex-direction: column;` ***property declaration***. But ***here***, we ***don't want*** to `target` the `ul selector` ***with*** the `CSS property` ***value*** of `column.` We want the ***default*** `spatial distribution` of `row`.

***Next***, I ***wanted*** the `navigation menu` to be ***situated*** to the `right side` of the `nav`. That's ***where*** the `justify-content: flex-end` ***property declaration*** comes in.

The `justify-content property` is ***used*** to `align items` on the `main axis`. ***Here***, it is the ***direction*** which `flex-direction` or the ***default*** `flex behavior` of `row` ***from*** the `display: flex` ***property declaration*** `defines`. In ***our*** case, the ***main axis*** is the `row` (or `horizontal`) `axis`.

There are `6 values` one can ***apply*** to the `justify-content` ***property***.

The ***first value*** is `flex-start`, which would ***place*** the` ul` ***all*** the ***way*** to the `left` ***within*** the `nav`.

The ***second value*** is the `center` ***value*** which ***places*** the `ul` ***right*** in the ***center*** of the `nav`.

 The ***third value*** is the `flex-end` ***value***, which ***places*** the `ul` ***all*** the ***way*** to the `right` ***within*** the `nav`.

 The ***last*** `three values` we ***can apply*** to the `justify-content property` are `space-around`, `space-between`, and `space-evenly`. ***However***, we will ***not*** be `using` them ***here***.

To ***learn more*** about the `justify-content property`, please ***visit*** the [Basic concepts of flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) on `MDN`.

We can ***take*** a ***look*** in the `browser` and ***see*** what our `navigation menu` ***looks like*** so ***far***.

</section>

---

<section class="section">
    <h2 class="sentence">Styling the li element: desktop</h2>

***Next***, we ***have*** to `style` the `li elements`. ***Right now*** there is ***very little*** `space` ***between*** the ***edges*** of the `nav` and the `content` of the `li elements`.

<aside>
    Note: we should take a look at what the navigation menu looks like at this point in the web browser.
</aside>

```css
li {
	font-size: 2.75vh;
    list-style-type: none;
    /* margin: 2vw; */
	/* added in my production styling of the li for the desktop navigation */
	margin: 0.5vw;
}
```

***This*** `rule set` ***should*** be ***placed*** `right under` the `ul selector` ***rule set***.

***First*** we **make** the `font size` a ***size*** that is ***readable***. That's ***where*** the `font-size` ***property declaration*** with its ***value*** of `2.75vh` comes in.

***Next*** we have the `list-style-type` ***property declaration*** with the ***value*** of `none`. What this ***means*** is that we ***don't want*** to ***display*** any `bullets` (or `numbers` in the ***case*** of an `ordered list`) to the ***left*** of the `list items`.

***Next***, we ***have*** the `margin` ***shorthand*** `property declaration` ***with*** a ***value*** of `2vw`. What this ***means*** is that we are ***applying*** a `margin-top`, `margin-right`, `margin-bottom`, and `margin-left` ***property*** with a ***value*** of `2vw` to ***all***. This ***creates*** a ***nice*** `amount` of `room` ***around*** the `list items`.

***Now***, when we ***look*** at the ***changes*** in the ***browser***, we ***see*** that the `text` for the `list items` is ***much more*** `prominent` and ***easier*** to ***read***. But we ***do notice*** that the `text` is ***still blue*** (the ***default*** `color` for the `a element`) and is `underlined`. That ***too*** is a ***default*** (`user-agent`) `styling` for the `a element`.

</section>

---

<section class="section">
    <h2 class="sentence">Styling the a element: desktop</h2>

```css
a {
	color: black;
	cursor: pointer;
	padding: 2vw;
	text-decoration: none;
}
```

***This*** `rule set` ***should*** be ***placed*** `below` the (***previous***) `li rule set` in `main.css`.

The ***first*** `property declaration` ***here***, `color: black;` ***changes*** the `color` of the `list item a element` ***from*** `blue` to `black`. You can ***make*** it ***whatever*** `color` you ***want***! A ***great resource*** for ***that*** is [color-hex.com](https://www.color-hex.com/color-palettes/). I ***use*** it ***all*** the ***time***.

The ***second*** `property declaration`, `cursor: pointer;`, **makes** the `mouse pointer` **look like** a `hand` when one **hovers over** the `element selector` that **contains** the `cursor: pointer;` **property declaration**. The `cursor property` **controls** what the `mouse cursor` will **look like** when it is ***located*** over the `element` in which this `property` is **set**. ***Ultimately***, it **results** in a ***better*** `user experience` when ***targeting*** `elements` that a **user** would **normally want** to ***hover over***, like `hyperlinks` in `anchor elements`, for ***example***!

The ***third*** `property declaration`, `padding: 2vw`, ***creates*** `padding` ***around each*** `list item a element`. It just ***spaces out*** the `list item elements` ***nicer*** than ***simply applying*** a `margin` ***around*** the `list items` ***only***.

The ***fourth*** `property declaration` ***here***, `text-decoration: none;` ***removes*** the ***default*** `underline` ***from*** the `list item a element`.

<aside class="notes">
Note: We can check out the difference in layout with and without the a selector padding property declaration in the browser.
</aside>

</section>

---

<section class="section">
    <h2 class="sentence">Styling the a element with the :hover pseudo-selector</h2>

***Next***, we ***want*** to `define` a ***special state*** of the `a element` ***using*** the `:hover pseudo-selector`. **Specifically**, it is **used** to `select elements` when you **mouse over** them.

What is a `pseudo-selector` in `CSS`? A `pseudo-selector` is ***used*** to ***define*** a `special state` of an `element`.

**Syntax**:

```css
selector:pseudo-selector {
  property: value;
}
```

`Pseudo-selectors` are ***commonly used*** with `a elements`. They ***can*** be ***used*** to ***indicate*** an `unvisited a element`, a `visited a element`, ***hovering*** over an `a element` ***with*** a `mouse` or ***using*** a `key pad`, and a `selected` (`active`) `a element`.

***Below***, we are ***going*** to ***change*** the `appearance` of our `a elements` ***with*** the `:hover pseudo selector`, which ***targets*** an `a element` ***when*** the` user` ***hovers over*** the `a element` ***with*** a `mouse` or `key pad`.

```css
a:hover {
    /* color: #2f6690; */
	/* changed to the below in my production styling of the a:hover pseudo-selector for the desktop navigation */
	color: #800080;
}
```

I, ***however***, did ***not like*** the  ***dark intensity*** of the `darker blue color` on `hover`, so I ***switched*** to `using` the `rgba() function`. We ***spoke about*** the `rgb() function` ***previously*** ***vs*** `hex color codes`.

***What***, ***however***, is the [rgba() function](https://www.w3schools.com/cssref/func_rgba.asp)?

The `rgba() function` ***defines*** `colors` by the `red-green-blue-alpha (RGBA)` ***model***. The (`a`) `alpha` is what ***permits*** the `designer` to ***control*** the `opacity` of a `color` ***using*** the `alpha channel` (the `a` in `rgba`), which ***specifies*** the ***level*** of `opacity` of a `color`. A `value` of `1` ***represents*** `100% opacity` of a `color`, `0` ***represents*** `0 opacity`, and ***makes*** the `color` ***transparent***. ***Anything*** `in between` ***represents*** `various levels` of `opacity` of a `color`.

`RGBA` ***color values*** are an ***extension*** of the `RGB` ***color values***. The `difference` ***between*** the ***two*** is the `alpha channel`.

```css
a:hover {
    color: #D6EFFF;
    background: rgba(47,102,144, 0.7);
}
```

***Ultimately***, I ***didn't*** `even use` the `background property` ***inside*** the `a:hover` ***rule set***. I went with ***only changing*** the `color` of the  `anchor element` ***text***, since I had ***decided*** to ***go with*** a ***transparent*** `navigation menu` ***background***.

I **ended up** `using` the ***following*** `CSS code` in the **production version** of my `portfolio site` on **Namecheap**:

```css
a:hover {
    /* color: #2f6690; */
	/* changed to the below in my production styling of the a:hover pseudo-selector for the desktop navigation */
	color: #800080;
}
```

</section>

---

<section class="section">
	<h2 class="sentence">Hiding the responsive hamburger menu in larger screens</h2>

***Next***, we **have** to ***make sure*** that our ***responsive*** `hamburger menu` is ***not displayed*** in ***larger screens*** (***greater than*** `> 899px`). We ***haven't*** `done anything` ***yet*** to ***make*** it ***display*** in the `browser`, but we might as well ***add*** the `CSS` ***now***, since it is ***desktop related*** `CSS`.

The ***following*** should be added ***below*** the `a:hover pseudo element rule set` ***inside*** `main.css`:

```css
a:hover {
    color: #2f6690;
}

.hamburger {
    display: none;
}
```

We had ***previously added*** the `.hamburger` ***class*** to the `button element` ***inside*** the `header element`.

We ***set*** the `value` of `none` to the `display property`. This ***means*** that on **screens** `> 899px`, the `hamburger menu` does ***not*** display ***at all***. This also ***implicitly means*** that the `hamburger menu` will ***not*** `take up space` in this ***hidden state***. If we ***had chosen*** to `use` the `visibility: hidden;` ***property declaration*** `instead`, the `hamburger menu` would ***not render*** on the ***page***, but it ***would*** `take up space` on the ***page***, so that ***other*** `elements` could ***not populate*** that ***space***. `display: none;` ***would*** `permit them` to ***do so***.

</section>

---

<section class="section">
	<h2 class="sentence">The @media rule for responsive navigation</h2>

***Next***, we **have** to **style** the `site navigation` for **screens** `less than < 900px` **wide**. In `desktop`, our `logo` and ***especially all*** our `navigation links` to ***all*** the **pages** on our `site` ***only*** `completely fit` on **wider screens** when the `width` of the `viewport` is ***at least*** `900px`. So to **style** our `site navigation` in **screens** `less than < 900px` **wide**, we **use** the ***following*** `@media rule`:

```css
@media (max-width: 899px) {

}
```

***Next*** we **have** to ***pick*** and ***choose*** what **has** to be `refactored` for the ***smaller screens***.

</section>

---

<section class="section">
	<h2 class="sentence">Refactoring the header element for smaller screens</h2>

In ***smaller screens***, I **had** to **move** the `logo` ***higher up*** the **page** (**closer** to the `top` of the `viewport`), so that ***meant*** I had to **decrease** the `margin-top` **property value** somewhat. I did the ***following***:

```css
.header {
    margin-top: 0.75rem;
}
```

</section>

---

<section class="section">
	<h2 class="sentence">Refactoring the ul element for smaller screens</h2>

We **have** to ***refactor*** the `ul element` for ***smaller screens***. We ***don't*** have to **touch** the `nav element`, because `100vw` can **also apply** to **smaller screens**. `100vw` is `100vw`!

To **make sure** that the `li elements` ***inside*** the `ul element` **stack** on **top** of **each other**, I ***do*** the ***following***:

```css
@media (max-width: 899px) {
	ul {
        /* display: block; */
        flex-direction: column;
        margin-top: 5rem;
    }
}
```

We **can make** the `li elements` **inside** the `ul element` ***stack*** one on **top** of the **other** in ***two ways***.

**One way** would be to **set** the `display: block;` **property declaration** on the `ul element selector`, ***transforming*** the `ul` from a `flex container` to a `block container`.

The ***other way*** would be to **change** the `flex direction`. In ***desktop*** `viewport widths`, we are **using** the ***default*** `flex direction` of `"row"`. **Within** our `media query` ***here***, we **could change** the **direction** to `"column"` with the **property declaration** of `flex-direction: column;`.

***Next***, I **set** the `margin-top: 5rem;` **property declaration** on the `ul element selector`. This ***moves all*** the `li elements` **down further away** from the `top` of the `viewport`. We ***do this*** because we **want** to **place** our `li elements` **below** the `responsive hamburger menu`. ***Otherwise***, it **would look** ***funny***!

</section>

---

<section class="section">
	<h2 class="sentence">Refactoring the li element for smaller screens</h2>

***Next***, I **needed** to `refactor` the `li element` in **screens** `smaller < than 900px`. I **did** the ***following***:

```css
li {
    margin: 0 0 0 1.25rem;
}
```

**Here**, I am **using** the `margin shorthand property`. I am **setting** the `margin-top`, `margin-right`, and `margin-bottom` **properties** to `0`. I am **setting** the `margin-left` **property** to `1.25rem`, because I ***don't want*** my `li elements` to be **butting up against** the `left side` of the `viewport`. I ***found*** that **setting** `margin-left` to `1.25rem;` was a ***good enough*** `distance` from the `left side` of the `viewport` to **make** the `li elements` ***look good*** and **separate from** the `viewport`'s **left side**.

</section>

---

<section class="section">
	<h2 class="sentence">Refactoring the anchor element for smaller screens</h2>

***Next***, I had to **make sure** that the `li elements` ***actually stacked*** on **top** of **each other**. Why do I say ***actually***? Because they **contain** `anchor elements` ***between*** their `opening` and `closing tags`.

I **did** the ***following***:

```css
a {
    display: block;
}
```

I **set** the `display: block;` **property declaration** on the `anchor element selector`.

</section>

---

<section class="section">
	<h2 class="sentence">Styling the responsive hamburger menu for smaller screens</h2>

***Most important*** for our `responsive navigation`, is to **style** the `responsive hamburger menu`! So I ***first*** did the ***following***:

```css
/* Responsive Hamburger menu styling */
.hamburger {
    background-color: transparent;
    /* show the hamburger menu image */
    background-image: url("https://ljc-dev.github.io/testing0/ham.svg");
    background-size: 100%;
    border: none;
    cursor: pointer;
    display: block;
    height: 36px;
    position: fixed;
    right: 20px;
    top: 20px;
    width: 36px;
    /* always keep ham on top of everything */
    z-index: 1000;
}
```

You ***may recall*** that we had **added** the `.hamburger` **class** to the `button element` which we had **placed under** the `anchor element` with the **class** of `"logo"` which ***defines*** our `text logo`. We ***also*** had added an `aria-label` **attribute** with the `value` of `"Right-Align"` for **accessibility purposes** (for `screen readers`).

***First*** I **set** the `property declaration` of `background-color: transparent;` on the `button element` with the **class** of `"hamburger"`. I ***had*** to **do this**, otherwise a `white background` would **appear behind** the `hamburger` **itself**. And I ***did not*** want that.

***Next***, I **set** the `background-size property` with the `value` of `100%` on  `.hamburger`. This **meant** that the `background` of the `hamburger menu` would **fill** `100%` of the `button element` **background**.

***Next***, I **set** the `border property` with the `value` of `"none"` so no **default border** would **appear** around the `hamburger menu` (`button element`).

***Next***, I **set** the `cursor property` with the `value` of `"pointer"` on the `hamburger menu`. This is to **provide** a ***better*** `user experience` and ***more*** `selection accuracy` when **clicking** on the `hamburger menu` to **expand** the `responsive navigation`.

***Next***, I **set** the `display property` with the `value` of `block` so that the `hamburger` ***fit properly*** within the `button element`, **removing** any `excess margins` or `padding` around it.

***Next***, I **set** the `height property` with the `value` of `36px` to the `hamburger menu`. **Here**, I ***did want*** to **set** a `fixed height` to the `hamburger menu`. I **did't want** it ***fluidly*** `shifting around` in **different** `screen sizes` along with the **shift** in the `viewport size`.

***Next***, I **set** the `position property` with the `value` of `fixed` on the `hamburger menu`. This is so that the `hamburger menu` would **remain** in the ***same place***, even if the `user` **scrolled down** the `browser window`.

***Next***, I **set** the `right property` with the `value` of `20px` on the `.hamburger` so that it is **moved** `20px` **away** from the **right side** of the `viewport`.

***Next***, I **set** the `top property` with the `value` of `20px` so that the `.hamburger` is **moved** `20px` **away** from the **top** of the `viewport`.

***Next***, I **set** the `width property` with the `value` of `"36px"` to the `hamburger menu`. I **wanted** the `hamburger menu` to ***basically*** be a `"square"`.

***Lastly***, I **needed** to **set** the `z-index property` with a `number value` on the `hamburger menu`. Because it does **contain** the `position` of `fixed`, I had to **make sure** that it was **in front** of ***all*** other `stacked elements` on the **page**. I **set** the `number value` of `1000`, ***which worked***!

</section>

---

<section class="section">
	<h2 class="sentence">Changing the hamburger menu to close</h2>

```css
/* change hamburger image to close */
.showClose {
    background-image: url("https://ljc-dev.github.io/testing0/ham-close.svg");
    background-size: 100%;
}
```

***Next***, I had to **set** the `background-image property` with the `value` of `url("https://ljc-dev.github.io/testing0/ham-close.svg")` on the `.showClose` class. ***This class***, however, ***does not*** exist by **default**. It is **created** with a **little help** from `JavaScript`. I **will explain** all about it when we ***add*** `functionality` to the `hamburger menu` with the **help** of `Javascript`. This will **take place** at the **end** of the `course`.

***Next***, I **set** the `background-size property` with the `value` of `100%` on the `.showClose` **class**, which is **added** to the `opening tag` of the `button element` as an ***added*** `value` of its `class attribute` along with the `.hamburger` **class** when the `user` **clicks** on the `hamburger menu`. A `background-size` of `100%` **means** that the `background image` **fills** `100% `of the `button`'s `background size` (`36px` x `36px`).

</section>

---

<section class="section">
	<h2 class="sentence">Opening the responsive navigation menu</h2>

***Next***, I **had** to ***add*** the **styling** for the `nav element` in **smaller screens** using the `nav element`'s `.navbar` **class**.

```css
.navbar {
    background: #6897BB;
    height: 100vh;
    left: 0;
    overflow: hidden;
    position: fixed;
    top: 0;
    /* hide the menu above the screen by default */
    transform: translateY(-100%);
    /* transition adds a little animation when sliding in and out the menu */
    transition: transform 0.2s ease;
    width: 100vw;
    z-index: 10;
}
```

***First***, I **set** the `background property` with the `value` of the `"#6897BB"` **color hex code** (a **shade** of `sailor's sea blue`) on the `nav element` using the `.navbar` **class**.  This is the `blue background` that **appears** when the `user` **clicks** on the `hamburger menu` to **open** the `responsive navigation menu`.

***Next***, I **set** the `height property` with the `value` of `100vh`. This is so that no matter **how high** the `viewport` is on **any device**, the `.navbar` **backdrop** will ***completely cover*** the `body` of the `page` ***behind it*** when the `responsive navigation` is **open**.

***Next***, I **set** the `left property` with the `value` of `0` so that there was **no gap** between the **left side** of the `viewport` and the `.navbar` **backdrop**.

***Next***, I **set** the `overflow property` with the `value` of `hidden` on the `.navbar` so that there is ***no overflow*** on either the `x` or `y axis`.

***Next***, I **set** the `position property` with the `value` of `fixed` on the `.navbar` so that when the `user` ***tries*** to **scroll down** the **page** when the `responsive navigation` is **open**, thereby **exposing** the **page** behind the `.navbar` **backdrop**, it ***won't happen***. The `scrollbar` is essentially **disabled**.

***Next***, I **set** the `top property` with the `value` of `fixed` on the `.navbar`. This is so that there is **no gap** between the **top** of the `viewport` and the **top** of the `.navbar`.

***Next***, I **set** the `transform property` with the `value` of `translateY(-100%)` to **hide** the `menu` by **default**.

***Next***, I **set** the `transition property` with the `value` of `transform 0.2s ease;`. This ***adds*** a little **animation** when **sliding in** and **out** the `menu`.

***Next***, I **set** the `width property` with the `value` of `100vw` on the `.navbar` so that the **whole width** of the `page` **underneath** the `menu` **backdrop** is **covered**.

***Lastly***, I **set** the `z-index property` with the `value` of `10` on the `.navbar`. I had to **play around** with the `value` until I ***finally found*** one that **places** the **backdrop** over everything else ***except**** the `responsive hamburger menu`.

</section>

---

<section class="section">
	<h2 class="sentence">Showing the responsive navigation menu</h2>

***Lastly***, I **had** to ***add*** the `styling` for the `.showNav` **class**. ***Again***, this **class** does ***not exist*** by **default**. It is **added** to the `.navbar` when the `user` **clicks** on the `hamburger menu`. When the `user` **clicks** on the `hamburger menu`, the `hamburger menu` is **transformed** into an `x`, and the `responsive navigation menu` **opens**. When the `responsive navigation menu` **opens**, the **class** of `.showMenu` is **added** to the `opening tag` of the `nav element`, where its `"default"` `.navbar` **class** also ***resides***.

When the `user` **clicks** on the `x` to **close** the `responsive navigation menu`, the `responsive navigation menu` **slides up** and ***disappears***, the `.showMenu` **class** is **removed** from the `opening nav tag`, and the `.showClose` **class** is **removed** from the `button element` with the `"default"` **class** of `"hamburger"`.

</section>

---

<section class="section">
	<h2 class="sentence">Adding the position of sticky to the header element in smaller screens</h2>

The ***one thing*** I **don't like** about **giving** the `hamburger menu` the `position` of `fixed` and **keeping** the `header element` **transparent** in **smaller screens**, is that it **looks like** the `hamburger menu` with the `transparent background` is **moving** with the `scroll` of the `page`. It ***isn't***, but it just `"looks"` that way to ***me***.

What we **can do** to ***fix this*** is to **add** the `position property` to the `header element` as well as a `background color`. We **can do** the ***following***:

```css
.header {
	background: pink;
	margin-top: 0.75rem;
	top: 0;
}
```

This then **means** we **have** to **move** the `h1 element` that is ***currently located*** at the **bottom** of the `header element` in the `portfolio.html` **page**. We **can do** the ***following***:

```html5
<header class="header">
	<a href="#"
	   class="logo">MDC</a>
	<button class="hamburger"
			aria-label="Right Align"></button>
	<nav class="navbar">
		<ul>
			<li>
				<a class="menu-link"
				   href="index.html">Home</a>
			</li>
			<li>
				<a class="menu-link"
				   href="portfolio.html">Portfolio</a>
			</li>
			<li>
				<a class="menu-link"
				   href="resume.html">Résumé</a>
			</li>
			<li>
				<a class="menu-link"
				   href="about.html">About</a>
			</li>
			<li>
				<a class="menu-link"
				   href="contact.html">Contact</a>
			</li>
		</ul>
	</nav>

</header>

<h1 class="main-heading">Birds!</h1>
```

This does ***not affect*** how my `CSS` **targets** the `h1 element` in the `external stylesheet`. It should also ***not affect*** the `HTML ranking` when I **test** my `markup` with the [W3C HTML Validation Service](https://validator.w3.org/).

<aside>
	Note: Go through the steps of changing the CSS for the header in my production portfolio site external stylesheet, and then upload it to Namecheap and show the changes. Then test the markup with the [W3C HTML Validation Service](https://validator.w3.org/).
</aside>

</section>

---

<section class="section">
    <h2 class="sentence">Related Resources</h2>

+ [Using HTML sections and outlines: MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_HTML_sections_and_outlines)

+ [How to create a responsive Navigation Bar with HTML, CSS and jQuery— step by step tutorial: ITNext](https://itnext.io/how-to-create-a-responsive-navigation-bar-with-html-css-and-jquery-step-by-step-tutorial-9c780b58479f)

+ [COMD2451 Sectioning HTML Documents, Adding external style sheets: Maria D. Campbell](https://github.com/interglobalmedia/sectioning-html/blob/master/sectioning-html.md)

+ [Reboot, Resets, and Reasoning: CSS Tricks](https://css-tricks.com/reboot-resets-reasoning/)

+ [Images and their backgrounds in HTML5, Relative vs Absolute Paths: Maria D. Campbell](https://github.com/interglobalmedia/image-backgrounds-rel-abs-paths/blob/master/image-backgrounds-rel-abs-paths.md)

+ [EM, PX, PT, CM, IN…: W3C](https://www.w3.org/Style/Examples/007/units.en.html)

+ [Basic concepts of Flexbox: MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)

+ [Rem in CSS: Understanding and Using rem Units: SitePoint](https://www.sitepoint.com/understanding-and-using-rem-units-in-css/)

+ [CSS :hover Selector](https://www.w3schools.com/cssref/sel_hover.asp)

+ [CSS Pseudo-classes](https://www.w3schools.com/css/css_pseudo_classes.asp)

+ [CSS rgba() Function: w3schools](https://www.w3schools.com/cssref/func_rgba.asp)

+ [cursor: CSS Tricks](https://css-tricks.com/almanac/properties/c/cursor/)

= [white-space: MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space)

</section>
