# FL STUDIO WINE VST PLUGIN COMPATIBILITY LIST
### This list is still work in progress, many plugins not tested. 
I though it would be useful to have this data in a single place instead of having to scour through forums and reddit.


I might change the rating system and other stuff later, didn't put too much thought into it tbh.

(as a sidenote, this is just my experience. I have found wine to sometimes be inconsistent between different machines and distros. You should expect a similar experience as listed here, but **your mileage may/will vary**.)

This list is specifically for running plugins with FL studio, so **it might not accurately apply to other software that also uses wine** (such as yabridge).

The installers for the plugins can often be as big of an issue as the plugin itself. For example, a plugin might work perfectly, but the installer may be broken. This is why **you might get differing results depending on if you use the official installer vs unofficial installers, such as pirated ones**. 


**All plugins tested on (unless stated otherwise):**

- Ubuntu 24.04.4 LTS x86_64
- GNOME 46.0 Wayland
- Bottles 63.2
- FL STUDIO 25.2.5 [5319]

**Bottles settings:**
- kron4ek-wine-11.6-staging-tkg-amd64
- DXVK-2.7.1
- vkd3d-proton-3.0
- latencyflex-v0.1.1

**Recommended:**
- ⭐ - Plugins I personally trust to work reliably

- ✅ - Recommended

- ➖ - Usable with caveats, read notes section

- ❌ - Not Recommended

  (Ratings based on the VST Plugins themselves, not the installing experience etc.)

**Testing:**
- High - Tested extensively, This plugin has been a part of my daily rotation, and I have used it for long periods of time 

- Medium - Tested for some time, but haven't put like 50+ hours of usage into it, so I cannot guarantee there isn't some rare instablility or bugs.

- Low - Basically just first impressions. Take these with a grain of salt.

## THE LIST

