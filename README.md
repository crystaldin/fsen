Our example is verified by giving the following command to our extended Maude model checker:

Maude> in example.maude 

--------------------------------------EXECUTION RESULTS--------------------------------------

==========================================
mod DWINPUT
==========================================
reduce in DWINPUT : check(init, feature "Front Sensors" exists starts andalso feature "Rear Sensors" exists starts 
between feature "Sensors" exists starts and 2) .
PASS
result Bool: true
==========================================
reduce in DWINPUT : check(init, feature "Touch Screen" exists starts when feature "Button Interface" exists stops) .
PASS
result Bool: true
==========================================
reduce in DWINPUT : check(init, feature "Sensors" has type MANDATORY starts at 1) .
FAIL
result Bool: false
==========================================
reduce in DWINPUT : check(init, feature "WiFi" exists starts between 3 and 6) .
FAIL
result Bool: false
