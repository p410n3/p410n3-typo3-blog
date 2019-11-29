# p410n3-typo3-blog
My blog. Recoded for TYPO3 9 LTS as an excercise.

### Required Extenions

https://typo3.org/extensions/repository/view/blog

### SETUP
````
<INCLUDE_TYPOSCRIPT: source="FILE:blog/ts/typoscript.txt">
````

### CONST
````
plugin.tx_blog.settings.comments.active = 0

plugin.tx_blog.settings.lists.posts.maximumDisplayedItems = 3
plugin.tx_blog.settings.lists.posts.maximumDisplayedItems = 0
plugin.tx_blog.settings.lists.pagination.itemsPerPage = 3

<INCLUDE_TYPOSCRIPT: source="FILE:blog/ts/constants.txt">

````

### Fonts are hosted locally
