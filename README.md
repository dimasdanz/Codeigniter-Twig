# Codeigniter-Twig

Simple Twig Templating Engine implementation on Codeigniter 3.0 via Composer

## Installation
1. **Add & Install Twig via Composer**  
  Yes, you can use composer on Codeigniter 3.0 out of the box. Just open composer.json and add  

  ```
  "config": {
      "vendor-dir": "application/vendor"
  },
  "require": {
  		"twig/twig": "~1.0"
  } 
  ```
  and run composer update (or install if you haven't already)  
  *application/vendor is Codeigniter default location for vendor  

1. **Enable Codeigniter composer_autoload**
  Open config.php on application/config (or wherever you have it set) and set 
  ```
  $config['composer_autoload`] = TRUE;
  ```

1. **Copy Files & Directories**  
	Copy the contents of the application folder to your own application folder.  
	If you already configured autoload.php, you might don't want to copy it directly as it will overwrite your configuration.  
	Just add Twig on libraries autoload and twig on config autoload.  
	```
	$autoload['libraries'] = array('Twig');
	$autoload['config'] = array('twig');
	```
	And also if you have MY_Loader (or with any prefixes), you might just wanna modify it.  
	
1. **Check Config Settings**  
	The default settings work out of the box.  
	But if you wanna change it, check the twig.php config file  
	
1. **Add Write Permissions to Cache Directory**  
	Make sure application/cache has permission to write if you enable cache (e.g CHMOD 777).

## Usage
Loading the view still the same as the original Codeigniter **load->view('view_file', $data)**   
So caching, output modification, etc will still works  
Now you can use every Twig syntax on your view files

## What is Twig
[Twig](http://twig.sensiolabs.org/) is PHP Template Engine. Or The flexible, fast, and secure template engine for PHP (as how their website state it)  
Template Engine provides a cleaner syntax and additional features for your view files  
For information about Twig and how to use it, please visit [Twig's Documentation](http://twig.sensiolabs.org/documentation)

## License

#### DON'T BE A DICK PUBLIC LICENSE

> Version 1, December 2009

> Copyright (C) 2009 Philip Sturgeon <me@philsturgeon.uk>
 
 Everyone is permitted to copy and distribute verbatim or modified
 copies of this license document, and changing it is allowed as long
 as the name is changed.

> DON'T BE A DICK PUBLIC LICENSE
> TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

 1. Do whatever you like with the original work, just don't be a dick.

     Being a dick includes - but is not limited to - the following instances:

	 1a. Outright copyright infringement - Don't just copy this and change the name.  
	 1b. Selling the unmodified original with no work done what-so-ever, that's REALLY being a dick.  
	 1c. Modifying the original work to contain hidden harmful content. That would make you a PROPER dick.  

 2. If you become rich through modifications, related works/services, or supporting the original work,
 share the love. Only a dick would make loads off this work and not buy the original work's 
 creator(s) a pint.
 
 3. Code is provided with no warranty. Using somebody else's code and bitching when it goes wrong makes 
 you a DONKEY dick. Fix the problem yourself. A non-dick would submit the fix back.

## Change Log

#### 1.0.0 - May 23, 2015
Initial release.

## Credit
 1. [Codeigniter 3.0.0] (http://www.codeigniter.com)
 1. [Twig PHP Template Engine] (http://twig.sensiolabs.org/)
 1. [Codeigniter_Smarty] (https://github.com/cryode/CodeIgniter_Smarty)
 1. [Codeigniter-Twiggy] (https://github.com/edmundask/codeigniter-twiggy)
 1. If you think your name should be here, feel free to contact me
 
###Contact:
 + [Facebook](http://www.facebook.com/Dimasdanz)
 + [Twitter](http://www.twitter.com/Dimasdanz)
 + [LinkedIn](https://id.linkedin.com/in/dimasdanz)
 + dimasdanz@gmail.com
