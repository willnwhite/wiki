# Give your JavaScript Slot Machine some stylish images
We've already set up the images for you in an array called images. We can use different indexes to grab each of these.

Here's how we would set the first slot to show a different image depending on which number its random number generates:

```javascript
$($('.slot')[0]).html('<img src = "' + images[slotOne-1] + '">');
```
