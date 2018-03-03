# Giveth Wiki
The wiki for the Giveth DApp, the Giveth DAC and everything else included in the Giveth universe. A place to get into detail about concepts, explanations and guides./customize parts of the wiki, please refer to: [http://www.mkdocs.org/](http://www.mkdocs.org/)

## About
The wiki is accessible via this link: https://wiki.giveth.io

It is built with https://netlify.com using the static site generator mkdocs http://www.mkdocs.org/

## Contributing
**Contributing content is very easy!** Just edit the files contained in the wiki directory.

**Please note:** If you are a **first time contributor to the Wiki**, please talk to us on Slack first to get you started (#documentation)

For an introduction to markdown, see: https://guides.github.com/features/mastering-markdown/

You can edit the files either directly on GitHub, or clone the project and push changes to a separate branch. It is possible to preview your changes directly in your pull request via netlify's preview build option.

## Installation
Requires MKdocs to test locally.  [http://www.mkdocs.org/](http://www.mkdocs.org/).

## User Guide
See a detailed guide here: [http://www.mkdocs.org/user-guide/writing-your-docs/](http://www.mkdocs.org/user-guide/writing-your-docs/)

**Please Note:** Before considering a new page, pls look at the Wiki structure and see if it fits as an addendum to an existing article or consider if your content may be suited for the **FAQ**, or the **glossary**

### To add a new page:
  1 - Create a new markdown file (.md) in a subfolder of /wiki/

  2 - Add a new entry that points to your newly created file under pages: in mkdocs.yml

### To add a new category:
  1 - Create a subfolder in /wiki/

  2 - Add a new entry that points to your newly created folder under pages: in mkdocs.yml

### Visual Identity:
  If you consider implementing some graphics, pls refer to the visual identity page for info on typefaces, colors, and the asset repository here: [https://wiki.giveth.io/documentation/visual-identity/](https://wiki.giveth.io/documentation/visual-identity/)

### Images:
  To add an image first upload it to /images/subfolder/, then insert a link to the file in your document:

  ```![ImageName](image/subfolder/imagefile.png)```

### Shields

Please create shields from https://shields.io/
