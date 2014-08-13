# tinyProgressbar
tinyProgressbar is an extremely tiny (640 bytes minified+gzipped) Javascript progressbar library.

It renders nice, flat progressbars fully customizable with CSS. It can display absolute values (eg: 25/300) or percentages (eg: 5%) on a progressbar. It also animates progression using CSS transitions.

Kailash Nadh, October 2014

License:	MIT License
Documentation and Demo: http://nadh.in/code/tinyprogressbar

## Usage

##### Include scripts in the &lt;head&gt;
<pre>
&lt;link rel=&quot;stylesheet&quot; type=&quot;text/css&quot; href=&quot;path/tinyprogressbar.css&quot;/&gt;
&lt;script type=&quot;text/javascript&quot; src=&quot;path/tinyprogressbar.js&quot;&gt;&lt;/script&gt;
</pre>

#####  Add the container to be rendered as the progress bar
<pre>
 &lt;p id=&quot;progress&quot; data-min=&quot;0&quot; data-max=&quot;200&quot; data-mode=&quot;absolute&quot;&gt; &lt;/p&gt;
 
 // OR -> data attributes are optional. They can be manipulated with Javascript
  &lt;p id=&quot;progress&quot;&gt; &lt;/p&gt;
</pre>
##### Initialize and use
<pre>
&lt;script&gt;
	// initialize
	var bar = new tinyProgressbar(document.getElementById(&quot;progress&quot;));

	// set min and max values from javascript (or use data attribute in the HTML)
	bar.setMinMax(0, 100);

	// set the mode (absolute = absolute numbers, percentage = percentage value %)
	// or use data-mode to set it in HTML
	bar.setMode("percentage");

	// that's it! move the bar
	bar.progress(30);

&lt;/script&gt;
</pre>