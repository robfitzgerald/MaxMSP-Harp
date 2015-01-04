MaxMSP-Harp
===========

Max patch for the laser harp installation


Basic Instructions

1: Open "harp_base.maxpat"

2: for a demo, click the bang labelled "play rob's overactive midi test"

3: there are 5 sampler instruments.  as an example, there are some simple demo
instruments that can be loaded into any sampler instrument.  click the drop menu to see
the list of candidates, all listed by their respective data file ".dat".  switch these
freely.

to the right of the drop menu is a table, which is used to control the velocity response
range of each sampler instrument.  
x coordinates show the velocity value, from low to high.  note that a low velocity
refers to a higher scan, closer to the source of the sensor.
y coordinates are amplitude to play that instrument at that velocity.
this table allows the user to create velocity ranges that trigger the sound, as well
as allows for crossfading sample ranges.

4: there is a global_ignore_noteoff toggle below the samplers.  switching it to on
makes note off messages no longer affect playback.  the default value for this toggle
is stored in the patch p globals (upper left corner of the base patch, or, can be
opened with shift-tilde)

5: tilde initiates a global patch reset.

6: midi input is hardwired to the emu interface, but, if you want to receive from another
midi channel, then double-click the midiin object, and a drop menu will appear.  the 
cute little midi keyboard graphic that provides a playable interface is sending 
unreliable data and shouldn't be trusted.

7: in order to make new sample instruments available, open the instruments folder and
use the instrument data utility.  first, create a new directory in instruments.  fill
it with soundfiles that follow the naming convention [midi note #]_[any unique filename].
see existing instrument folders for examples.  then, run the utility.  select your new
instrument folder and follow instructions until you have generated your .dat file.  your
new instrument should be visible next time you load harp_base.maxpat.

ok!  that's the basic guide.  i ran short on time, i hope that's not confusing.  i will
be available once a day by email mon-wed, and then by wed evening i will be back in cell
range.

-rob