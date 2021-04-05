## Install requirements

`npm install -D @tailwindcss/jit tailwindcss postcss autoprefixer`


## Generating developer Tailwindcss build:

While editting styles keep running

`npm run build`

This will interactively produce all classes used in code.


## Generate production Tailwindcss build:

	cat tailwind.css custom.css > tailwind.temp.css
	npx tailwindcss build tailwind.temp.css -c tailwind.config.prod.js | npx clean-css-cli > build.css

This will produce classes only used in code (files are specified in `./tailwind.config.prod.js`) and minify the resulting css.
