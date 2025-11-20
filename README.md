This is a fork of the original takt script for norns by itsyourbedtime.
To install, first ensure that you have uninstalled any previous version of takt.  
Then use the following commandline within maiden:
;install https://github.com/chailight/takt

![docs](lib/doc.png)

@chailight extensions

Global Clock
------------
By default, this version uses the norns global clock.
Use the Clock options to determine whether takt syncs to Ableton Link, external Crow input or sends out MIDI clock, or modular clock via a Crow output

MIDI chord output
-----------------
You can select chord output instead of note output on a MIDI track.
On the MIDI page, use E2 to scroll to the next setting after the note selection tile. Instead of selecting the next tile, you should see the note symbol above the selected note value light up. 

![docs](lib/takt_note.png)

Use E3 to scroll to the right to select a chord type (M = major, m = minor, etc). The selected note value will be the root of the chord. Chord inversions are currently not supported. If your selected device supports polyphonic playback, then you'll get a chord instead of a single note. 

![docs](lib/takt_chord.png)

Chord types and root notes can be adjusted per step just like any other parameter lock.

Just Friends, w/syn and crow support
------------------------------------
On the Parameters page, ensure that your JF, w/syn or crow output options are set to on.

![docs](lib/jf_enabled.png)

On the MIDI page, use E2 to scroll to the Device tile. Use E3 to scroll past the first four MIDI device number selections. Depending on which i2c devices are enabled in Parameters, you'll be able to select JF, w/syn or crow.

![docs](lib/jf_selected.png)

This track will send out notes to the selected device.
Note that when w/syn is selected, the UI updates to display various w/syn parameters. Currently these do nothing. You need to adjust w/syn via the Parameters page.
Similarly, when crow is selected, the UI displays various parameters which currently do nothing. Watch this space for updates.

MIDI CC LFO output
-----------------
This uses the hnds library by @justmat to provide additoinal LFO's for MIDI CC.
You can select an LFO from the relevant section of the Parameters page

![docs](lib/lfo_selection.png)

You can set the target of the LFO to be one of the 6 CC outputs for a given track, e.g. CC1 on track 8.

![docs](lib/lfo_target.png)

Note that the target number refers to the CC output "slot" on the MIDI page for that track. You can still change the actual CC number to be whatever you want, e.g. CC 127, and the LFO you assigned to that output position (e.g. 1) will continue to work.

![docs](lib/lfo_output_slot.png)

When you have an LFO assigned to a CC, you can't adjust the value of the CC manually.


