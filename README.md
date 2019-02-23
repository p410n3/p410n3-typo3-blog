# p410n3-typo3-blog

This is the code currently at use at https://blog.palone.top. It was done as an excerise, and because i didnt like the theme of my old blog that much. So I made my own for TYPO3.

I also wanted to start actually using CSS Grid. So I also did that.

## Installation

The template was initially made for TYPO3 8 LTS but is now used at TYPO3 9 LTS as well.
For the blog functionality I use the [tx_news plugin](https://github.com/georgringer/news). Other news system will need CSS changes

To install it via SSH, simply navigate to <your site>/fileadmin and git clone it.

````
git clone https://github.com/p410n3/p410n3-typo3-blog.git
````

The in your TYPO3 include the scripts in your SETUP and CONSTANT fileds by adding these lines in the Backend:

````
    # For Setup Area
    <INCLUDE_TYPOSCRIPT: source="FILE:fileadmin/p410n3/conf/setup/main.txt">

    # For Constant Area
    <INCLUDE_TYPOSCRIPT: source="FILE:fileadmin/p410n3/conf/constants/constants.txt">

````

The file `/conf/setup/additionalSettings.txt` contains general settings and plugin specific values. You should probably change some things there.
    
I also suggest to add that Backend Layout to your ROOT Page TSConfig: 
````
mod.web_layout.BackendLayouts {
  exampleKey {
    title = p410n3-blog
    
    icon = EXT:example_extension/Resources/Public/Images/BackendLayouts/default.gif
    config {
      backend_layout {
        colCount = 1
        rowCount = 2
        rows {
          1 {
            columns {
              1 {
                name = Content
                colPos = 1
              }
            }
          }
          2 {
            columns {
              1 {
                name = Footer
                colPos = 2
              }
            }
          }
        }
      }
    }
  }
}
````

Last step is to add a Route enhancer to your site's config.yaml for the news plugin as desribed [here](https://stackoverflow.com/questions/52983851/how-to-get-speaking-urls-for-news-7-0-7-on-typo3-9-5-0)

## What is that Design?

I was inspired by that site: https://brutalist-web.design/


## Why no fluid?

Due to the extreme minimalist design, I didn't consider using Fluid neccesary. 
Same goes for the CSS, it's to simple to set up a preprocessor in my opinion.
