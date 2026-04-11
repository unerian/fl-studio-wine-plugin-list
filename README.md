# FL STUDIO WINE VST PLUGIN COMPATIBILITY LIST
### This list is still work in progress, many plugins not tested. 
I though it would be useful to have this data in a single place instead of having to scour through forums and reddit.


I might change the rating system and other stuff later, didn't put too much thought into it tbh.

(as a sidenote, this is just my experience. I have found wine to sometimes be inconsistent between different machines and distros. You should expect a similar experience as listed here, but your mileage may still vary.)

This list is specifically for running plugins with FL studio, so it might not accurately apply to other software that also uses wine (such as yabridge).

The installers for the plugins can often be as big of an issue as the plugin itself. For example, a plugin might work perfectly, but the installer may be broken. This is why you might get differing results depending on if you use the official installer vs unofficial installers, such as pirated ones. 


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

- ✅ - Recommended

- ➖ - Usable with caveats, read notes section

- ❌ - Not Recommended

**Testing:**
- High - Tested extensively, This plugin has been a part of my daily rotation, and I have used it for long periods of time 

- Medium - Tested for some time, but haven't put like 50+ hours of usage into it, so I cannot guarantee there isn't some rare instablility or bugs.

- Low - Basically just first impressions.




## WORKS PERFECTLY 

| Recommendation | Testing | Name  | Plugin Version  |Notes |
|------------|----|------------------------|--------|-------|
|     ✅    |     High  |Vital            |   1.5.5     |    Pre wine 11 versions cause GUI flickering. Use wine 11 or newer  |
|     ✅|     High        |KHS Essentials Effects Pack            |   2.4.6     |    -  |
|     ✅|     High        |Devious Machines Infiltrator 2                    |   2.4.7        | -  |
|     ✅|     High        |Reveal Sound Spire                    |   1.5.19-x64     |    -  |
|     ✅  | Medium   |Melda MFreeFXBundle                    |   17.08     |    If your Melda Installer can't connect to the internet, try the offline installation, or run the installer with a different wine runner. I ran the installer with soda-9.0-1, and then switched back.   |
|     ✅  |  Medium  |Fabfilter Bundle            |   4.10     |    -  |
|     ✅  | Medium   |Output Portal                    |   1.0.1     |    -  |


## MINOR VISUAL GLITCHES

| Recommendation | Testing | Name | Plugin Version  |Notes |
|------------|----|------------------------|--------|-------|
|     ✅    |High    |All Valhalla Plugins            |-|    [Some weird visuals with drop down menus on some plugins](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/valhalla_dropdown.png?raw=true). Runs very stable generally.  |
|     ✅    |High    |Xfer OTT            |   1.37     |    Plugin window FPS is definitely lower than 60fps. Still works reliably   |
|     ✅     | Low  |Sonic Cat Purity            |   1.4.3    |     Plugin window FPS is definitely lower than 60fps. Seems to work fine otherwise.   |
|     ✅     | Low  |Zynaptiq Pitchmap                    |   1.7    |Plugin hover tooltips sometimes dont appear, and sometimes when they appear they get stuck on the screen for a bit. Works perfectly otherwise     |

## MAJOR VISUAL GLITCHES

| Recommendation | Testing | Name | Plugin Version  |Notes |
|------------|----|------------------------|--------|-------|
|     ➖    |Low    |Arturia Analog Lab V            |5.12.2|  Whole plugin GUI flashes and flickers when interacting with or moving the plugin window. Enabling "Detached" in the top left drop down menu of the FL wrapper fixes most of these issues. All sounds/other functionality seems to work fine and the plugin feels usable.   |

## REQUIRES TWEAKING WINE OR OTHER TRICKS
| Recommendation | Testing | Name | Plugin Version  |Notes |
|------------|----|------------------------|--------|-------|
|     ✅    |Low    |Oeksound Soothe2                    |1.1.2| Install mfc42 as a dependency if you get an error when launching the installer. Click the opengl checkbox in the settings to stop the plugin GUI from flashing |
|     ➖    |Low    |Steinberg Hypersonic 2                    |2.0.0.600|   Plugin is 32bit -> [Requires changing a registry entry in wine](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/32bitfix.md) This plugin is very old and has instablility even on windows. Though funnily enough it seems to work better on wine |
|     ❌    |Low    |Xfer Serum 1                    |1.368|[Add dll override d2d1.dll (native) to stop FL from crashing when opening it](https://github.com/unerian/fl-studio-wine-plugin-list/blob/main/other/d2d1.png?raw=true). I do not recommend doing this though, because it breaks a huge amount of other plugins. So only if you really need serum and dont care about other plugins |


## SLOW / VERY LAGGY
| Recommendation | Testing | Name | Plugin Version  |Notes |
|------------|----|------------------------|--------|-------|
|  ➖   |   Low  |Roland Zenology                    |   2.02     |    Takes 20 seconds to open, and freezes FL studio for that whole time. Same for deleting the plugin, but for 5 seconds. Plugin text seems to not have anti-aliasing, and generally looks uglier than on windows. Scaling the window by dragging the border is broken, and instantly snaps to the smallest size. Seems to work fine otherwise.    |
|  ❌    |  -  |Antares AutoTune                    |   Various     |    Every version I've tried is very laggy. Takes a long time to open (like 20 sec), and the GUI is extremely laggy to the point its unusable. The audio processing itself seems to work.    |

## UNSTABLE / UNRELIABLE / CRASHING
| Recommendation | Testing | Name | Plugin Version  |Notes |
|------------|----|------------------------|--------|-------|
|     ➖   | High |Soundtoys Bundle                    |   -     | Older versions of these (🏴‍☠️) seem to be a bit unstable, and crash frequently. The up to date VST3 versions seem to be much more stable, so if you are going to install, install them. |
|     ❌   | - |Xfer Serum 2                    |   2.0.23     |    Opening wavetable editor crashes FL. Wavetables, LFOs, Envelopes and filters have missing anti-aliasing and are laggy. Most other features work, but there is a general feeling of instability in the plugin.  |
|     ❌   | - |Modartt Pianoteq 9                    |   -     |    Crashes FL when opening  |



