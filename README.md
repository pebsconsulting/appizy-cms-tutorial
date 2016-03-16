# Appizy CMS integration tutorial 

Tutorial to modify Appizy output to integrate easily your application into your website.

**This method has been tested with WordPress and Wix.**

Appizy version: 0.10.0

## Starting point

The ```bmi_appizy.ods``` spreadsheet has been used to generate the content of ```appizy-output``` folder. It contains two files working together: 

```
appizy-output/
	└── myappizy.html # Display of the application: style and html tags
	└── script.js     # Calculations
```

You might want to merge those two files to have your application code in one file. This way you can easily integrate it in WordPress or Wix.

## Refactor

The content of ```script.js``` has been copied into ```myappizy.html```.

    // before, in myappizy.html
    <script src="script.js"></script>

    // after
    <script>
	    /* content of script.js */
    </script>

The application is now self contained in ```myappizy.html```. No need of ```script.js``` anymore.

If you are using **Wix**, follow this article to [add your HTML application](https://www.wix.com/support/html5/article/adding-html-code) into your website.

For **WordPress** users we recommand to host the application with the method of your choice (self hosting, Dropbox, Github Pages...) and then use an iframe to integrate your application:

```
<iframe src="http://example.com/link_to_your_application.html" width="100px" height="300px"></iframe>
```

This iframe method is also valid for **Wix** users.
