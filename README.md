# Link-Recognition
Recognize links in an element text and replace with anchor tags

###What can I do with it
You can use this simple jquery plugin to add anchor tags for the links in in text in HTML page. Useful if you are loading content synchronously from third party sources like Twitter of Facebook for example.

###How to add to a page
Add a reference to jQuery library, this plugin library and this plugin CSS stylesheet
```html
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
<script type="text/javascript" src="/src/jquery.linkrecognition.js"></script>
```
Simply add a container (div or any other element) and apply the plugin to it.
```html
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>Link Recognition test</title>
    <script type="text/javascript" src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
    <script type="text/javascript" src="/src/jquery.linkrecognition.js"></script>
    <script type="text/javascript">
        $(document).ready(function () {
            $(".content").LinkRecognition(
                {
                    target: "_blank",
                    cssClass: "external-link"
                }
            );
        })
    </script>
</head>
<body>
    <div class="content">
        <p>
            Lorem ipsum dolor sit amet, consectetur http://google.com adipiscing elit.
            Vestibulum eleifend ut eros at ullamcorper http://yahoo.com. Nullam dictum cursus lectus et eleifend http://www.facebook.com.
        </p>
        <p>
            Duis nulla elit, cursus vitae libero eu, porta http://wikipedia.org vehicula orci.
            Donec vitae velit mi. Duis risus eros, http://www.jquery.com elementum et semper eu, tempus eu mi. Suspendisse sed viverra mi, quis aliquet nulla.
        </p>
    </div>
</body>
</html>
```

###What are options for plugin
As this is pretty simple plugin, there are not so many properties taht you might think of using for it :)

* **target** - Target property of the anchor tag that will be created for url text. 
* **cssClass** - Css class to be applied to newly added anchor tags.
