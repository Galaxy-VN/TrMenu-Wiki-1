---
description: Perform actions when opening/closing the menu
---

# Events

## Usage

```yaml
Events:
  Open:
    - condition: 'perm *trmenu.use'
      actions:
        - 'sound: BLOCK_CHEST_OPEN-1-0'
      deny:
        - 'sound: ENTITY_ITEM_BREAK-1-0'
        - 'title: `&c&lPermission Required` `&7&lYou need permission &6&ltrmenu.use &7&lto open this menu` 15 20 15'
        - 'return'
  Close:
    - 'sound: BLOCK_CHEST_CLOSE-1-0'
```

## Note

* If action `RETURN` is executed，the open event will be cancelled
* You are not allowed to use `PAGE` action in the events  
  Here's an example if you wish to modify the opening page before the menu is opened
   ```YAML
   - condition: check player name is *Arasple
     action:
     - 'force-open: <MenuName>:1' # Open the specified page
     - 'return' # Cancel the current open event
     deny:
     - 'tell: Opening page 0'
   ```