| Recommendation | Testing amount | Name  | Plugin Version  |Notes |
|------------|----|------------------------|--------|-------|
|     ✅⭐    |     High Testing |Vital            |   1.5.5     |    Pre wine 11 versions cause GUI flickering. Use wine 11 or newer  |
|     ✅⭐|     High Testing        |KHS Essentials Effects Pack            |   2.4.6     |    -  |
|     ✅⭐    |High Testing    |All Valhalla Plugins            |-|    [Some weird visuals with drop down menus on some plugins](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/valhalla_dropdown.png). Runs very stable generally.  |
|     ✅⭐    |High Testing    |Xfer OTT            |   1.37     |    Plugin window FPS is definitely lower than 60fps. Still works reliably   |
|     ✅|     High Testing        |Reveal Sound Spire                    |   1.5.19-x64     |    Use in "Detached" mode to avoid visual glitches with the plugin  |
|     ✅|     High Testing        |Devious Machines Infiltrator 2                    |   2.4.7        | -  |
|     ✅  | Medium Testing   |Melda MFreeFXBundle                    |   17.08     |    If your Melda Installer can't connect to the internet, try the offline installation, or run the installer with a different wine runner. I ran the installer with soda-9.0-1, and then switched back.   |
|     ✅  |  Medium Testing  |Fabfilter Bundle            |   4.10     |    Works fine, and I have also heard from others that these work well. Not much personal experience yet  |
|     ✅  | Medium Testing   |Output Portal                    |   1.0.1     |    Seems to work without issue, haven't done much testing yet though.  |
|     ✅  | Low Testing   |CableGuys ShaperBox 3                   |   3.6.0     |    Seems to work without issue, haven't done much testing yet though.  |
|     ✅  | Low Testing   |XLN Audio RC-20 Retro Color                   |   1.5.1     |    All installation methods were a bad experience. Eventually managed to get installed through the official installer. If it doesn't connect to the internet, make sure you don't have a VPN on, or try other wine runners. Plugin itself seems to work without issue, haven't done much testing yet though.  |
|     ✅  | Low Testing   |XLN Audio Addictive Keys                   |   1.7.3     |    See RC-20 for installer tips. Plugin itself seems to work without issue, haven't done much testing yet though.  |
|     ✅  | Low Testing   |XLN Audio Addictive Trigger                   |   1.7.3     |    See RC-20 for installer tips. Plugin itself seems to work without issue, haven't done much testing yet though.  |
|     ✅     | Low Testing  |Sonic Cat Purity            |   1.4.3    |     Plugin window FPS is definitely lower than 60fps. Seems to work fine otherwise.   |
|     ✅     | Low Testing  |Zynaptiq Pitchmap                    |   1.7    |[Plugin hover tooltips sometimes dont appear, and sometimes when they appear they get stuck on the screen for a bit](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/pitchmap_tooltip.png). Works perfectly otherwise     |
|     ✅    |Low Testing    |Oeksound Soothe2                    |1.1.2| Install mfc42 as a dependency if you get an error when launching the installer. Click the opengl checkbox in the settings to stop the plugin GUI from flashing |
|     ➖    |Low Testing    |Surge XT                    |1.3.4| Plugin runs smoothly and is stable. [Has an annoying bug where (at least on GNOME) submenus appear behind when they should be on top.](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/surge.png) Luckily there are other buttons to navigate the preset menu. |
|     ➖    |Low Testing    |Steinberg Hypersonic 2                    |2.0.0.600|   Plugin is 32bit -> [Requires changing a registry entry in wine](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/32bitfix.md) This plugin is very old and has instablility even on windows. Though funnily enough it seems to work better on wine |
|  ➖   |   Low Testing  |XLN Audio Addictive Drums 2                    |   2.9.0     | Plugin works, but takes a long time to open, and the UI is a bit sluggish.  Disabling OpenGL in UI&Scaling settings seems to make it more stable so its probably fine. Crashed on me once in like 5 minutes of using with OpenGL, hasn't crashed without it yet. Generally the older UI versions of XLN plugins work better, so I would prefer those. I think there is a version of addictive drums with that UI as well.   |
|     ➖   | High Testing |Soundtoys Bundle                    |  5.0.1 / 5.5.4     | Older versions of these (🏴‍☠️) seem to be a bit unstable, and crash frequently. The up to date VST3 versions seem to be much more stable, so if you are going to install, install them. |
|     ➖    |Low Testing    |Arturia Analog Lab V            |5.12.2|  [Whole plugin GUI flashes and flickers when interacting with or moving the plugin window](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/analoglab.md). Enabling "Detached" in the top left drop down menu of the FL wrapper fixes most of these issues. All sounds/other functionality seems to work fine and the plugin feels usable, just the flashing is an eyesore.   |
|  ➖   |   Low Testing  |Roland Zenology                    |   2.02     |    Takes 20 seconds to open, and freezes FL studio for that whole time. Same for deleting the plugin, but for 5 seconds. Plugin text seems to not have anti-aliasing, and generally looks uglier than on windows. Scaling the window by dragging the border is broken, and instantly snaps to the smallest size. Seems to work fine otherwise.    |
|     ❌    |Low Testing    |Xfer Serum 1                    |1.368|[Add dll override d2d1.dll (native) to stop FL from crashing when opening it](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/d2d1.png). I do not recommend doing this though, because it breaks a huge amount of other plugins. So only if you really need serum and dont care about other plugins |
|     ❌   | - |Xfer Serum 2                    |   2.0.23     |    Opening wavetable editor crashes FL. Wavetables, LFOs, Envelopes and filters have missing anti-aliasing and are laggy. Most other features work, but there is a general feeling of instability in the plugin.  |
|  ❌    |  -  |Antares AutoTune                    |   Various     |    Every version I've tried is very laggy. Takes a long time to open (like 20 sec), and the GUI is extremely laggy to the point its unusable. The audio processing itself seems to work.    |
|     ❌   | - |Modartt Pianoteq 9                    |   -     |    Crashes FL when opening  |







