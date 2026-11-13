# Augmented-Mandolin
ECE 18 Senior Design Project 2023

The Augmented Mandolin was a senior design project developed by a 4 person student team. The motivation was to explore way technology could add to acoustic instruments without replacing or digitizing the sound. We spent several months prototyping a system of MCUs, Electromagnets, Amplifiers, Pickups, and Sensors to create the system shown below.

<img width="581" height="763" alt="Screenshot 2026-11-12 at 10 14 55 PM" src="https://github.com/user-attachments/assets/c2cdfd6c-7f7e-4826-b04f-5d7622ed1bb6" />

In the end we landed on a beaglebone microcontroller fitted with a bela cape (https://bela.io/), for super low latency audio processing, that took in input from individual pickups in the form of frequency reading, and input from a "trill" capacitive touch sensor (https://bela.io/products/trill-touch-sensors/) as the trigger and indicator for intensity. After synthesizing those two inputs the bela put out waveforms that matched the frequency to amplifiers designed by a prior project that powered electromagnets which were suspended above the corresponding strings. Creating a "sustain" 

In the end, we chose a BeagleBone microcontroller fitted with a Bela cape (https://bela.io/) for ultra-low-latency audio processing. The system took real-time frequency readings from 4 individual pickups, one pickup per doubled string, and output frequency-matched waveforms to the corresponding electromagnets suspended over the string, through custom amplifiers (developed by a previous team). o give the player real-time control over the effect's timing, intensity, and duration, we integrated a Trill capacitive touch sensor (https://bela.io/products/trill-touch-sensors/) as a trigger and controller. Together, this produced a sustained vibrato effect that used the mandolin's acoustic body to naturally resonate and project.

This repository is the Pur eData code, which we used to detect input from the pickups convert that input into waveforms, detect input from the trill sensor, and then pass parameters to the amplifiers. 

The (01) Trill Control is the default patch we used for all demos, outputting a sine wave, the trill controls the depth of a vibrato effect on the strings
The Ramping Wave (03) and Square Wave (04) are similar to trill control but with different waveforms, there are in beta and haven't been fully fleshed out
Testing Patches (05) is where we stored the patches that allowed us to test each individual components

Short Video Demo using Patch (01) : [https://youtu.be/5ds4SkmchZo](url)

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

#



