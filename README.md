visualjournalist.github.io
==========================

An experiment in using Jekyll with Github pages to host a simple portfolio site.

This is a quick demo to show how Jekyll can be used to bake out static HTML for the circumvention project. The comic book templates are stored in the '_includes' folder. The JSON of the translations for the comics (and metadata) is stored in the '_data' folder in individual .json files (e.g. 'dns.json'). Each language has its own folder (e.g. '/russian/') with a '/_posts/' folder. By keeping the markdown files for the translations in those folders the site will preserve the site structure. Each translation .md file has an include at the topic for the appropriate comic and passes in the language number: '{% include comic__dns.html langnumber=5 %}'

###Directory structure of Jekyll sites using gem-based themes
Starting Jekyll 3.2, a new Jekyll project bootstrapped with jekyll new uses gem-based themes to define the look of the site. This results in a lighter default directory structure : _layouts, _includes and _sass are stored in the theme-gem, by default.

minima is the current default theme. 
Type: 
'$ bundle show minima'

To see  where minima theme's files are stored on your computer.

Type:

'$ open .'

To open that folder in the current terminal window in finder.

If you read the README file for the theme, it gives instructions on ways to override the theme SASS at the project level

	### Customization

	To override the default structure and style of minima, simply create the concerned directory at the root of your site, copy the file you wish to customize to that directory, and then edit the file.
	e.g., to override the [`_includes/head.html `](_includes/head.html) file to specify a custom style path, create an `_includes` directory, copy `_includes/head.html` from minima gem folder to `<yoursite>/_includes` and start editing that file.

	The site's default CSS has now moved to a new place within the gem itself, [`assets/main.scss`](assets/main.scss). To **override the default CSS**, the file has to exist at your site source. Do either of the following:
	A. Create a new instance of `main.scss` at site source.
	  - Create a new file `main.scss` at `<your-site>/assets/`
	  - Add the frontmatter dashes, and
	  - Add `@import "minima";`, to `<your-site>/assets/main.scss`
	  - Add your custom CSS.
	B. Download the file from this repo
	  - Create  a new file `main.scss` at `<your-site>/assets/`
	  - Copy the contents at [assets/main.scss](assets/main.scss) onto the `main.scss` you just created, and edit away!
	or C. Copy directly from Minima 2.0 gem
	  - Go to your local minima gem installation directory ( run `bundle show minima` to get the path to it ).
	  - Copy the `assets/` folder from there into the root of `<your-site>`
	  - Change whatever values you want, inside `<your-site>/assets/main.scss`




