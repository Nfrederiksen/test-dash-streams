# Gaming Stream Setup Guide (Twitch + OBS)

## 🔌 Hardware Setup
1. **Nintendo Switch → Elgato HD60 S+**
   - HDMI cable from Switch dock → *HDMI In* on Elgato.
   - HDMI cable from *HDMI Out* on Elgato → TV/monitor (passthrough).
   - USB 3.0 cable from Elgato → laptop.

2. **Canon 60D Camera**
   - Webcam mode: connect via USB, install Canon EOS Webcam Utility.
   - (Optional advanced) HDMI clean feed → Elgato with dummy battery.

3. **Audio**
   - Laptop’s built‑in mic for now.
   - Bluetooth headphones for monitoring (note: latency).

---

## 🖥️ Software Setup (OBS Studio)
1. Install OBS Studio (latest version).
2. Install Elgato drivers/software.
3. Add Sources:
   - **Game Capture:** Video Capture Device → Elgato HD60 S+ (1920×1080, 60 FPS).
   - **Camera:** Video Capture Device → Canon EOS Webcam Utility.
   - **Audio Input Capture:** Laptop mic.
   - **Audio Output Capture:** System audio (game sound).
   - **Banner:** Image source with “JBird” banner.

4. Scene Layout:
   - Scene 1: Gameplay + face‑cam overlay + banner.
   - Scene 2: “Starting Soon” placeholder.
   - Scene 3: “BRB” placeholder.

---

## 🎛️ OBS Configuration
1. **Output Settings:**
   - Encoder: NVIDIA NVENC (GTX 1650).
   - Bitrate: ~4500 kbps (upload speed 6.7 Mbps).
   - Rate Control: CBR.
   - Keyframe Interval: 2.
   - Preset: Quality.
   - Profile: High.

2. **Video Settings:**
   - Base (Canvas): 1920×1080.
   - Output (Scaled): 1920×1080.
   - FPS: 60.

3. **Audio Settings:**
   - Sample Rate: 48 kHz.
   - Mic: Laptop mic.
   - Desktop Audio: Elgato capture.

---

## 📡 Twitch Setup
1. Create Twitch account.
2. Get Stream Key:
   - Creator Dashboard → Settings → Stream → Copy Stream Key.
   - Paste into OBS: Settings → Stream → Service: Twitch → Input Stream Key.
3. Enable VOD storage: Settings → Stream → Store past broadcasts.
4. Alerts & Chat:
   - Use Streamlabs or StreamElements for alerts.
   - Add browser source in OBS for alerts overlay.
   - Optional: On‑screen chat overlay.

---

## 🧪 Testing & Go‑Live Checklist
1. Dry run: private stream with Twitch bandwidth test (`?bandwidthtest=true`).
2. Check audio balance: game vs. mic.
3. Check camera framing: overlay not blocking HUD.
4. Lighting: confirm exposure.
5. Network stability: 10‑minute test stream, monitor dropped frames.
6. Go live: Title stream, set category, hit “Start Streaming.”

---

## 🚨 Blind Spots
- Laptop mic = poor quality. Upgrade to USB mic ASAP.
- Bluetooth headphones = latency. Wired is better.
- DSLR batteries die fast. Get dummy battery.
- Upload speed borderline. If dropped frames, lower bitrate to 3500–4000 kbps or stream at 720p60.

---

## 🎯 Prioritized Next Steps
1. Wire up Switch → Elgato → laptop + monitor.
2. Install OBS + Elgato drivers.
3. Add sources (game, camera, mic, banner).
4. Configure OBS output (NVENC, 4500 kbps, 1080p60).
5. Get Twitch stream key, paste into OBS.
6. Run test stream, adjust audio/video balance.
7. Go live.
