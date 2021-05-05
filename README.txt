Amiga 1000 Rejuvenator Recreation Project
-------------------------------------------------------------------------------------------

Any projects, additions, alterations, or improvements based on this Amiga-1000-Rejuvenator
project must be openly shared, includingsoftware or PLD coding.  I belive the license I
have specified in LICENSE equates to this, but I am not a license expert, so suggestions
are welcomed.  And with that out of the way...

Thanks to the extreme graciousness of intric8 at amigalove.com, I had on loan a Rejuvenator
board for the Amiga 1000.  Originally created by Greg Tibbs, this Amiga 1000 hardware
upgrade provides up to 2MB Chip Memory, an onboard ROM based kickstart, a video slot, and
additional Fast memory.  Installation requires replacing the A1000's daughterboard with the
Rejuvenator.

This project aims to recreate the original Rejuvenator, and eventually improve on the
original design.

Schematics and board artwork are complete, and have been fabricated and tested.  Several
design errors on the original Rejuvenator which required bodge wires and trace cuts to
rectify have been identified and eliminated in the new design.

The last remaining obstacle is discovery of the PLD code contained in the four protected
PALs.  If these can be persuaded out of their lock boxes, or perhaps logically reasoned,
this project will be complete.

Since these are early PALs, and not GALs, I had hoped using a logic analyzer along with
Charles Macdonald’s Protected PAL reader would be enough to reason out the equations, but
the attempt is troublesome.  Recent discoveries in bypassing GAL protection simply do not
work with PALs.

27C020 dumps of the PALs are included in the PLD folder, along with analysis using PA.exe.
Unfortunately, many of the outputs include tri-state or feedback, which is a registered
output not able to be analyzed by PA.exe.

Additionally, two of the PALs are 20L8 versions, which have 4 additional I/O pins.  These
PALs were broken down into 3 subsections to test every output pin for registered functions.
For the combinatorial equations, eventually all inputs could be tested if they were
included in the output function and a final map of the pins could be identified and wired
to complete the equation.  For registered functions, perhaps knowing the hardware layout
and using known equations from Amigas or other projects with 2MB Chip memory could fill in
the gaps.

I also thought of some more extreme measures, but since this is not my personal hardware,
I would not be comfortable risking the PALs on unproven methods.

Unfortunately, I haven’t had the time to work this project since 2020, and other individuals
are looking at a chance to crack the PLDs. I hope my efforts can at least provide some
insight on the hardware.  Nothing would be better than finally knowing these equations!

As of recent, my sporadic efforts had changed from trying to read the PALs, to using a
hardware analyzer (DSLogic) to recreate the equations.  This will not be possible anymore
as I have shipped the original board and PALs back to intric8.

I will continue my efforts as time allows with more hardware study, memory mapping, and
signaling.

Best of luck to everyone contributing.  And if anyone has a Rejuvenator for sale, hit me
up!  ;D



--joethezombie
