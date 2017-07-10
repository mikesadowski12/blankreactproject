How to initialize (make sure to download node):
	1. 'npm init' in project root directory
	2. 'npm install --save webpack'
	3. 'npm install --save babel-core babel-loader babel-preset-es2015 babel-preset-react es6-promise react react-dom'

	4. 'webpack.config.js' contains:
		var path = require('path');
		var webpack = require('webpack');

		module.exports = {
		 entry: './js/app.js',
		 output: {
		  path: __dirname,
		  filename: 'js/bundle.js'
		 },
		 watch: true,
		 module: {
		  loaders: [
		   {
		    test: /.jsx?$/,
		    loader: 'babel-loader',
		    exclude: /node_modules/,
		    query: {
		     presets: ['es2015', 'react']
		    }
		   }
		  ]
		 },
		};﻿

	5. change 'package.json' to contain:
		  "scripts": {
		    "babel": "babel",
		    "webpack": "webpack",
		    "test": "echo \"Error: no test specified\" && exit 1"
		  },

	6. '.babelrc' contains:
		{
		    "presets": ["react"]
		}

	7. 'npm run webpack'

Install babel:
	npm install --global babel-cli
	npm install --save-dev babel-plugin-transform-es2015-arrow-functions
	npm install --save-dev babel-plugin-check-es2015-constants
 	npm install --save-dev babel-plugin-transform-es2015-block-scoping
 	npm install --save-dev babel-preset-es2015
 	npm install --save-dev babel-preset-env
 	npm install --save-dev babel-preset-react
 	npm install --save-dev babel-preset-stage-2