# 📽️ Viral Video Studio: Documentary-Style Bhagavad Gita Short

A code-driven, automated video production pipeline built with [HyperFrames](https://hyperframes.heygen.com), GSAP, and Whisper.cpp. Produces viral 9:16 vertical shorts engineered specifically for Instagram Reels, YouTube Shorts, and TikTok algorithms.

---

## 🎬 Video Overview

- **Topic**: Bhagavad Gita 6.17 (*"Your energy is leaking, and the Gita says where..."*)
- **Format**: Vertical 9:16 (1080 × 1920) at 30 FPS
- **Duration**: 31.73 seconds
- **Aesthetic**: Ancient Indian museum diorama, warm cinematic lighting, "Objects, Not Faces" philosophy.
- **The Secret Sauce Overlay**: 7 binder punch holes down the left edge, vertical paper crease at 67%, fine paper grain, and subtle warm vignette.
- **Render Output**: [`Render_GitaSlokas/renders/final_output.mp4`](./Render_GitaSlokas/renders/final_output.mp4)

---

## 📁 Repository Structure

```
Project_Render/
├── README.md                          # Project documentation
├── .gitignore                         # Clean git ignore rules
├── script.txt                         # Full narration script
├── audio_files/                       # Original voiceover recordings
└── Render_GitaSlokas/                 # Master HyperFrames composition project
    ├── index.html                     # Entry point & paper overlay composite
    ├── meta.json                      # Project metadata (1080x1920, 30fps)
    ├── package.json                   # HyperFrames CLI scripts & pinned version
    ├── hyperframes.json               # Framework path configuration
    ├── script.txt                     # Narration copy
    ├── BGM_LICENSE.txt                # Music attribution & CC-BY 4.0 license
    ├── compositions/                  # Modular sub-scenes
    │   ├── scene1.html                # Shot 1: Cracked clay pot leaking water (0.00s - 3.76s)
    │   ├── scene2.html                # Shot 2: Palm manuscript + HTML verse card (3.76s - 12.32s)
    │   ├── scene3.html                # Shot 3: Brass balance scale (12.32s - 18.68s)
    │   ├── scene4.html                # Shot 4: Diya in midnight-blue room (18.68s - 28.80s)
    │   └── scene5.html                # Shot 5: Diya with ending question & CTA (28.80s - 31.72s)
    ├── assets/
    │   ├── audio_final.mp3            # Master mixed audio (-14 LUFS, ducked BGM, SFX)
    │   ├── voiceover.mp3              # Voiceover narration
    │   ├── bgm.mp3                    # Instrumental background score (Eastern Thought)
    │   ├── transcript.json            # Word-level Whisper timestamps
    │   ├── fonts/
    │   │   └── NotoSansDevanagari-Regular.ttf # Bundled offline Sanskrit font
    │   ├── images/                    # 9:16 museum diorama scene images (shot1.jpg - shot5.jpg)
    │   └── sfx/                       # Sub-bass boom & cut whooshes
    └── renders/
        └── final_output.mp4           # Final broadcast MP4
```

---

## 🛠️ How to Preview & Render

### Prerequisites
- Node.js (v22+)
- FFmpeg (v8+)
- Google Chrome

### 1. Previewing in Browser
Navigate into the project directory:
```bash
cd Render_GitaSlokas
npm run dev
```
Or start persistent agent-safe preview:
```bash
npx hyperframes preview --background
```

### 2. Linting & Quality Verification
Verify layout, contrast, and contracts:
```bash
npm run check
```

### 3. Rendering Final Video
To re-render the composition to MP4:
```bash
npm run render
```

---

## 🎵 Audio & License Details

- **Music**: *Eastern Thought* by Kevin MacLeod ([incompetech.com](https://incompetech.com))
- **License**: Creative Commons: By Attribution 4.0 International ([CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/))
- **Commercial Use**: 100% permitted for monetized YouTube & social media.
- **Mix Specifications**:
  - Target Loudness: **−14.2 LUFS**
  - True Peak: **−1.6 dBFS** (zero clipping)
  - Sidechain Compression: Ducked 18 dB below speech, rising to 10 dB below in pauses (60 ms attack, 500 ms release).
