# Blazor MAUI Query Parameter Issue

## Description
This project demonstrates an issue in **Blazor MAUI** where URLs containing a query parameter with a dot (`.`) cannot be force reloaded. 
The problem arises because the `Path.HasExtension` method incorrectly identifies the query parameter as a file extension, leading to unexpected behavior.

## Steps to Reproduce
* Clone the repository
* Open the solution
* Run the application on iOS or Android
* Navigate to the home page
* Click on the link to force a refresh/reload for the current page with query parameters.
* Observe the application navigating to a empty webpage with a "There is no content at url" message.

## Expected Behavior
The URL containing a query parameter with a dot should be correctly identified as a page URL, and the force reload should work as expected.  

## Actual Behavior
The URL containing a query parameter with a dot is incorrectly identified as a file path, causing the force reload to fail.

