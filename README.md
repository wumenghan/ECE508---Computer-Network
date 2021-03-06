# Low-traffic browser screen sharing
A **low-traffic** visual monitoring system (with **realtime and replay** modes) that aims to facilitate online user experiments.

## Getting Started
Install dependencies
```sh
$ npm install   # for the first time
```
Start server
```sh
$ npm start
```
Then visit `localhost:8010/dashboard`.

## Resources
* Simulate mouse events <https://github.com/kangax/protolicious/blob/master/event.simulate.js> and <https://stackoverflow.com/questions/6157929/how-to-simulate-a-mouse-click-using-javascript>
* Get Xpath, `getPathTo` - <https://stackoverflow.com/questions/2631820/how-do-i-ensure-saved-click-coordinates-can-be-reloaed-to-the-same-place-even-i/2631931#2631931> and <https://stackoverflow.com/questions/36452390/get-xpath-of-a-dom-element-with-jquery>
* Select by Xpath, `jquery.xpath.js` - <https://stackoverflow.com/questions/6453269/jquery-select-element-by-xpath> and <https://github.com/ilinsky/jquery-xpath>
* Web video player, [video.js](https://videojs.com/) and [videojs-panorama](https://github.com/yanwsh/videojs-panorama) which supports 360 video
* [Free 360 video download](https://www.mettle.com/360vr-master-series-free-360-downloads-page/)
* [Custom Mouse Pointer in JS](https://www.youtube.com/watch?v=QyeBCBYXjfw)


## Fatal issues with Iframe:
[Hard to Detect Click into Iframe using JavaScript](https://stackoverflow.com/questions/2381336/detect-click-into-iframe-using-javascript)
* We can at most know that we click on Iframe element, but cannot know the clicked elements, let alone simulate mouse events into Iframe
* Therefore, it's impossible to embed Youtube.
* Solution: use [video.js](https://videojs.com/) to load video in the same page.

## Key notes:
Simulate mouse events on video player
* Must use "mousedown" and "mouseup", not "click" event
* Must pass the correct clicking XY, not 0,0
* The target is the canvas (created by videojs-panorama), not the video


## Possible tasks:
* [A Subjective Study on QoE of 360 video for VR communication](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8122249)
* [A survey of network virtualization](https://www.sciencedirect.com/science/article/pii/S1389128609003387)
* [A blueprint for introducing disruptive technology into the Internet](https://dl.acm.org/citation.cfm?id=774772)
