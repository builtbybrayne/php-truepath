php-truepath
============

Replace PHP's extremely buggy realpath()

## Usage

### Installation

##### Via Composer

Truepath is available on Packagist ([perchten/truepath](https://packagist.org/packages/perchten/truepath)) and as such is installable via [Composer](https://getcomposer.org/).

Add the following to your `composer.json`

	{
    	"require": {s
        	"perchten/truepath": "1.*"
	    }
	}

##### Direct include

Clone or download from [GitHub](https://github.com/perchten/php-truepath) and include directly in your code:

	require_once "path/to/truepath/truepath.php"


### Code

It's just one simple function, and as such it is not namespaced, but loaded as a globally available function. So just use:

	$truepath = truepath("some/possible/path")
	
Unlike PHP's realpath, this function does not return false on error; it returns a path which is as far as it could to resolving these quirks.

This does not work on network resources including UNC and URLs. It works for the local file system only.


## Acknowledgements

All credit goes to [Christian](http://stackoverflow.com/users/314056/christian) from [this StackOverflow question](http://stackoverflow.com/questions/4049856/replace-phps-realpath). I'm just putting this up on some repos for easier access.

