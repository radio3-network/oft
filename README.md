This is an off-grid app for Android devices.

The main goal is to turn any normal android phone into an offline library that works without internet.


Basic requirements:
+ open source, licensed as Apache-2.0
+ written in Java
+ hosted on github (repository to be provided)


Features:
+ search box to find files on local storage
++ plugin structure to add data to be found
++ needs to accept similar searches, not just exact
++ use already existing libraries for search
+ uses plugins to parse text data from different files
++ for example PDF, music, films, etc

-----------------------------
Description of main screens
-----------------------------

[frontpage]
The frontpage contains a search box.
When the user types a search item, it will show results
+ when the search takes longer than a few seconds, show progress of search
+ has an history tab, allow to show previous searches (cached results)
+ can put specific searches as favorite
+ can filter searches according to type (e.g. music, documents, images)
+ can search files according to attributes (e.g. date interval, file size, ...)
+ clicking on a search result opens that file with the default app
+ show basic statistics on main page
++ number of files indexed
++ overall disk space that is covered
++ amount of free disk space left
+ show most clicked items
+ show basic categories
++ films, music, PDF/ebooks, libraries
++ permit to search inside specific category



[settings]
+ list of search folders
+ list of folders specifically to ignore
+ set how often to update the search database
+ language change
+ install plugins
++ gets list of common plugins that can be installed
++ permit to add URL for new plugins (e.g. on github)
++ show plugins that can be upgrades
++ button for upgrading all plugins at once
++ uninstall/disable plugin
+ change theme
+ add/remove/edit libraries



[libraries]
+ create a library, basically a collection of items
+ JSON file to keep settings for this library
+ permits to import/export libraries from URL
++ can get a list of recommended libraries from the app github repo
+ permit to add specific tags to folders
++ tags can use any text sequence
++ including other languages
+ libraries can be shared through IPFS
++ create a zip file, share on IPFS
++ user phones become servers on IPFS



-----------------------------
Functionality
-----------------------------

[search]
+ use library like Lucene for Android
+ e.g.: https://github.com/shashavali-d/android-lucene
+ permits complex search types
++ very fast search results over large data
++ database needs to be recreated every now and then


[tags]
+ permit to add specific tags to files/folders
+ each folder name is a tag associated to a file
++ e.g. the path /books/survival/water 
++ adds for example three tags: "books", "survival", "path"


[duplicated files]
+ for each file calculate the SHA1
+ when the SHA1 is duplicated, show it on the results
++ e.g. one entry and then the multiple locations where same file was found


[plugins]
+ allow to extract data from specific files
++ for example films
++ can call outside programs 
+ plugins are separate APK apps
++ can be upgraded separately
+ github repository host list of suggested plugins URLs
+ can create new tabs on the main app
+ plugin template needs to be provided


[themes]
+ themes are simple JSON files
+ change the colors of the app
+ used for light/night mode
+ can change font types and size
+ permit modifications
+ github repo hosts the themes available
+ users can add new themes to the folder themselves


[collection]
+ a URL to a github repository (any git server/URL)
+ JSON file contains the tag info and any other settings
++ title
++ description
++ other fields
+ can be imported/downloaded from a URL or local folder
++ is basically a zip file with all contents inside
++ when installing, the zip is extracted to a folder
+ permits to have versions
+ deletes previous versions to save space
+ collection can be created by any user
+ multiple users can be permitted to update a collection
+ collection can be exported by user as zip file
+ collections can be shared by IPFS
++ IPFS for android: https://github.com/textileio/android-ipfs-lite







