# testing

> [!IMPORTANT]
> **Electron 42 and newer**: As of Electron 42, the binary is no longer downloaded automatically during `npm install` ([release notes](https://github.com/electron/electron/releases/tag/v42.0.0)). You must download it explicitly before `add-electron-debug-identity` runs:
>
> ```json
> {
>   "scripts": {
>     "postinstall": "npx --no-install install-electron && winapp restore && winapp node add-electron-debug-identity"
>   }
> }
> ```
>
> The `--no-install` flag ensures `npx` only runs the `install-electron` bin shipped by your installed Electron package and never silently downloads anything from the registry. If you pin to Electron < 42, omit this step — the binary is already in place after `npm install`.

Now run `npm install` to trigger the postinstall script and configure the Windows environment:

```bash
npm install
```
