# lgpt_manual
A Little GP Tracker Manual because the official one seems to be gone forever.

This is mostly a transcription of a youtube video: https://www.youtube.com/watch?v=ejYSnCWLc6A .

Additional advanced controls from https://www.youtube.com/watch?v=_IDQZkzc9sQ .

I am planning to learn more about LGPT over the next month but we'll see. At the very least it'll be good to have a list of shortcuts for the program on the internet in text form ... somewhere.

I did also find https://github.com/djdiskmachine/LittleGPTracker/blob/master/docs/wiki/What-is-LittlePiggyTracker.md and https://github.com/djdiskmachine/LittleGPTracker/blob/master/docs/wiki/quick_start_guide.md.

... I don't know why I didn't realize that those official documentation guides existed before! This is ... a simplified version of that, I guess.

# General Controls
- Arrow keys: Move around.
- Hold right trigger and the arrow keys to change pages. The map on the top left shows you where you are. The pages in the map are:

```
Project             Groove
Song   Chain Phrase Instrument
             Table  Table
```

You can only move from Song to Chain, Chain to Phrase, Phrase to Instrument, etc., after selecting a Chain/Phrase/Instrument. If you have a new song, you might need to create one (See CREATE below).

- Start or stop the song: press Start.
  - If you're in Chain or Phrase mode, it will play only that Chain or Phrase, unless you press start and right shoulder at the same time, then it’ll play the song from that spot.
- Create a new chain or phrase: press A twice. This fills the slot with the first chain or phrase number.
  - (Pressing A once just fills the spot with the 'default' chain/phrase/note/etc.)
- Edit a chain/phrase/instrument/note: select it with the arrow keys, hold a, and then move the arrow keys.
  - Up/down moves by 10, moving right is +1, left is -1.
  - All of these are represented by hexadecimal values.
- Delete: select with the arrow keys, then press A and B at the same time.
- Selection: Press left shoulder and B to go into selection mode. (You can let the keys go after going into that mode.) Move the selection with the arrow keys, then do one of:
  - Copy: Press B (copy).
  - Cut: Press left shoulder again and A (cut).
- Paste: copied or cut data, press left shoulder and A at the same time, with the same command as you cut with.
- Clone: select the data you want to clone, hold the left shoulder, and press b and then a.
  - This will 'clone' that information into a new chain, and you can edit it without affecting the previous chain you had.

# Advanced
- Selection:
  - While in selection mode, holding left trigger and pressing B twice will select the whole row right away. You can then release the buttons and move down to get a specific place.
  - While in selection mode, holding left trigger and pressing B three times will select the whole screen.
- In Song mode to mute a column (track), select the track, hold right trigger, hold B, and then let go of the right trigger. You can do this again to unmute a specific column as well.
- To solo a track, select the track, hold right trigger, hold A, and then let go of the right trigger.
  - Hitting both triggers will unmute and unsolo all triggers.
 
# Tables and Effects
- Tables are both a way to affect phrases or instruments on a step-by-step basis. You can, for instance, 'approach a volume at a speed', or 'hop to a place a number of times'.
- In general a table is a 16-step sequence with two hexidecimal selections on each step.
- You can have up to three effects per step within a table. You can have two effects per step within a phrase as well. These all use the same effects.
  - In Phrases the effects are listed backwards from the way I listed them here. 

All of this information is in the program and in https://github.com/djdiskmachine/LittleGPTracker/blob/master/docs/wiki/What-is-LittlePiggyTracker.md,
but I find it's nice to read it in a shorter list, so I made this.
- ARPG: Arpeggio. Cycle through relative pitches from original pitch.
- CRSH: Drive and Crush. Set Drive to aa and crush to b.
- DLAY: Delay bb tics.
- FBMX: Set feedback mix to BB at speed AA.
- FBTN: Feedback Tune. Set feedback tune to BB at speed AA.
- FCUT: Filter Cutoff. set cutoff to bb at speed aa
- FLTR: Set filter in general. Cutoff aa resonance bb
- FRES: Filter Resonance. Set resonance to BB at speed AA.
- GROV: Trigger Groove bb.
- HOP: Hop to location BB AA times.
- IRTG: Instrument Retrig. Retrig and transpose to bb at speed aa.
- KILL: Stop playing note after bb tics.
- LEGA: Legato. slide from previous note to pitch BB at speed AA
- LPOF: Loop Offset. Shift loop start and loop end values aaaa digits.
- MDCC: Midi CC message aa value bb
- MDPG: send program change bb to current channel
- MVEL: Midi velocity, set to bb
- PAN: Pan to value bb at speed aa
- PFTN: Pitch Finetune. Fine tine to bb at speed aa.
- PLOF: Play Offset virtually cuts any sample in 256 chunks. jump absolutely to chunk aa, or relatively move forward/back bb chunks.
- PTCH: approach pitch bb at speed aa
- RTRG: Retrig loop from current position over 'bb' tics at speed 'aa'
- STOP: Stop the song immediately
- TABL: Table, trigger table 'bb'
- TMPO: sets the tempo to hex value bb
- VOLM: Volume, approach volume 'bb' at speed 'aa'

