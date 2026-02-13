# foo_mediacontrol
Adds the ability for foobar2000 to interact with the Windows 10 media control overlay.

## Screenshots

Screenshot of the Windows 10 Media Control overlay

![Display of the current track in Windows Media Control](./assets/screenshot-windows-media-control.png)

Screenshot of foobar2000 in your Discord status using
[**Music Presence**](https://github.com/ungive/discord-music-presence)

![foobar2000 in your Discord status using Music Presence](./assets/screenshot-music-presence.png)

## Development

### Building

Building requires Windows 10 SDK version 10.0.10240.0 or higher.

- Open the provided solution file in Visual Studio: `foobar2000/foo_mediacontrol/foo_mediacontrol.sln`
- Change the target to `Release` and platform to `x86`
- Build the solution
- Move the resulting `foo_mediacontrol.dll` to your foobar2000's components folder
- Restart foobar2000

### Debugging

- TODO Describe how to set the build directory to the foobar2000 component directory
- TODO Describe how to launch foobar2000 instead of the built DLL

### Updating the version

- Open `foobar2000/foo_mediacontrol/main.cpp`
- Change the version string to the new version

### Packaging

Build the project by opening Visual Studio and following these steps:

- Go to "Build" and click "Clean Solution"
- Select "Release" and "x86". Go to "Build" and click "Build foo_mediacontrol"
- Select "Release" and "x64". Go to "Build" and click "Build foo_mediacontrol"
- Wait until both builds completed successfully

Now open a command prompt and enter the following command,
presuming you have `make` installed:

```
make package
```

Alternatively you might want to use `nmake`,
if your `make` binary comes from a Cygwin/MSYS2 installation.

`fb2k-component` files for x86 and x64 will be in the `package` directory.

## License

[BSD-2-Clause](./LICENSE)
