# autoInstaller for Webspell
Version 1.2

- [Intro](#what-is-this)
- [Requirements](#requirements)
- [Usage](#usage)
- [Screenshots](#screenshots)

## What is this?
---------------------------------------
The autoInstaller is a script for addon / mod creator who want to have your scripts installed easily.
You can use the autoInstaller to check files for their existence, manipulate files or insert sql commands



## Requirements
---------------------------------------
Supports all webspell.org versions

## Usage
---------------------------------------
##### Check the files if exist
If you want to check they exsist admincenter.php
```php
$find_file[] = 'admin/admincenter.php';
```

The script looking for the absolute path in webspell.

##### Manipulate files
You can use the auto installer to insert simple code into files to certain positions.
```php
$files[] = 
	array('filename' => 'admin/languages/uk/admincenter.php', 
		  'find'   =>   '\'settings\'=>\'Settings\',', 
          'add'  => 	'	\'addonname\'=>\'Addonname\',');
```
In this example you will see, the script open the file admincenter.php and looking for *'settings'=>'Settings',*.
After that the script add a new line and insert: *'addonname'=>'Addonname',* here.

###### Important Informations!
- Unmask apostrophes 
(Correct:  ```\'```  --  False: ```'``` )
- Insert the complete line for the find parameter 
(Correct:  ```\'settings\'=>\'Settings\',```  --  False: ```\'settings\'=``` )

##### Insert/Update MySQL
You can simply paste the mysql commands
```php
$mysql[] = "INSERT INTO `".PREFIX."table` (`row1`, `row2`, `ro3`, `row4`) VALUES ('', 'value2', 3, 'value4')";
```

## Screenshots
---------------------------------------
Opening

![autoInstaller Opening](http://www.atworkz.de/_git/installer/opening.jpg)

Step 1

![autoInstaller Step 1](http://www.atworkz.de/_git/installer/step1.jpg)

Step 2

![autoInstaller Step 2](http://www.atworkz.de/_git/installer/step2.jpg)


