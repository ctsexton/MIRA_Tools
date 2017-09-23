# MIRA_Tools
Collection of Max patches for use with Cycling 74's MIRA app for iPad. Download MIRA package from Cycling 74 package manager in Max. These mostly focus on multitouch input using [mira.multitouch] and related objects. They could be easily adapted for use with any other multitouch interface input (Wacom tablet, TC Data, etc.). 

Multitouch_SVF: This patch presents a state variable filter control interface. The distance between touch points determines filter cutoff (average distance of touch points to their centroid) so cutoff increases as the hand is outstretched. Rotating the hand CW transitions the filter type from Low Pass to High Pass and rotating CCW transitions in the other direction. The distance from the touch points to the centre of the surface is mapped to resonance - try moving two fingers around the screen to see how it responds. This patch requires the EASE package from Cycling 74 (via package manager).

XY_highest_point: Outputs the position of the touch point with the lowest Y value (MIRA multitouch is at zero in the Y axis at top of iPad). Useful for calculating the direction of rotation.

XY_rotate: Outputs the direction of rotation of two points around their centroid (CW or CCW). Also outputs DELTA - the change in radians - and distance from center or centroid.

mt.rotate: for use in Multitouch_SVF. Takes mira.multitouch input and outputs Rotation Delta, Centroid, Average Distance from Centroid, no. of touch points. 

mira.mt.fingercount: Outputs no. of fingers touching surface. Potentially unnecessary if you use mira.mt.centroid (from MIRA package) - will address this in update.

example_patch: An example of the Multitouch_SVF filtering some oscillators and noise. Requires iPad with MIRA app.
