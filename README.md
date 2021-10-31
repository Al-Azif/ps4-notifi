# Notifi

## Synopsis

Adds a single function `notifi()`. It functions like printf however the first arg is the image to use (NULL and any invalid input should default to the default image). Examples are as follows, 

```c
#include "notifi.h"

int percent = 0;

notifi(NULL, "We are %i%% complete", percent);

notifi(NULL, "%s", "Having \"NULL\" in the first arg means the default image will be used");

notifi(NULL, "%s", "We can use line breaks too\nJust like this!");

notifi("cxml://psnotification/tex_icon_champions_league", "%s", "If you missed the \"Original\" icon");
```

You can use URLs in the image space as well, just try it and see if it works.

## Notes

- The image string is limited to 1024 chars, including the null terminator.
