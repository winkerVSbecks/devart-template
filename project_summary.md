# Ellsworth Kelly Animated

## Varun Vachhar
- [github.com/winkerVSbecks](https://github.com/winkerVSbecks)
- [@winkerVSbecks](https://twitter.com/winkerVSbecks)
- [lambdafunction.ca](http://lambdafunction.ca/)

## Description
A couple of years ago I made a [Processing](http://processing.org/) sketch with the logic described in the image below. Shortly thereafter I came across Ellsworth Kelly's [Black Relief II](http://www.matthewmarks.com/new-york/exhibitions/2011-02-12_ellsworth-kelly/works-in-exhibition/#/images/5/). It seemed that, unknowingly, I had created an animated version of his painting.

![Early Prototype built with Processing](../project_images/polygon.png)

This led me to explore more of his work. His paintings carry an immense amount of potential energy in my opinion. It's as if they are kinetic sculptures frozen in time.

This project is an attempt to animate some of his pieces using web-based technologies.

Most of the works are made using [Box2dWeb](https://code.google.com/p/box2dweb/). A simple mouse click allows you to animate them. 

In the first piece, you can grab the interface of the blue blob and the surrounding green fill and drag it around. Press ? to see the underlying skeleton.

## Link to Prototype
- Web version: [winkervsbecks.github.io/ellsworthKellyAnimated](http://winkervsbecks.github.io/ellsworthKellyAnimated/ "winkervsbecks.github.io/ellsworthKellyAnimated")
- Google Chrome App: [chrome.google.com/webstore/detail/ellsworth-kelly-animated/mhgohnogimfoohafafblgpgonabjhlal](https://chrome.google.com/webstore/detail/ellsworth-kelly-animated/mhgohnogimfoohafafblgpgonabjhlal)

## Example Code
```
SpringyTriangle.prototype.impulse = function () {
	var ping = Math.random(-1,1);
	var pinger = 1;
	if (ping > 0) pinger = 1;
	if (ping <= 0) pinger = -1;
	var appliedForce = new b2Vec2(this.force.x*pinger / scale, this.force.y / (2*scale) );
	this.imp = this.a_imp.getPosition();
	this.a_imp.body.ApplyImpulse(appliedForce, this.imp);
};
```
## Links to External Libraries
- [Box2dWeb](https://code.google.com/p/box2dweb/)
- [Make a rope with Box2dWeb](http://www.binarytides.com/make-rope-box2d-javascript/)

## Images & Videos
![springy blob](../project_images/orange.gif)
![springy wavy box](../project_images/ropeinterface.gif)
