---
title: Putting Website offline with Service Worker
tags:
  - JavaScript
created: 2021-05-08
modified: 2021-05-08
---

```javascript
if ('serviceWorker' in navigator) {
  console.log("Let’s register Service Worker.");
  navigator.serviceWorker
           .register('/sw.js')
           .then(() => console.log("Service Worker Registered") );
}
```

The content of `sw.js` for the service worker. Please note that it runs in a different threads and not the same thread as the script in index.html runs.

```javascript
const cacheName = 'pcms-demo-only';
const cacheFileList = [  
  'https://unpkg.com/react@17.0.2/umd/react.development.js',
  'https://unpkg.com/react-dom@17.0.2/umd/react-dom.development.js',
  '/',      
  '/index.html',
  '/about.html',
  '/style.css',
  '/script.js'
];

/**** Service Worker Logic ****/

self.addEventListener('install', (e) => {
  console.log('[Service Worker] Install');

  e.waitUntil(
    caches.open(cacheName).then( cache => {
      console.log("Caching all");
      return cache.addAll(cacheFileList);
    })  
  );
});

self.addEventListener('fetch', function(event) {
  console.log(event.request.url);

  event.respondWith(
    caches.match(event.request).then(function(response) {
      return response || fetch(event.request);
    })
  );
});
```