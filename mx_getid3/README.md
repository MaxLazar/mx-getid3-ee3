# MX ZIP#

**MX Zip** adds you capability to add files/folders into zipping archive directly from ExpressionEngine 3;

## Installation
* Download the latest version of MX Zip and extract the .zip to your desktop.
* Copy *zip* to */system/user/addons/*

## Configuration
Once the Plugin is installed, you should be able to see it listed in the Add-On Manager in your ExpressionEngine Control Panel. Is no needs in any control panel activation or configuration.

## Template Tags
{exp:zip}

	{exp:zip direct_output="no" folder="images" filename="min.zip" max_size="1024" comment="Made in ExpressionEngine" remove_path="" add_path=""}
	    {zip:files}
	        [themes/cp_global_images/watermark_test.jpg]
	        [themes/cp_global_images/ee_logo.jpg]
	        [themes/profile_themes/]
	        [themes/cp_themes/classic/classic.css]
	    {/zip:files}
	
	{/exp:zip} 

### Parameters

*folder*

folder whare you want to save your zip files in direct_output = false mode

*filename*

zip fillename. By default the filename is unix_timestamp.zip

*remove_path* optional

This parameter gives the ability to suppress a part or all the path of the files (or directories) when they are extracted or archived.

*add_path* optional

This parameter gives the ability to insert a path while files are extracted or archived.

*comment* optional

This parameter gives the ability to set a comment in the ZIP archive.

*remove_all_path* optional

This parameter gives the ability to suppress all the path of the file when extracting it or adding it in the archive.

*return_name_only* optional

This parameter gives ability to return archive name only

*max_size* optional 

*overwrite* optional

overwrite file or not

*direct_output* optional

	direct_output="no" 

the plugin can sent direct to user or can save package file on the web server

*speed* optional

	speed="500" 
	
Download speed in kb

### Conditional variables:
	{if file_limit}
	
	{/if}

You may use this conditional for displaying a message in the case when size of your files preparing for package more then max_size


### Variable pairs

	{zip:files}
		[file_or_folder_path,folder_structure4zip]
	{/zip:files}
	
A comma separated list of files/folders for packing

      file_or_folder_path - file or folder which you want to zip with full or relative server path.

      folder_structure4zip (optional) - individual folder path for file in the zip archive.

## Support Policy
This is Communite Edition (CE) add-on.

## Contributing To MX Zip for ExpressionEngine 3

Your participation to MX ZIP development is very welcome!

You may participate in the following ways:

* [Report issues](https://github.com/MaxLazar/mx-zip-ee3/issues)
* Fix issues, develop features, write/polish documentation
Before you start, please adopt an existing issue (labelled with "ready for adoption") or start a new one to avoid duplicated efforts.
Please submit a merge request after you finish development.


### License

The MX Zip is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)