# BlackHole and GarageBand are enough. You route the browser's audio into BlackHole and record from it in GarageBand.

1. Create a Multi-Output Device (so you can still hear the song)

Open Audio MIDI Setup (Spotlight → "Audio MIDI Setup").
Click + at the bottom left → Create Multi-Output Device.
Tick BlackHole 2ch and your speakers or headphones (e.g., MacBook Speakers).
Set your speakers as the Primary Device (the master clock), then tick Drift Correction on BlackHole 2ch.
Set the format to the same sample rate on every device, ideally 44.1 kHz for music or 48 kHz if that's what your devices default to.

2. Send the browser audio to it

Go to System Settings → Sound → Output and choose the Multi-Output Device.
The Mac's volume keys won't work on a Multi-Output Device, so set the volume in the browser or player instead. Keep it at 100% for the cleanest capture.

3. Record in GarageBand

Create a new project with an Audio → Microphone track.
Open GarageBand → Settings → Audio/MIDI and set Input to BlackHole 2ch. Leave Output as your speakers.
On the track, turn off input monitoring (the little "Monitor" icon) or you'll get echo or feedback.
Start playback in the browser, then press Record (R) in GarageBand. Stop both when the song ends.
Trim the silence at the start and end if you like.

4. Export as MP3

Share → Export Song to Disk… → choose MP3, pick the highest quality (320 kbps), and save.
If you want a lossless copy first, choose AIFF or WAV instead. You can convert that to MP3 later.

About "exact quality"

The recording captures the audio your Mac decodes, at the sample rate you set. It is not a copy of the source file.
A streaming source (YouTube, Spotify web, and so on) is already compressed, so the capture can't be better than that source.
MP3 encoding then compresses it again. If you want to keep the maximum quality, save the WAV or AIFF and make an MP3 only for convenience.

Also, only record songs you have the right to copy for personal use, since many streaming services' terms restrict this.

When you're done, switch the Mac's output back to your normal speakers, so your audio isn't still routed through the Multi-Output Device
