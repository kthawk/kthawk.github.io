layout: page 
title: "Air Quality Widget for Notion" 
permalink: /airquality_notion_embed

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tomorrow.io  Air Quality Widget</title>
    <style>
        .tomorrow {
            position: relative;
            min-height: 180px; /* Ensure widget has space to render */
            width: 100%;
        }
        
        .tomorrow a {
            position: absolute;
            bottom: 0;
            transform: translateX(-50%);
            left: 50%;
            color: transparent;
            font-size: 0;
        }
    </style>
</head>
<body>
     <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
        }
        
        .tomorrow {
            position: relative;
            padding-bottom: 10px;
            width: 100%;
            max-width: 4000px;
            margin: 0 auto;
        }
        
        .powered-by {
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .powered-by img {
            width: 250px;
            height: 10px;
        }
  </style>
    <!-- Widget Container -->
    <div class="tomorrow"
            data-location-id="120636"
           data-language="EN"
           data-unit-system="IMPERIAL"
           data-skin="light"
           data-widget-type="aqiPollen">
    </div>

    <!-- Widget SDK Loader Script -->
<script>
        (function(d, s, id) {
            if (d.getElementById(id)) {
                if (window.__TOMORROW__) {
                    window.__TOMORROW__.renderWidget();
                }
                return;
            }
            const fjs = d.getElementsByTagName(s)[0];
            const js = d.createElement(s);
            js.id = id;
            js.src = "https://www.tomorrow.io/v1/widget/sdk/sdk.bundle.min.js";

            fjs.parentNode.insertBefore(js, fjs);
        })(document, 'script', 'tomorrow-sdk');
        </script>
</body>
</html>
