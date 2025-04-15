# H4rml3ss
Hardware List:

Compute:
Raspberry Pi Model 5, 8GB (2)
Raspberry Pi Model Zero 2 W

Display: 
5" Waveshare HDMI Screen (pulled from parts bin)
Vufine HMD
Waveshare LED Matrix Panel (2)

Inputs:
Arducam IR USB Camera
USB GPS Dongle
USB C Conference Mic
3.5mm lapel mic

Audio Devices: 
USB Audio Adapter (Mic and Speaker)
PiAudio Hat
Portable Audio Splitter/Mixer

Audio Outputs:
Helmet Speakers 3.5mm 
External Portable Speakers

HID:
Wireless Keyboard/Mouse Combo

Miles of off the shelf glow cables.

-------

Compute Summary:
H4rml3ss' systems are spread across 3 different compute units.  Each is responsible for certain features, as described below:

Compute Unit 1:

Designation: Inner Mind

Type: RPi 5 8GB

Primary Task: HUD w/IR Camera and GPS details

Secondary Task: Personal Audio (EXT Mic and INT Speakers)

Software Repo for Tasks: https://github.com/h4rml3ss-actual/protogen-hud

Notes: HUD is designed using OpenCV.  Current implementation is a bit choppy on video performance, working to improve.


Compute Unit 2:

Designation: Outer Mind

Type: RPi 5 8GB

Primary Task: Drive the Mental Association Display Unit

Secondary Task: Speech amplification and modulation (INT Mic, EXT Speakers)

Software Repo for Tasks: https://github.com/h4rml3ss-actual/protogen-thought-display

Notes: See repo for code and writeup on how the software works.  Needs re-working to get the time between speaking a word and showing an animation.  Also, lowering latency on the audio moduluation by swapping from SOX to something else.


Compute Unit 3:

Designation: Expressions Unit

Type: RPi Zero 2W

Primary Task: Audio visualizer on LED Matrix Panels

Secondary Task: Play Gifs

Notes: Does what it is supposed to at current.  Will be implementing further features.  



-------
Silly little feature list:

Audio responsive LED Matrix Panels (They show a specific image based on the level of sound detected from my speech, along with a random gif at specified intervals from a folder on the Pi.)

Central Display Module: See write up for more details, but:

  - Runs in Cool Retro Term
  - Listens for a pre-defined word bank
  - Upon detection of a trigger word, plays a gif from that folder
  - When none are detected, periodically shows an idle message or plays an animation.

HUD: It's a HUD, on a Vufine.

  - GPS stats/simple compass indicator
  - System Stats
  - Detected Wireless Networks
  - Audio visualizer
  - Integrated audio listening/playback while HUD is running

Voice Modulator/Amp (Uses SOX or Easy Effects)



