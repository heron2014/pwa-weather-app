### pwa-weather-app
Learn progressive web app - based on Google Developers [Tutorial](https://developers.google.com/web/fundamentals/getting-started/your-first-progressive-web-app/)

### What do you need to know?

- what is the app shell model, how to design and construct it
- what are Service Workers?
- https servers
- manifest
- how to make your app work offline
- how to store data for use offline later


### What is the app shell model?

- is the minimal HTML, CSS, and JavaScript that is required to power the user interface
- it is the core components necessary to get your app off the ground, but likely does not contain the data
- its first load should be extremely quick, then immediately be cached

##### How to design app shell?

- What needs to be on screen immediately?
- What other UI components are key to our app?
- What other resources you app needs? example: images, styles, js


![app-shell](readme-images/app-shell.png)


##### What are Service Workers?

A service worker is a script that is run by your browser in the background, separate from a web page, opening the door to features which don't need a web page or user interaction.

They provide foundation for:

- offline experience
- background sync
- push notification
- geofencing
- caching

Service worker functionality is only available on pages that are accessed via HTTPS.

Choosing the right caching strategy for your data is vital and depends on the type of data your app presents. For example, time sensitive data like weather or stock quotes should be as fresh as possible, while avatar images or article content can be updated less frequently.

Steps to add the Service Worker in your app:

1. Create a JavaScript file that will be the service worker (must live in the app root)
2. Check if the browser support it and register the JavaScript file as the service worker.


### How to run this repo:

Run a simple web server with ```python -m SimpleHTTPServer 8000``` then visit: ```http://localhost:8000/```

App is live at https://pwa-weather-app.firebaseapp.com

#### Steps to deploy on Firebase Https server [here](https://developers.google.com/web/fundamentals/getting-started/your-first-progressive-web-app/step-08?hl=en)

### References

- Excellent article by Addy Osmani [here](https://addyosmani.com/blog/getting-started-with-progressive-web-apps/)
- [Service Workers](http://www.html5rocks.com/en/tutorials/service-worker/introduction/)
- [Service Workers Cookbook](https://serviceworke.rs/)
- [Building Flipkart Lite: A Progressive Web App](https://medium.com/@AdityaPunjani/building-flipkart-lite-a-progressive-web-app-2c211e641883#.jnt977z1l)
- [Flipkart](http://tech-blog.flipkart.net/2015/11/progressive-web-app/)
- [Offline Cookbook](https://jakearchibald.com/2014/offline-cookbook/)
- Avoid edge cases when caching in production using Service Workers [sw-precache](https://github.com/GoogleChrome/sw-precache)
- [learn-progressive-enhancement](https://github.com/nelsonic/learn-progressive-enhancement)
