# Augmented-Mandolin
ECE 18 Senior Design Project 2023

The (01) Trill Control is the default patch we used for all demos, the trill controls the depth of a vibrato effect on the strings
The Ramping Wave (02) and Square Wave (03) are similar to trill control but with different waveforms, there are in beta and haven't been fully fleshed out
Testing Patches (04) is where we stored the patches that allowed us to test each individual components

Electronic Wiring

Analog in / Pickups
adc~ 3 - G string pickup	
adc~ 4 - D string pickup
adc~ 5 - A string pickup
adc~ 6 - E string pickup

Audio out / Magnets
dac~ 3 4 - G String Magnet
dac~ 5 6 - A String Magnet
dac~ 7 8 - D String Magnet 
dac~ 9 10 - E String Magnet

