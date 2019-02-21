## Some common questions
There are questions I keep receiving via email, GitHub or in person at conferences.  
I tried to address some of them here.

### Is Codeception/wp-browser PHP 5.2 compatible?
No, Codeception, and wp-browser by extension, will require PHP 5.6 minimum.  
This does **not** mean your code cannot be PHP 5.2 compatible: you can test your code using all the possibilities of newer PHP versions and still keep it PHP 5.2 compatible.  
Just because you can doesn't mean you should though: this documentation will assume a minimum PHP version, for the example and test code, of PHP 5.6.

### Can I run unit tests with wp-browser/Codeception?
Yes, with some distinctions.  
In the WordPress echosystem there's a tendency to call **any** kind of test a "unit test". Under that definition will fall tests that are not "unit" tests at all.  
Without drowning into a long and painful battle for definitions this guide will use the following definitions for different levels of testing.  
The [next section](levels-of-testing.md) will detail the conventions this documentation uses to define different levels of testing in more detail.

### Isn't WordPress untestable?
No; it's sometimes **difficult** to test and not as straightforward as other PHP frameworks but it's definitely not untestable.  
**You** are writing code that **runs** on WordPress, not the Core code for WordPress so the question should really be: will **you** write testable code?  
It's up to **you** to decide at what level you want to make your code testable and how much you want to test it.

### Do I need to use a specific local development environment to use wp-browser?
No. I've started using wp-browser on a vanilla PHP built-in server to, then, move to [MAMP](https://www.mamp.info/en/) (or [XAMP](https://www.apachefriends.org/download.html)) and, from there, to other solutions.  
I've configured and used wp-browser on Docker, Vagrant, [VVV](https://github.com/Varying-Vagrant-Vagrants/VVV), [Valet](https://laravel.com/docs/5.7/valet) and various CI solutions.  
To this day I keep using different setups on different machines and personally prefer [Docker](https://www.docker.com/) for its portability.

### Can I only test plugins with wp-browser?
No, you can test any kind of WordPress application.  
With "application" I mean any PHP software built on top of WordPress: plugins, themes, whole sites.

### If I'm testing a site do I have to use the default WordPress file structure?
No, you can use any file structure you want.  
Some wp-browser modules will need a little help to find your code but, so far, I've never been unable to set it up.

### Can I use wp-browser even if my WordPress application doesn't use Composer?
Yes, although wp-browser, as a development tool, cannot be installed without [Composer](https://getcomposer.org/).

### Should I use wp-browser to test my production servers?
No. Unless you know very well what you're doing that's a dangerous idea that might leave you with a broken site and an empty database.  
As almost any testing tool wp-browser should be used locally on local installations of WordPress that do not contain any valuable information.