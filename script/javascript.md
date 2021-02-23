---
description: >-
  This section requires a certain Java / JavaScript or similar programming
  foundation to facilitate understanding
---

# JavaScript

## Objects

TrMenu’s JavaScript engine currently provides the following objects

* `bukkitServer`  Bukkit.getServer\(\)
* `utils`  me.arasple.mc.trmenu.module.internal.script.js.Assist.INSTANCE
* `player`  the player himself
* `session`  me.arasple.mc.trmenu.module.display.MenuSession

## Functions

TrMenu’s JavaScript engine currently provides the following functions

* `vars(String input)`  Replace the string with placeholders and inline functions
* `varInt(String input)` Perform the above operation and then convert it to Integer
* `varDouble(String input)` 

## Note

* TrMenu’s JavaScript will be pre-compiled and cached, aiming to improve performance, so all variables need to be processed through functions

## Assist Utils

{% embed url="https://github.com/TrMenu/TrMenu/blob/master/src/main/kotlin/me/arasple/mc/trmenu/module/internal/script/js/Assist.kt" caption="Assist.kt" %}

## Examples

* Check Permission
  * `player.hasPermission("perm")` 
* Check money
  * `utils.hasMoney(player, vars("%player_health%"))` 
* ...





