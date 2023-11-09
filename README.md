# Tauri + React

## Tauri setup:

### Rust installation:
```
winget install --id Rustlang.Rustup
```

### To create a new tauri app:
```
npm create tauri-app@latest
```

<hr />

## Running the tauri-draw-app locally:

### To install app dependencies:
```
npm i
```

### To run the app:
```
npm run tauri dev
```

### To build an executable:
```
npm run tauri build
```

After successful build, you should see the following output:

```
Finished 2 bundles at:
{PATH}\tauri-draw-app\src-tauri\target\release\bundle\msi\tauri-draw-app_0.0.0_x64_en-US.msi   
{PATH}\tauri-draw-app\src-tauri\target\release\bundle\nsis\tauri-draw-app_0.0.0_x64-setup.exe  
```

<hr />

### Build issues:

#### Reference: <a href="https://github.com/tauri-apps/tauri/discussions/3770">https://github.com/tauri-apps/tauri/discussions/3770</a>

1. 
```
Info Verifying wix package
Downloading https://github.com/wixtoolset/wix3/releases/download/wix3112rtm/wix311-binaries.zip
Error failed to bundle project: `https://github.com/wixtoolset/wix3/releases/download/wix3112rtm/wix311-binaries.zip: Network Error: timed out reading response`
```

Then, 
Download WixTools from <a href="https://github.com/wixtoolset/wix3/releases/download/wix3112rtm/wix311-binaries.zip">wix311-binaries.zip</a> and place the contents of `wix311-binaries` in `%LOCALAPPDATA%\tauri\WixTools`

2. 
```
Info Verifying NSIS package
Downloading https://github.com/tauri-apps/binary-releases/releases/download/nsis-3/nsis-3.zip
Error failed to bundle project: `https://github.com/tauri-apps/binary-releases/releases/download/nsis-3/nsis-3.zip: Network Error: timed out reading response`
```

Then,
Extract <a href="https://github.com/tauri-apps/binary-releases/releases/download/nsis-3/nsis-3.zip">nsis-3.zip</a> to `%LOCALAPPDATA%\tauri\NSIS`, <a href="https://github.com/tauri-apps/binary-releases/releases/download/nsis-plugins-v0/NSIS-ApplicationID.zip">NSIS-ApplicationID.zip/ReleaseUnicode/ApplicationID.dll</a> to `%LOCALAPPDATA%\tauri\NSIS\Plugins\x86-unicode` and <a href="https://github.com/tauri-apps/nsis-tauri-utils/releases/download/nsis_tauri_utils-v0.1.1/nsis_tauri_utils.dll">nsis_tauri_utils.dll</a> to `%LOCALAPPDATA%\tauri\NSIS\Plugins\x86-unicode`.



