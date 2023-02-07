# svgToJson
This is a simple tool written in html an js to convert a svg image to json.
To achieve this, this tool uses [svgson](https://github.com/elrumordelaluz/svgson#readme).

# Usage
Download everything and start 'convert.htm'.

# Developer notes
To use a npm package in html you have to
<ol>
  <li> Initialize npm in the directory: <code>npm init -y</code>
  </li>
  <li> Install browserify: <code>npm install browserify --save</code>
  </li>
  <li> Install the npm package that you want to use. This tool uses (as said) svgson. Therefore: <code>npm install svgson --save</code>
  </li>
  <li> Create the file 'index.js' and add the exported module (package) to it. So the index.js looks like this:
  <pre>const svgson = require('svgson');
module.exports=svgson</pre>
  </li>
  <li> Output the module exported to a js file that you can use in the html. To do this run <code>node_modules/.bin/browserify index.js -s <name of module> > <name of output JavaScript file></code>. For this tool the command looks like this:
  <pre>node_modules/.bin/browserify index.js -s svgson > svgson.js</pre>
  </li>
  <li> Include the created js file in your html. For example: <code><script type="text/javascript" src="svgson.js"></script></code>
  </li>
</ol>
