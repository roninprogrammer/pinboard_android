# PinBoard App

[SCENARIO]
Imagine me are on the Android team from XYZ company(made up company) and working with some colleagues on the pinboard (the scrolling wall of images), I am split up the tasks among each other and my task is to create an image loading library that will be used to asynchronously download the images for the pins on the pinboard when they are needed..

<b>Requirement:</b>

The library will also be useful for all other parts of the app where asynchronous remote image loading is required. The 
images are available on a publicly accessible URL (like a CDN). The library should be general purpose and not assume anything about the use case, the pinboard is an example but other parts of the app that show images will also use it (e.g. a user's profile pic on the profile screen).

Let's says one of my colleagues will also want to use the library for loading JSON documents, and  just know that my boss and colleagues will love my library so much that they will ask me to support other data types in the future as well, so my design should not limit support to a particular data type.

The purpose of the library is to abstract the downloading (images, pdf, zip, etc) and caching of remote resources (images, JSON, XML, etc) so that client code can easily "swap" a URL for any kind of files (JSON, XML, etc) without worrying about any of the details. Resources which are reused often should not be continually re-downloaded and should be cached, but the library cannot use infinite memory.

API : http://pastebin.com/raw/wgkJgazE 

<b>What i am trying to archive by develop this application</b>

1. Readability
   
   + Class method names should clearly show their intent and responsibility.

2. Maintainability

   + “SOLID” Principles and design pattern;
   + MVP/MVVM/MVC model.

3. Scalability
   
   + This application should easily accommodate possible future requirement changes.

4. Testability

   + This application accompany code with test classes

Technical Specification

1. Images and JSON should be cached efficiently (in-memory only, no need for caching to disk);
2. The cache should have a configurable max capacity and should evict images not recently used;
3. An image load may be cancelled;
4. The same image may be requested by multiple sources simultaneously (even before it has loaded), and if one of the sources cancels the load, it should not affect the remaining requests;
5. Multiple distinct resources may be requested in parallel;
6. You can work under the assumption that the same URL will always return the same resource;
7. The library should be easy to integrate into new Android project / apps;
8. You are supposed to build a solid structure and use the needed programming design patterns;
9.Think that the list of item returned by the API can reach 100 items or even more. At a time, you should only load 10 items, and load more from the API when the user reach the end of the list;
10. Usage of Material Design UI elements (Ripple, Fab button, Animations) and also adding "pull to refresh" is an advantage.
 is an advantage;




