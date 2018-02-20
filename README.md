Teleports admins/developer under the world when they disconnect.

If configured admins and developers will be teleported back to land and vanished after waking up.
Optionally admins and developers health, calories and hydration can be set to max upon waking up if enabled in the config.

## Permissions

- **underworld.blocked** -- Block admins/devs from using the plugin if they have this permission.

## Chat Commands

- **/uw save** -- toggles saving and stripping inventory on disconnect
- **/uw set `<x y z>`** -- sets your log out position. can specify coordinates. if accepted then they will be used instead
- **/uw reset** -- resets your log out position to be underground unless a position is configured in the config file
- **/uw wakeup** -- toggle waking up on land
- **/uw noclip** -- toggle auto noclip on reconnect
- **/uw g** -- teleport to the ground

## Configuration

All options can be configured per user. You can override the saving of inventories by disabling it in the config file.

Saved inventories will be deleted if you log out naked, but not if you log out dead.

A blacklist is available for specific items to not be saved via the config file. Use an itemid or shortname.

```json
{
  "Settings": {
    "Allow Save And Strip Admin Inventory On Disconnect": true,
    "Auto Vanish On Connect": true,
    "Blacklist": [
      "2080339268",
      "can.tuna.empty"
    ],
    "Default Teleport To Position On Disconnect": "(0, 0, 0)",
    "Set Health, Hunger and Thirst to Max": false
  }
}
```
