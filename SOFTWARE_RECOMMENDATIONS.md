# Recommended Software for moonchip

## Development Tools ✅ (Runs Great)
- **VSCode** / Neovim — Full IDE experience, no issues
- **Git, Node.js, Python, Rust, Go** — All compile and run fine
- **Docker** — Works well for containerized dev
- **PostgreSQL, SQLite, Redis** — Local databases no problem
- **Blender (Scripting)** — Python scripting is fine; 3D rendering has limits

## Media & Content Creation

### ✅ Excellent on moonchip
- **GIMP** — Image editing, lightweight, handles Photoshop-like tasks
- **Krita** — Digital painting, very responsive
- **Audacity** — Audio editing, recording, mixing (no issues)
- **OBS Studio** — Streaming/recording, works smoothly
- **FFmpeg** — CLI video processing (can be slow for large files, but works)
- **Inkscape** — Vector graphics
- **DaVinci Resolve (Free)** — Video editing, color grading (see limits below)

### ⚠️ Works but with Limitations
- **Blender 3D** — Can render, but slowly (see limits)
- **Storyboarder** — Web-based tool, works great for storyboarding
- **Shotcut** — Lightweight video editor (better than DaVinci on this CPU)
- **Kdenlive** — Lightweight video editor, faster than DaVinci

### ❌ Not Practical
- **Premiere Pro, After Effects** — Not on Linux anyway
- **4K Video Editing** — Too heavy for this CPU
- **Real-time 3D VFX** — Won't be smooth

---

## Hardware Limitations & Workarounds

### Your Specs
- **CPU**: Intel i5-8365U (4 cores / 8 threads @ 4.1 GHz max)
- **RAM**: 15 GB
- **GPU**: Integrated Intel UHD Graphics (no discrete GPU)
- **Storage**: 477 GB SSD (good speed, limited space for video)

### What This Means

| Task | Reality | Workaround |
|------|---------|-----------|
| **1080p Video Editing** | ✅ Smooth in Shotcut/Kdenlive | Use proxy editing for complex timelines |
| **4K Video Editing** | ❌ Too slow, will lag | Downscale to 1080p or use external GPU |
| **Blender 3D Rendering** | ⏳ Very slow (hours for complex scenes) | Use cloud rendering (Gumroad, Sheepit) |
| **Storyboarding** | ✅ Perfect (web-based, lightweight) | No limits |
| **Audio Production** | ✅ Full DAW capability | Audacity or lightweight DAWs |
| **Photo Batch Processing** | ✅ Works great | GIMP can automate with scripts |
| **Game Development** | ⚠️ Limited (Godot/Unity playtest fine, dev is OK) | Avoid heavy real-time features |
| **Docker + Dev** | ✅ Works fine | Keep containers lean, one or two at a time |
| **Video Codec Work** | ⏳ Slow | x264 is slow; x265 (HEVC) is slower |

### Storage Warning
- **Video takes space fast**: 1 hour of 1080p ≈ 100-300 GB (depending on codec)
- **Current free**: ~470 GB total (no room for error)
- **Recommendation**: External SSD (500GB+) for media projects
- **Project structure**: Keep raw footage on external drive; projects on internal SSD

### RAM Considerations
- **15 GB is OK** for most work
- **Blender large scenes**: Will swap to disk (slow)
- **DaVinci Resolve**: Fine for 1080p; 4K will be sluggish
- **Running many tools**: Docker + VSCode + Firefox + media tool = ~8-10 GB used

---

## Recommended Software Stack for ahoy indie media

### Core Setup
```bash
# Development
sudo pacman -S code git nodejs python rust

# Video/Editing
sudo pacman -S ffmpeg kdenlive obs-studio

# Audio
sudo pacman -S audacity

# Graphics
sudo pacman -S gimp krita blender inkscape

# Extras
sudo pacman -S storyboarder  # or use web version
```

### Your Ideal Workflow
1. **Planning**: Storyboarder (web or Electron app) → store in moonchip repo
2. **Scripting**: VSCode → version control
3. **Filming/Recording**: OBS Studio for capture, FFmpeg for batch conversion
4. **Editing**: Kdenlive for video (faster than DaVinci on this CPU)
5. **Color/Audio**: Audacity for audio, DaVinci Resolve only if you need professional color work
6. **Graphics**: GIMP for effects, Krita for digital media

---

## Next Steps
- [ ] Install Firefox (browser)
- [ ] Install VSCode or Neovim (already have?)
- [ ] Install Kdenlive + FFmpeg for media work
- [ ] Get external SSD for raw video/media storage
- [ ] Test Storyboarder web version: https://wonderunit.com/storyboarder/

## Not Recommended (Won't Stop You, But Struggles)
- Real-time 3D animation (use Blender + render overnight)
- Professional color grading in 4K (use 1080p proxy)
- Heavy machine learning training (too slow; use cloud GPU)
- Game engine development (OK for small projects; big projects are slow)
