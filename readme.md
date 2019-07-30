<!-- DO NOT EDIT THIS FILE; it is auto-generated from readme.txt -->
# Syntax-highlighting Code Block (with Server-side Rendering)

Extending the Code block with syntax highlighting rendered on the server, thus being AMP-compatible and having faster frontend performance.

**Contributors:** [westonruter](https://profiles.wordpress.org/westonruter), [mkaz](https://profiles.wordpress.org/mkaz)  
**Tags:** [block](https://wordpress.org/plugins/tags/block), [code](https://wordpress.org/plugins/tags/code), [code syntax](https://wordpress.org/plugins/tags/code-syntax), [syntax highlight](https://wordpress.org/plugins/tags/syntax-highlight), [code highlighting](https://wordpress.org/plugins/tags/code-highlighting)  
**Requires at least:** 5.0  
**Tested up to:** 5.2  
**Stable tag:** 1.0.0  
**License:** [GPLv2 or later](http://www.gnu.org/licenses/gpl-2.0.html)  
**Requires PHP:** 5.6  

[![Built with Grunt](https://gruntjs.com/cdn/builtwith.svg)](http://gruntjs.com) 

## Description ##

This plugin extends to Code block in WordPress core to add syntax highlighting which is rendered on the server. By performing the syntax highlighting on the server, there is then no need to enqueue any JavaScript on the frontend (e.g. Highlight.js or Prism.js) and this ensures there is no flash of unhighlighted code (FOUC?). Reducing script on the frontend improves frontend performance and it also allows for the syntax highlighted code to appear properly in AMP pages as rendered by the [official AMP plugin](https://amp-wp.org) (see also [ampproject/amp-wp#972](https://github.com/ampproject/amp-wp/issues/972)).

The extended Code block uses auto-detection for the language in the block to add syntax highlighting, but you can override the language in the block inspector. There is currently no syntax highlighting of the block in the editor. On the frontend, server-side rendering is performed by [highlight.php](https://github.com/scrivo/highlight.php) which is a port of [highlight.js](https://highlightjs.org/), allowing you to use all [89 styles](https://highlightjs.org/static/demo/). To override the `default` style, use the `syntax_highlighting_code_block_style` to supply the one of the [style names](https://github.com/scrivo/highlight.php/tree/master/styles), for example `github`:

<pre lang=php>
add_filter(
	'syntax_highlighting_code_block_style',
	function() {
		return 'github';
	}
);
</pre>

This plugin is [developed on GitHub](https://github.com/westonruter/syntax-highlighting-code-block). See [list of current issues](https://github.com/westonruter/syntax-highlighting-code-block/issues) with the plugin. Please feel free to file any additional issues or requests that you may come across. [Pull requests](https://github.com/westonruter/syntax-highlighting-code-block/pulls) are welcome to help extend.

This is a fork of [Code Syntax Block](https://github.com/mkaz/code-syntax-block) by [Marcus Kazmierczak](https://mkaz.blog/) (mkaz), which is also [available on WordPress.org](https://wordpress.org/plugins/code-syntax-block/).

[highlight.php](https://github.com/scrivo/highlight.php) is released under the BSD 3-Clause License.
Copyright © 2006-2013, Ivan Sagalaev (maniac@softwaremaniacs.org), highlight.js (original author).
Copyright © 2013, Geert Bergman (geert@scrivo.nl), highlight.php

## Changelog ##

For the plugin’s changelog, please see [the Releases page on GitHub](https://github.com/westonruter/syntax-highlighting-code-block/releases).

