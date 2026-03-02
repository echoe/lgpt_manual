# lgpt_manual
A Little GP Tracker Manual because the official one seems to be gone forever. This is mostly a transcription of a youtube video: https://www.youtube.com/watch?v=ejYSnCWLc6A .
I am planning to learn more about LGPT over the next month but we'll see. At the very least it'll be good to have a list of shortcuts for the program on the internet in text form ... somewhere.

# General Controls
-Arrow keys: Move around.
-Hold right trigger and the arrow keys to change pages. The map on the top left shows you where you are. Pages are: 

Project,           Groove
Song, Chain, Phrase, Instrument
                       Table,    Table

The groove and both tables aren't covered in this information.

-Press Start to start or stop the song. If you're in Chain or Phrase mode, it will play only that Chain or Phrase, unless you press start and right shoulder at the same time, then it’ll play the song from that spot.
-To create a new chain or phrase, press A twice. This fills the slot with the first chain or phrase number. (Pressing A once just fills the spot with the 'default' chain/phrase/note/etc.)
-To edit a chain or phrase or instrument or note, select it with the arrow keys, hold a, and then move the arrow keys. Up/down moves by 10, moving right is +1, left is -1.
-To delete something, select it, then press A and B at the same time.
-To copy something, press left shoulder and B to go into selection mode, move the selection with the arrow keys, and then press either B (copy) or left shoulder again and A (cut).
-To paste copied or cut data, press left shoulder and A at the same time.
-To clone data, select the data you want to clone, hold the left shoulder, and press b and then a. This will 'clone' that information into a new chain, and you can edit it without affecting the previous chain you had.

# Walkthrough

When you start the program, the first thing you see is the project selection screen.
You can select what project you would like to work on, or create a new one. All projects are folders starting with lgpt.
The installation archive contains two projects: one with an existing song called 10k, and an empty one called New.

We recommend you open up the 10k project. Use the up and down arrows to highlight the project and press a to load it.
When you do this you’ll be transported to the Song screen. This is where you organize your patterns into songs. Since LittleGPTracker is - well - a tracker, it uses a vertical timeline. Horizontally you have one column per channel, and vertically you can see the sequence of patterns, or chains as we will call them, play in each channel. To play a song, simply press the start button. Press start again to stop it.

You can navigate up/down/left/right and press start to play the song from the current curser position, as well.

Notice that only the channels with chains on them are started. Empty slots, represented by a double dash (--), are not played on startup.


As we mentioned earlier, LittleGPTracker is organized around a set of screens. Screens are organized in a maplike fashion. If you take a look at the left side of the display, you will see a rectangle with letters in it. This rectangle is the screen map representation. Currently the ‘S’ letter should be highlighted, because we are in the Song screen.

To navigate to another screen, simply press the right shoulder button, and hit the direction which you would like to move, on the map.
For example, the project screen (the letter P above the S on the map) is accessible by holding right shoulder and pressing up. To go back, we press the right shoulder and hit down.

There are two major differences between little GP Tracker and conventional trackers.
-A pattern does not include note data across all channels. For each step in the song screen, each channel has its own chain number containing data for that channel exclusively.

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
