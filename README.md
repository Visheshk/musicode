##Musicode
A music programming puzzle game.
With heavy inspiration from RoboZZle, we wanted to make a more open ended game that involved making music - something we saw as potentially more fun, and try to make it easier so that there's more scope to play around, and also manage solving puzzles.

##Currently
The prototype supports making disks.
Each disk has all these properties, where it's supposed to play music, and which nodes send it to which other disk.

##Interface
Every disk is divided into 8 time-unit-sectors. This is to allow for description of 8-beat music. Further, every disk has 3 concentric circles. These are to be associated with different notes. For instance, markings in the smallest circle, play C, the next play D, the next play E, and so on.

The nodes on the circumference, are to link one disk to another. This is like a function call. When the 'spindle' reaches a linked node, it stops playing the current disk, and starts playing the disk it is linked to.

##Limitations
Currently, the UI is very poorly implemented. There's supposed to be support for adding and removing disks, and then we plan to introduce a puzzle system, where the music you make is displayed more clearly, and the aim is to make music or notes of a particularly described manner.

A strong technical flaw, is the lack of stacking of functions, which makes recursion and many aspects of function calling redundant/incorrectly done. When another function is called, that function runs from the start, and all its operations are popped from a stack sequentially. Calls to another place in between cause that function to happen, and the compiler to return to the previously stacked operations after. None of this happens in the current emtaphor, as made. A link only causes the other disk to start playing from wherever it was. Yet to explore how to do this, if at all.