# Grooves
Grooves let you edit swing. By default every step gets 6 'tics' of time. If you have a 2-step groove table for instance, you can set the first one to 6 asnd second one to 5, and get a sort of herky-jerky swing going on for that phrase.

# Text Walkthrough, using starter project

When you start LPGT, the first thing you see is the project selection screen.
You can select what project you would like to work on, or create a new one. All projects are folders, starting with lgpt.
The installation archive contains two projects: one with an existing song called 10k, and an empty one called New.

Open up the 10k project by using the up and down arrows to highlight the project, and pressing a to load it.
When you do this you’ll be transported to the Song screen. This is where you organize your patterns into songs. Since LittleGPTracker is a tracker, it uses a vertical timeline. Horizontally you have one column per channel, and vertically you can see the sequence of patterns - or chains as we will call them - in each channel.

To play a song, simply press the start button. Press start again to stop it.

You can navigate up/down/left/right and press start to play the song from the current cursor position, as well.

Notice that only the channels with chains on them are started. Empty slots, represented by a double dash (--), are not played on startup.

LittleGPTracker is organized around a set of screens. Screens are organized in a maplike fashion. If you take a look at the left side of the display, you will see a rectangle with letters in it. This rectangle is the screen map representation. Currently the ‘S’ letter should be highlighted, because we are in the Song screen.

To navigate to another screen, simply press the right shoulder button, and hit the direction which you would like to move, on the map.
For example, the Project screen (the letter P above the S on the map) is accessible by holding right shoulder and pressing up. To go back, we press the right shoulder and hit down.

There are two major differences between Little GP Tracker and conventional trackers.

First: A pattern does not include note data across all channels. For each step in the song screen, each channel has its own chain number containing data for that channel exclusively.

This makes it convenient if you want to reuse a drum pattern but want to alter the melody. All you need is to create the drum chain a couple times and create new ones for the melody. It makes building song structure a lot easier.

As you can see each chain is represented by a hexidecimal number from 00 to ff. 

The second difference is that a chain doesn’t directly contain note data. Rather, it will hold a collection of subpatterns, called phrases, that contain note data. The chain can be seen as a bigger block of notes that makes sense being repeated in a song.

For instance, let’s examine chain 0e in this song - open the song and go to the 0e chain on the far right channel. To edit this chain, you have to press right shoulder and right, to go to the Chain ( C ) screen.

The chain is a collection of phrases - in this case, four phrases - that are played one after the other sequentially. To see the contents of a phrase, highlight it and press right again. We’ll see the content of Phrase 1C.

Now you can see the note data. If you press play in a phrase screen, you’ll only hear the phrase going over and over. You can also go back to the chain screen and press start there to hear the whole block of patterns. If you want the start the chain from the last cursor position while being in either screen, just hit right shoulder and start at the same time.

Now let’s learn to create new material. Go to the end of the song and position yourself on an empty slot. To create a new empty chain, tap A twice. This will fill the slot with the first empty chain number. You can now press right shoulder and right to enter the chain. Create a new phrase using the same commands.

To enter a note simply press a. This automatically makes a note(c3) and assigns it to an instrument (0).
To edit the note or instrument, scroll to that value with the arrow keys, then press a and use the arrow keys. Going left/right changes the value by one: going up/down changes the value by ten.
To delete a note press a and b at the same time.

Once your phrase is completed, you can go to the chain and add a new phrase, add a new set of notes, etc., and so on, until you’re happy with it.

Littlegptracker also supports copy paste.

Press left shoulder and b at once, extend the block using the arrow keys, and then copy (b) or cut (left and a). To paste this data you just go to where you want to put the data, then press left shoulder and a.

Note that cutting in the song screen will shift the selection up or down around it.

You can also clone chains, phrases, instruments, and tables.

To clone, first have a copied version of the thing you want to clone. Select that with the arrow keys, hold the left shoulder and then press b, then a. This will clone what you have selected into a new chain: this way you can edit the new chain freely without affecting previous chains.

That's enough of a beginner walkthrough. If you want to know more, look at the quick guide part of this page, or look at the official LittleGPTracker documentation (linked at the top of this page).
