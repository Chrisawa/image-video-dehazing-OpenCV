image-video-dehazing
image and video dehazing by median dark channel prior proposed by Gibson et al.
====================

There is a problem that if we use the original estimated airlight value for dehazing, it makes most of dehazed images/frames
too dark. Therefore I put an airlight compensation part which is able to handle with most of the hazy video frames.

However, the compensation part is made only by the observations on the test videos I found, please try some clips of your
own. Moreover, since sometimes the airlight value of current frame changes too much from the one of the previous frame,
the compensated airlight values need to be smoothed as well to remove the brightness changes.

3 questions:
1. Any better way of airlight compensation?
2. I put the compensation part in the main function for the reason of processing different frames and it made the main function too large.
3. There's still noticeable brightness changes if the scenes between frames change too much. Solutions?


Yuze Chen
