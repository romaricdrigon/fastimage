# FastImage

FastImage finds the dimensions or filetype of a remote image file given its uri by fetching as little as needed, based on the excellent [Ruby implementation by Stephen Sykes](https://github.com/sdsykes/fastimage).

This version was forked from [Tom Moor PHP port](https://github.com/tommoor/fastimage), and introduced a few changes:

 * usage of exceptions
 * ability to customize HTTP headers
 * composer-ready

## Usage
```php
<?php 
		
require 'Fastimage.php';
		
$uri = "http://farm9.staticflickr.com/8151/7357346052_54b8944f23_b.jpg";
		
// loading by creating an instance and use the 'load' method
$image = new FastImage();
$image->load($uri);
$type = $image->getType();
echo "filetype: " . $type;
```

## References

* https://github.com/sdsykes/fastimage
* http://pennysmalls.com/find-jpeg-dimensions-fast-in-pure-ruby-no-ima
* http://snippets.dzone.com/posts/show/805
* http://www.anttikupila.com/flash/getting-jpg-dimensions-with-as3-without-loading-the-entire-file/
* http://imagesize.rubyforge.org/


## License

FastImage is released under the MIT license. It is simple and easy to understand and places almost no restrictions on what you can do with the software. [More Information](http://en.wikipedia.org/wiki/MIT_License)

