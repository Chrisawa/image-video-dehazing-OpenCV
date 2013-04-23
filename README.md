image-video-dehazing
image and video dehazing by median dark channel prior proposed by Gibson et al.
====================

Since we estimate the atmospheric light (AL) value for every frame, sometimes it changes a lot and makes the brightness of
the video change suddenly. So I added an AL smoothing part in the main function: AL(n) = alphaAL(n) + (1 - alpha)AL(n-1),
where n stands for the frame number and alpha is set to be 0.05.

Some problems:
1. Since the brightness of the dehazed frames is not only decided by the AL values, the variation of the brightness is
still noticeable.
2. w is the parameter which decides the degree of dehazing. If we use the default value of 0.95 in the paper, the dehazed
frames are more or less dark. But if we reduce the value to around 0.75, the brightness is fine but the dehazing result
seems not obvious enough.

please contact me if you have any idea about improving the algorithm or just would like to discuss it.

Yuze Chen
chenyuze1988@gmail.com
