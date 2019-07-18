### On MAC/WIN10 Dual System, how to change touchpad scroll direction?

1. Open `Control Panel'. Search 'Mouse`. 
2. In `Hardware`, choose the device with location `on Apple Multi-Touch` by double-cliking or click `property`.
3. In `Details`, choose `Device Instance Path` property. Remember the `Value`.
4. Open `Register Editor`, choose `HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Enum/Value/Device Parameters`. Modify `FlipFlopWheel` into `1`.
5. Save and Reboot.
