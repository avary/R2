R2
---
R2 helps you achieve cross-language layout-friendly websites (including bi-directional text). It looks like this:

``` css
/* before */
#content {
  float: left;
  margin-right: 2px;
  padding: 1px 2px 3px 4px;
  left: 5px;
}
.info {
  text-align: right;
}

/* after */
#content {
  float: right;
  margin-left: 2px;
  padding: 1px 4px 3px 2px;
  right: 5px;
}
.info {
  text-align: left;
}
```

Install it
----------

    $ [sudo] npm install R2 -g

Use it as a CLI

    $ r2 input.css output.css

Or require it as a Node module

``` js
var output = require('r2').swap(css)
```

Caution
--------
R2 will only work as good as what you give it, therefore *inline-styles* embedded in your HTML will not converted, and therefore may cause unexpected results. However inline-styles apart from R2 is still a bad idea, and you should avoid it anyway in favor of separating content from presentation.

**Happy layout Swapping!**