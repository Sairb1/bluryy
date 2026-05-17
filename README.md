<div align="center">

<img width="1774" height="887" alt="ChatGPT Image May 17, 2026, 01_34_49 PM" src="https://github.com/user-attachments/assets/0c3bd6d7-a0cb-412e-85ca-105a4c4969bb" />

<img src="https://img.shields.io/badge/BlurryAnimations-v2.9-blueviolet?style=for-the-badge&logo=android" alt="BlurryAnimations"/>
<br/>
<img src="https://img.shields.io/badge/ColorOS%20%7C%20OOS16-Supported-brightgreen?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Root-Magisk%20%7C%20KernelSU-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Telegram-colorosmodules-blue?style=for-the-badge&logo=telegram"/>

# ✨ BlurryAnimations

**Enable system-wide Blur, Animations & Wallpaper effects on ColorOS / OxygenOS 16**

Made with ♥ by **[Ayan (@imnotaino)](https://t.me/imnotaino)**  
Updates & Support → **[t.me/colorosmodules](https://t.me/colorosmodules)**

</div>

---

## 📖 What is this?

**BlurryAnimations** is a Magisk / KernelSU module that unlocks and enhances the blur, animation, and wallpaper rendering pipeline on **ColorOS** and **OxygenOS 16** devices.

Out of the box, many of these effects are either disabled by the OEM or gated behind feature flags. This module surgically patches the right system properties and extension configs — **without touching system files directly** — so you get a smooth, premium-feel UI experience.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🌫️ **Background Blur** | Enables SurfaceFlinger background blur and Gaussian blur effects |
| 🎞️ **Smooth Animations** | Unlocks OPLUS animation level 2 for fluid UI transitions |
| 🖼️ **Wallpaper Effects** | Enables live wallpaper zoom animation and OOS16 wallpaper rendering |
| 🎨 **Dynamic Blur** | SystemUI dynamic blur for notification shade and recents |
| 🔲 **Rounded Corners** | Enables vendor display rounded corner rendering |
| 🚀 **Non-destructive** | All changes are applied via Magisk overlay — safe to remove anytime |

---

## 📦 What it patches

The module mounts and patches only **two partitions**:

- `/my_product` — OEM extension configs (blur & animation feature flags)
- `/my_stock` — Stock system props

It does **not** touch `/system`, `/vendor`, `/odm`, or any other partition.

---

## 📋 Requirements

- Android device running **ColorOS** or **OxygenOS 16**
- [Magisk](https://github.com/topjohnwu/Magisk) `v20.4+` **or** [KernelSU](https://github.com/tiann/KernelSU) `v0.6.6+`
- Unlocked bootloader

---

## 🚀 Installation

1. Download the latest `.zip` from [Releases](https://github.com/Sairb1/bluryy/releases)
2. Open **Magisk Manager** → Modules → Install from storage  
   *or* flash via **KernelSU Manager**
3. Select the downloaded zip
4. Wait for the installer to complete (it will display your device info during flash)
5. **Reboot**

> ⚠️ Do **not** flash in recovery — only Bootmode (Magisk/KSU) install is supported.

---

## 🖥️ Flash Preview

When flashing, the installer shows a live device info readout:

```
╔══════════════════════════════════════╗
║        BlurryAnimations Module       ║
║         for ColorOS / OOS16          ║
╚══════════════════════════════════════╝

  Developer : Ayan (@imnotaino)
  Channel   : t.me/colorosmodules

  Flash Time : 2026-05-17 13:37:42

──────────────────────────────────────
          ★  Device  Info  ★
──────────────────────────────────────
  Device  : OPPO Reno 11
  Codename: OP5B07L1
  Android : 14  (SDK 34)
  Build   : CPH2599_14.0.0.XXX
  OTA Ver : XXXX
  Kernel  : 5.15.123-android14
  Battery : 87%
──────────────────────────────────────

  ► Initialising flash environment...
  ► Verifying Magisk / KernelSU root...
  ► Mounting partitions (my_product, my_stock)...
  ► Extracting BlurryAnimations files...
  ► Applying blur & animation props...
  ► Patching OOS16 extension configs...
  ► Setting permissions...
  ► Cleaning up temp files...

══════════════════════════════════════
   ✓  BlurryAnimations Installed!
══════════════════════════════════════

  ➤  t.me/colorosmodules

  Made with ♥ by Ayan (@imnotaino)
```

---

## ⚙️ Props Applied

```properties
# Background Blur
ro.surface_flinger.supports_background_blur=1
ro.surface_flinger.media_panel_bg_blur=1
ro.oplus.gaussianlevel=2
ro.sf.blurs_are_expensive=0

# Animation Level
persist.sys.oplus.anim_level=2
persist.sys.oplus.systemui.dynamic_blur=true
ro.oplus.animationlevel=2

# Wallpaper & Effects
persist.sys.wallpaperanimation.enable=true
ro.oplus.ltw.ability_level=full
persist.sys.oplus.upgrade_anim_level=2
```

---

## ❓ FAQ

**Q: Will this work on AOSP / MIUI / OneUI?**  
A: No. This is built specifically for **ColorOS** and **OxygenOS 16** with OPLUS system props.

**Q: Is it safe to uninstall?**  
A: Yes. Disable or remove the module in Magisk Manager and reboot — all changes are reverted.

**Q: My blur looks choppy after install?**  
A: Make sure your ROM supports SurfaceFlinger blur (most OOS16/ColorOS builds do). A clean reboot usually fixes it.

**Q: KernelSU not working?**  
A: Requires KernelSU `v0.6.6+` (version code 11184+).

---

## 📢 Channel & Support

Join the Telegram channel for updates, new modules, and support:

> **[t.me/colorosmodules](https://t.me/colorosmodules)**

---

## 📄 License

This module is provided as-is for personal use.  
Credits: MMT-Extended framework by [Zackptg5](https://github.com/Zackptg5)

---

<div align="center">
<sub>Made with ♥ by Ayan (@imnotaino) • t.me/colorosmodules</sub>
</div>
