This is a simple development board for the QFP version of the ATMEGA1281. The
layout of the connector is an extended superset of the digital header found on
the Arduino Mega + an internal MajorCore development board I have also
created.

The idea of the connector is to make it trivial to use a dual window design
with the EBI/XMEM interface found in the 1281. 

Note: In my designs the EBI A15 is known as ~{CACHE}/BUS. I then use a different pin for EBI A15.
This allows me to carve the EBI address space into two 32k chunks. The lower
half is known as the cache segment that the 1281 uses as its internal cache.
The upper 32k is used as a view into a separate "bus" which is up to 32-bits in
size. 
