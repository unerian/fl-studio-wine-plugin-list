After much searching, I found the fix and I'm currently using 32-bit VSTs with no problem that were formerly crashing my FL.

The bug is when FL tries to render the GUI of 32-bit VSTs. If you load in existing projects that use them the audio will play correctly, but crash if you click on the plugin to view its GUI and modify its parameters.

The fix is to modify the registry entry for each problem VST to have a `DWORD` key `BridgedExternalWindow` with value `1`. This ensures that instead of trying to render the VST GUI as a native FL Studio widget, it renders as an external window. These will be found under
```
HK_USERS 
    SOME NUMBER 
        Software 
            Image-Line 
                Shared 
                    Plugins 
                        Fruity Wrapper 
                            Plugins
```

SOURCE: Reddit user NineNinchNails

https://www.reddit.com/r/winehq/comments/s7mrqx/comment/kovtrcf

Go give them reddit gold or something
