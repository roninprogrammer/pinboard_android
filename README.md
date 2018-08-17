# PinBoard App

Imagine me are on the Android team in on of the company and working with some colleagues on the pinboard (the scrolling wall of images), you split up the tasks among each other and your task is to create an image loading library that will be used to asynchronously download the images for the pins on the pinboard when they are needed
<b>Requirement:</b>

The library will also be useful for all other parts of the app where asynchronous remote image loading is required. The images are available on a publicly accessible URL (like a CDN). The library should be general purpose and not assume anything about the use case, the pinboard is an example but other parts of the app that show images will also use it (e.g. a user's profile pic on the profile screen).

Let's says One of your colleagues will also want to use the library for loading JSON documents, and you just know that your boss and colleagues will love your library so much that they will ask you to support other data types in the future as well, so your design should not limit support to a particular data type.

The purpose of the library is to abstract the downloading (images, pdf, zip, etc) and caching of remote resources (images, JSON, XML, etc) so that client code can easily "swap" a URL for any kind of files (JSON, XML, etc) without worrying about any of the details. Resources which are reused often should not be continually re-downloaded and should be cached, but the library cannot use infinite memory.

<b>Purpose of the Showcase this app</b>

1. Readability
   
   Class and method names should clearly show their intent and responsibility.

2. Maintainability

“SOLID” Principles and design pattern;
MVP/MVVM model.

3. Scalability
This application should easily accommodate possible future requirement changes.

4. Testability
This application accompany code with test classes



