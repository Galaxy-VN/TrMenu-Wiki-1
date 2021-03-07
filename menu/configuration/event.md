---
description: 对菜单的一些事件执行条件动作反应
---

# Event

## Usage

```yaml
Events:
  # Menu open event
  Open:
    - condition: 'perm *trmenu.use'
      actions:
        - 'sound: BLOCK_CHEST_OPEN-1-0'
      deny:
        - 'sound: ENTITY_ITEM_BREAK-1-0'
        - 'title: `&c&lPermission Required` `&7&lYou need permission &6&ltrmenu.use &7&lto open this menu` 15 20 15'
        - 'return'
  # Menu close event
  Close:
    - 'sound: BLOCK_CHEST_CLOSE-1-0'

```

## Note

* If the `return` action is executed, the event will be canceled. You can see that we use this in the open event of the example in the deny commands of the condition. This way, if the player doesn't meett the condition, it won't open the menu.

