# Sleep

On macOS, this command:

```bash
sudo pmset -a disablesleep 1
```

**disables system sleep** on the Mac.

* `sudo` → run with administrator privileges
* `pmset` → macOS power-management utility
* `-a` → applies to **battery, charger, and UPS** power modes
* `disablesleep 1` → prevents the Mac from entering sleep

### To turn it back on

```bash
sudo pmset -a disablesleep 0
```

### Check current setting

```bash
pmset -g
```

Look for:

```text
disablesleep 1
```

**Note:** This can keep your Mac running even when the lid is closed, but it doesn't necessarily prevent every form of power-state change (such as shutdown or hibernation).

