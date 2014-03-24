MSLiveBlur
==========

The MSLiveBlurView dynamically blurs the content on the screen and updates at the given interval.
I use a condensed version of [GPUImage](https://github.com/BradLarson/GPUImage) to do the blurring.

# Usage

#### For live blur:

    #import "MSLiveBlur.h"
    [[MSLiveBlurView sharedInstance] blurRect:CGRectMake(0, 0, 100, 100)];

#### For static blur:

    #import "MSLiveBlur.h"
    [[MSLiveBlurView sharedInstance] setBlurInterval:kLiveBlurIntervalStatic];
    [[MSLiveBlurView sharedInstance] blurRect:CGRectMake(0, 0, 100, 100)];

then, to update manually:

    [blurView forceUpdateBlur];

# Todo:
* Figure out how to only blur views beneath so as not to require a new window
* Different shapes (ex: rounded corners)

# Done
* Live blur with variable interval
* Live blur appears on top of the application and blurs underneath
* Specify the size of the blurred area so it does not blur the entire screen (i.e. actually use the given frame)
* Tint color
* Support multiple areas at once