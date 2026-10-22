# Valeton GP200 & Reaper: Wet/Dry Recording & Re-amping Guide

This guide details how to simultaneously record a fully processed patch (Wet) and a raw guitar signal (Dry) using the Valeton GP200 as a USB interface in Reaper (macOS), and how to loop the dry track back through the hardware to tweak your tone live.

---

## 1. Hardware Connections
* **USB:** Connect the Valeton GP200 directly to your Mac via a USB cable.
* **Headphones:** Plug your headphones **directly into the GP200 headphones jack** (not the Mac) to ensure zero-latency monitoring.

## 2. Valeton GP200 On-Unit Settings
Navigate to **GLOBAL > USB Audio** on your GP200 hardware and apply these settings:
* **USB Mode:** Set to **Reamp** (or *Multi-channel 6-in/4-out* depending on firmware version). 
* **Rec Mode (L):** Set to **Wet** (sends the processed patch tone over USB Channel 1).
* **Rec Mode (R):** Set to **Dry** (sends the raw, clean DI guitar signal over USB Channel 2).

## 3. macOS Audio System Settings
Before launching Reaper, ensure the Mac operating system is recognizing all available channels:
1. Open the built-in Mac application **Audio MIDI Setup**.
2. Select **GP-200 Audio** from the left sidebar.
3. Under the **Output** tab, ensure the **Format** dropdown is set to **4 ch** (instead of 2 ch).
4. Under the **Input** tab, ensure the Format dropdown is set to **6 ch**. Close the app.

## 4. Reaper Audio Device Preferences
1. Launch Reaper and open Preferences (**Cmd + ,**).
2. Go to **Audio > Device** in the left sidebar.
3. Set **Audio System** to **CoreAudio**.
4. Set **Audio Device** to **GP-200 Audio**.
5. **CRUCIAL:** Make sure the checkbox *“Allow use of different input and output devices (legacy option)”* at the bottom is **UNCHECKED**. 
6. Set **Last Input** to Channel 4 or 6, and **Last Output** to Channel 4. Click **Apply** and **OK**.

---

## 5. Recording the Performance (Wet & Dry Simultaneously)
Create two separate tracks in your Reaper project layout:

### Track 1: "Guitar WET" (The Processed Patch)
* **Input Configuration:** Set to **Input: Mono > Input 1**.
* **Record Status:** Arm for recording (Red button on).
* **Monitoring:** Turn **Record Monitoring OFF** (Speaker icon off) since you hear the patch directly from the hardware.

### Track 2: "Guitar DRY" (The Raw DI Signal)
* **Input Configuration:** Set to **Input: Mono > Input 2**.
* **Record Status:** Arm for recording (Red button on).
* **Monitoring:** Turn **Record Monitoring OFF**.

*Press **Record** in Reaper. Track 1 will capture your full tone, while Track 2 captures the quiet, raw guitar strumming.*

---

## 6. Live Re-amping & Tone Sculpting (Post-Recording)
Once you have saved your take and want to experiment with changing the amp parameters, patches, or effects using the physical GP200 knobs:

1. **Unarm** both tracks so you don't accidentally record over them.
2. **Mute Track 1** (Guitar WET).
3. On **Track 2** (Guitar DRY), click the **Route / I/O** button.
4. **Uncheck** the box in the very top-left corner that says **Master send** (this prevents a distracting double-audio monitoring effect).
5. In the bottom section under **Audio Hardware Outputs**, click **<Add new hardware output...>** and select **3: Channel 3**. Close the routing window.
6. Highlight your recorded guitar region, toggle the **Loop** option on Reaper's transport bar, and press **Play**.

### The Result:
The clean guitar loop is now feeding straight back into the input stage of the GP200. With your headphones on, you can now change patches, swap amp models, or twist the physical gain and EQ knobs on the unit. You will hear the recorded performance morph live with direct audio feedback.
