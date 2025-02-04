=== WP BugBot ===
Contributors: majick
Donate link: http://wordquest.org/donate/?plugin=wp-bugbot
Tags: plugin search, theme search, keyword search, core search, file search, editor, plugin editor, theme editor
Author URI: http://wpmedic.tech
Plugin URI: http://wpmedic.tech/wp-bugbot/
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Requires at least: 3.0.0
Tested up to: 5.2.2
Stable tag: trunk

Search your current plugin/theme/core files for keywords from admin. A 3rd party plugin bugfixers dream.

== Description ==

Broken plugin? Broken theme? Bizarre error messages? How to find the problem?
Track it down *fast* with WP BugBot, the Plugin and Theme Search Engine Editor.

** *"Every good set up deserves a PATSEE..!"* **

Lets you search your plugin and theme files for keywords from the editor screens! 
A 3rd party developer and bugfixers dream... find and squash those pesty bugs.

**NEW**:

* PHP Error Log AutoSearch and Viewer on Settings Page
* Directory navigation for the plugin and theme editor screens!
* Active and inactive plugins/themes are grouped in the selector
* You can now search (but not edit) Wordpress Core files too
* Works with Multisite (access from network/plugins.php etc.)

[WP BugBot Home](http://wpmedic.tech/wp-bugbot/)
[Support Forum](http://wordquest.org/support/wp-bugbot/)
[Contribute](http://wordquest.org/contribute/?plugin=wp-bugbot)


**Search**:

* Search for any keyword or phrase
* Search all, individual or multiple-select plugins!
* Search all active, inactive or update-available plugins
* Search all installed themes or a single themes files
* Search root, wp-includes or wp-admin files or subdirectories
* Case sensitive or insensitive matching

**Results**:

* Highlighted results for every occurrence
* Files and line numbers linked to file editor page
* Snipped but expandable long results lines

**Options**:

* Option to save last searched keyword/plugin/theme
* Add to the default Wordpress editable plugin file extensions
* Choose which file extensions not to search through

**Editor**:

* Adds directory navigation for plugin and theme files
* Shows Plugin/Theme files not editable/listed by Wordpress
* Javascript jump to line and find in code on editor screen

[WP BugBot Home](http://wordquest.org/plugins/wp-bugbot/)
[Support](http://wordquest.org/support/wp-bugbot/)
[Contribute](http://wordquest.org/contribute/?plugin=wp-bugbot)


== Installation ==

1. Upload `wp-bugbot.zip` via the Wordpress plugin installer.
2. Activate the plugin through the 'Plugins' menu in WordPress.
3. The search menus are added to the Plugin and Theme Editors.
4. Core search is available via the Updates page.


== Frequently Asked Questions ==

= Where is the search interface? =

When the plugin is activated, the search interfaces are available:
The Plugin search interface is at the top of the Plugins -> Editor page.
The Theme search interface is at the top of the Appearance -> Editor page.
The Wordpress Core search interface is at the top of the Dashboard -> Updates page.
The PHP Error Log Viewer at the bottom of the WP BugBot admin page.


= Where are the plugin settings? =

There are some minimal options for this plugin so they are available after searching.
After performing a search (see above) the WP BugBot sidebar will appear on the right.
Click on Plugin Options at the top of the search sidebar to change available options.


= How can I edit files with unsupported extensions? =

By default Wordpress limits the editable extensions for files in the inbuilt editor.
If you want to change which files extensions you can edit you can do so this way:

Perform a search from an editor page and the WP BugBot plugin sidebar will appear.
Click on Plugin Options and you will see a list of editable extensions.
Add the extensions (comma separated) that you want to the list and click Save.
Files with these extensions should now be editable with the Wordpress internal editor.


= How can I change what is not searched? =

By default WP BugBot will not search through most common media file extensions:
zip, jpg, gif, png, bmp, svg, psd, mp3, wma, m4a, wmv, mpg, mkv, avi, mp4, flv, swf
If there are other file extensions you want to ignore, you can add them this way:

Perform a search from an editor page and the WP BugBot plugin sidebar will appear.
Click on Plugin Options and you will see a list of editable extensions.
Add the file extensions (comma separated) here to not search, and click Save.


= How can I speed up the search? =

If your search is taking too long or timing out, generally it is because you are
searching through too many plugins at once (eg. ALL) so you might need to narrow
your search by using the multi-select option and searching through half or a third
of your plugins at once. Also, you might want to check you server's maximum execution
time limit for scripts and increase that if it is too low.


= Can I use the plugin with file editing disabled? =

Yes, if you have defined DISALLOW_FILE_EDIT as true in your wp-config.php to remove
the plugin and theme editing interfaces, you can still use the plugin and theme search.
BugBot will detect this is the case and move all interfaces to the core Updates page.


= The scroll to line feature is not working properly for me? = 

This original feature was thanks to Andrew Buckman's Wordpress Editor Search:
http://www.theoneandtheonly.com/wordpress-editor-search/
This should still work fine for legacy installations (pre WP 4.9), however as the code
editor has been replaced by Code Mirror from WP 4.9 onwards, a new solution will need
to be implemented for this in a future version.


= How do I filter the PHP error log files searched for? = 

WP BugBot will attempt to automatically detect the setting for your PHP error log files.
If you have a more complex setup or wish to change the filenames that are searched for,
you can use the filter 'bugbot_error_log_search' to return an array of error log filenames.
If you wish to turn this feature off (it is run on the WP BugBot admin screen only)
simply use this same filter and return an empty array.


== Screenshots ==

1. Plugin Search Interface
2. Plugin MultiSearch Interface
3. Theme Search Interface
4. Core Search Interface
5. Example Search Result Display


== Changelog ==

= 1.8.1 =
* Updated to Plugin Loader 1.0.7
* Updated to WordQuest Helper 1.7.5
* Updated to Freemius SDK 2.3.0

= 1.8.0 =
* Updated to use new Plugin Loader class
* Updated to WordQuest Helper 1.7.4
* Updated to Freemius SDK 2.2.2
* Fix for undefined firstblock variable

= 1.7.9 = 
* Updated to use global settings array
* Removed replace Theme Editor default (no longer needed)
* Filter manage plugin settings capability
* Fix editable theme and plugin extensions
* Added settings reset button and processing
* Fixes for warnings and undefined variables
* Use generic page elements for editor toolbar

= 1.7.5 =
* Update to Freemius SDK to 1.2.2.9
* Update to Wordquest Helper 1.6.9
* Improved plugin option for filtering
* Fix to theme object for search

= 1.7.4 =
* Fix to last searched saving logic
* Fix to settings page link for DISALLOW_FILE_EDIT
* Fix to permission checks for DISALLOW_FILE_EDIT
* Fix to javascript checks on update-core.php page

= 1.7.3 = 
* Added error log search filename filter
* Extend error search for subdirectory installs

= 1.7.2 =
* Update to WordQuest Library 1.6.6
* Fix error log links to file content displays
* Use WP Filesystem writing for theme editor

= 1.7.1 =
* Update to Freemius Library 1.2.1.5
* Added input for error log lines to process
* Check theme editor and write method before using
* Allow for searching with DISALLOW_FILE_EDIT true

= 1.7.0 =
* Added error log searches and display
* Use single global plugin options array
* Added Settings saving validation
* Update to Wordquest Library 1.6.5
* Added Search Time Limit option
* Fix to theme editor loading
* Added translation ready wrappers

= 1.6.0 =
* Transition to WordQuest release
* Added Freemius Features
* Added Standalone Settings Page
* Group/Mark Parent Theme in Theme Select Box
* Single Icon Display Fix for search pages
* Fixed Plugin Directory Selection on Filepage

= 1.5.0 =
* Added directory selection for plugin files
* Added all active/inactive plugin search
* Added update available plugin search
* Added some styling to select boxes
* Added more core path options to core search
* Added * to mark update available plugins
* Added time limit adjustment for searches
* Added modified copy of theme-editor.php 
* - to allow changing of editable extensions
* - also to allow theme directory selection
* Added magnifying glass icon to search bar
* Grouped active/inactive plugins in select
* Grouped current/inactive themes in select
* Improved Styling on search display screen
* Fix for repeat multiple plugin searches
* Fix to view unlisted plugin file
* Fix to show plugin unlisted files
* Fix to subsubdirectory recursion listing

= 1.4.5 =
* Fix to Default Editable Extensions (again)
* Fix to Plugin File Editor Links

= 1.4.0 = 
* Added Multisite support
* Added Wordpress Core file search
* Added unlisted files display
* Fixed adding of editable extensions
* Fixed parent/child theme selection bug
* Minor display bugfixes

= 1.3.0 =
* Public release version.

= 1.2.0 =
* Pre release version.

= 1.1.0 =
* Unreleased version.

= 1.0.0 =
* Development version.


== Other Notes ==

[WP BugBot Home](http://wpmedic.tech/wp-bugbot/)

Like this plugin? Check out more of our free plugins here: 
[WP Medic Tools](http://wpmedic.tech/ "WP Medic Tools")
[WordQuest Plugins](http://wordquest.org/plugins/ "WordQuest Plugins")

Looking for an awesome theme? Check out my child theme framework:
[BioShip Child Theme Framework](http://bioship.space "BioShip Child Theme Framework")

= Support =
For support or if you have an idea to improve this plugin:
[WP BugBot Support Quests](http://wordquest.org/support/wp-bugbot/ "WP BugBot Support")

= Contribute = 
Help support improvements and log priority feature requests by a gift of appreciation:
[Contribute to WP BugBot](http://wordquest.org/contribute/?plugin=wp-bugbot)

= Development =
To aid directly in development, please fork on Github and do a pull request:
[WP BugBot on Github](http://github.com/majick777/wp-bugbot/)

= Limitations = 
* 'Scroll to Line' and 'Search in Code' features not working with Code Mirror.

= Planned Updates/Features =
* Integration of Debug Bar Features with linked search ability
* A custom directory search option for any user defined directory
* CSS/JS Resource to Plugin/Theme matching list via Custom Search
* Scroll-to-line integrations with other source code editor plugins?
* Improve Quick File Viewer Interface (allow saving?)