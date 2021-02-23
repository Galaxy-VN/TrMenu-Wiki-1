---
description: The menu layout is a major feature of TrMenu which allows you to quicly design menus easily (it looks better with items with a single character).
---

# Layout

## Usage

```yaml
Layout:
  - '########`Close`'
  - '         '
  - '         '
  - '         '
  - '########`Next`'

PlayerInventory:
  - '         '
  - '         '
  - '         '
  - '         '
```

* **Each character** represents an icon's position.
* You can also use icons with multiple characters if you surround them by \` `
* This defines the size of the menu at the same time
* The PlayerInventory feature, allows you to have 4 rows more in your menu by using the player's inventory!

## Multiples pages

```yaml
Layout:
  - - '########`Close`'
    - '         '
    - '         '
    - '         '
    - '########`Next`'

  - - '########`Close`'
    - '         '
    - ' *       '
    - '         '
    - '`Pre`########'
```

* You can also have multiples layouts (multiples pages) which you can then change with the `Page` action
* The PlayerInventory works alongside multiples layouts too!

## Note

* If a Layout doesn't have a corresponding PlayerInventory layout, then the player's inventory won't be used on this page  
