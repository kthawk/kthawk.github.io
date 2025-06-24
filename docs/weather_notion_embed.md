layout: page
title: "Weather Widget for Notion"
permalink: /docs/weather_notion_embed

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tomorrow.io Weather Widget</title>
    <style>
        .tomorrow {
            position: relative;
            min-height: 175175px; /* Ensure widget has space to render */
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
            max-width: 1200px;
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
            height: 18px;
        }
  </style>
    <!-- Weather Widget Container -->
    <div class="tomorrow"
         data-location-id="120636"
         data-language="EN"
         data-unit-system="IMPERIAL"
         data-skin="light"
         data-widget-type="upcoming">
        <a href="https://weather.tomorrow.io/" rel="nofollow noopener noreferrer">
            Powered by Tomorrow.io
        </a>
    </div>

    <!-- Widget SDK Loader Script -->
     <script>
        // Load Tomorrow.io script
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
        
        // Create the powered by link
        const widgetContainer = document.querySelector('.tomorrow');
        const poweredByLink = document.createElement('a');
        poweredByLink.href = "https://weather.tomorrow.io/";
        poweredByLink.rel = "nofollow noopener noreferrer";
        poweredByLink.target = "_blank";
        poweredByLink.className = "powered-by";
        
        const poweredByImg = document.createElement('img');
        poweredByImg.alt = "Powered by Tomorrow.io";
        poweredByImg.src = "https://weather-website-client.tomorrow.io/img/powered-by.svg";
        poweredByImg.width = "250";
        poweredByImg.height = "18";
        
        poweredByLink.appendChild(poweredByImg);
        widgetContainer.appendChild(poweredByLink);
    </script>

</body>
</html>
