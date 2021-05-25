# vog_oracles
### Audio processor to map oracle notes in the VoG raid in Destiny 2 to call outs.

Huge thanks to [mzucker](https://github.com/mzucker/python-tuner) on GitHub for the note detection code. Also thanks to [u/brainstormcsgo](https://www.reddit.com/r/DestinyTheGame/comments/njo9zl/had_a_bunch_of_people_asking_if_you_have_perfect/) on reddit for mapping the notes to call outs.

#### Requirements
Python 3.6, as pyaudio hasn't been updated since.

Game audio as PC input. On PC this should be trivial, on console I use my monitors output as an audio line in. I haven't tested using speakers from console and microphone, but it could work. Try to avoid routing VC with game audio, as this will make it harder to detect notes.

#### To use
Set ATHEON constant to true if in Atheon room, false for oracles/templar. Run script. Select audio input.

You will need to modify the constants for better results. DECIBEL_CUTOFF helps to isolate background noise, but if too high it will prevent proper note detection. Debug modes will help with fine tuning the constants.

You can change the note_to_location function to modify the callouts you want to use. By deafault it uses 1-7 left to right for oracles, and far/close left/middle/right for Atheon.

Recommend running in a termnial that you can easily clear, to get rid of any incorrect results between cycles.

#### Usefulness
Script is not perfect, but should help with missed calls, ordering etc. Works a lot better if you are able to isolate the oracle sounds, for example not firing weapons/using abilities.

I have not tested it as much in Atheon room, as you can't easily test it solo and there are less videos with good audio for it. Atheon room also has the issue of more sounds / less places to avoid damage, making note detection harder. If you sit on the ledge at the back it should work pretty well.

#### Improvements
1. Improvment to B flat detection
1. Better filtering out of non oracle sounds
1. Using both rotations of the notes to figure out call, instead of printing all

If anyone has any suggestions for improvments please let me know! I'm an average player and programmer, but have no music experience, so there are definetely improvments to be made!