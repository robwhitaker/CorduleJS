CorduleJS
==========

CorduleJS (pronounced like "cordial") is short for **Core Module JS**. CorduleJS is a lightweight module control system that streamlines the process of writing modular JavaScript by providing a central hub (or core) which manages all of the modules in an application. While these modules remain unaware of the existence of other modules, CorduleJS enables them to communicate using the `pushRequest` and `observe` functions. 

--------

####pushRequest
The `pushRequest` function allows the user to pass a request string and a set of parameters. CorduleJS will attempt to match the request string with an observer that is listening for that type of request. Any observers listening for that request string will fire off their callback function with the set of parameters passed in during the call to `pushRequest`. An array of results from all listening observers will be returned.

####observe
The `observe` function creates an observer, or a listener which fires its callback function when the request it is listening for is pushed.

--------

If a request is pushed, but no observers are listening for that request, `pushRequest` will return false, and the program will continue running smoothly. In other words, a missing module should never affect the functionality of other modules. Only the functionality of the missing module will not be present. 

Installation
--------------

Installation of CorduleJS is as simple as including a single file at the bottom of your `<body>` tags.
```
<body>
<!-- page content -->

<script src="CorduleJS.js"></script>
<!-- other script includes -->
</body>
```

Once CorduleJS is included, you can begin adding modules to your application with the `addModule` function. Just be sure that CorduleJS is loaded before attempting to add modules!

Tutorial
---------
*Coming soon.*

License
-------------
MIT.
