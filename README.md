# p410n3-typo3-blog

This is the code currently at use at https://blog.palone.top. It was done as an excerise, and because i didnt like the theme of my old blog that much. So I made my own for TYPO3.

I also wanted to start actually using CSS Grid. So I also did that.

## Installation

To install the theme include the TypoScript files:

    <INCLUDE_TYPOSCRIPT: source="FILE:fileadmin/p410n3/main.txt">
    <INCLUDE_TYPOSCRIPT: source="FILE:fileadmin/p410n3/additionalSettings.txt">
    
I also suggest copying that Backend Layout: 

    mod.web_layout.BackendLayouts {
      exampleKey {
        title = Example
        
        icon = EXT:example_extension/Resources/Public/Images/BackendLayouts/default.gif
        config {
          backend_layout {
            colCount = 1
            rowCount = 3
            rows {
              1 {
                columns {
                  1 {
                    name = Content
                    rowspan = 2
                    colPos = 1
                  }
                }
              }
              2 {
                columns {
                }
              }
              3 {
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

## What is that Design?

I was inspired by that site: https://brutalist-web.design/
