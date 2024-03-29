Changelog
===================

Due to the fact the the original developer of this code is on leave I have to make some edit myself. To make sure I don't make a mess
of things and all my steps can be traced this file in addition to git tracking was added

V1.0.0
---------
The initial release by Peter.

V1.0.1
---------
Homing update

.. attention::
    I tried to turn up the zeroing speed but with no result

Changed
^^^^^^^^^
- Added a return position after zeroing (axis does not return to 0 but zero + offset) so the homing 
    pin doesnt get damaged (line 1979)
- Upped the ZERO_SPD to 5000 (from 600)
- Switched homing order (now first y then x y can be centered)
- Y now centers after zeroing the axis
- Changed x and y man endpos to 659500 (center)
- Changed homing so it now centers instead of go to the switch
- Fixed small spelling errors

V1.0.2
---------

Changed
^^^^^^^^^^
- Fixed the homing position correction (X axis corrected center position after zero now during zero)
- Fixed some issues with setting the manual end position and homing to the center instead of zero position
  (Z still homes and zeros to the zero position)

V1.0.3
--------

Added
^^^^^^^^^^
- Jogging function

.. warning::
    The jogging function on the base controller is not the same as jogging in the stacking system. Jogging in this case means
    a relative move of a predetermined distance.

Changed
^^^^^^^^^^
- Added auto status updating function (has not yet been enabled)
- Changed the zero speed to 500 

.. warning::
    The zero speed is not given in steps/s, it is unknown which unit it is given in, but 500 seems to be a safe speed of around
    25600 steps/s (1 Hz).

V1.0.3
------------

Changed
^^^^^^^^^^^^^^
- Updated the cooling and heating PID parameters to reduce overshoot, still has to be performance tested

