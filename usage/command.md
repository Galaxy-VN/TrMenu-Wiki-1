---
description: '[] are required，<> are optional'
---

# Command

## Main

> The plugin's main command

* Name: `trmenu` `menu`
* Permission: `trmenu.access`

## List

> List loaded menus

* Permission: `trmenu.command.list`
* Arguments
    * &lt;Filter&gt;

## Open

> Open a specified menu

* Permission: `trmenu.command.open`
* Arguments
    * \[ID\]:&lt;Page&gt; Menu name and specified page index
    * &lt;Player&gt; Specify the player (by default is the command sender)
    * &lt;菜单Arguments&gt; The incoming menu arguments, can be used as variables
* 示例
    * `trmenu open Example BlackSKY` Open menu `Example` for player `BlackSKY`
    * `trmenu open Shop:3` Open menu `Shop`, page `3`, for yourself

## Reload

> Reload all menus

* Permission: `trmenu.command.reload`

## Template

> Create a menu quickly

* Permission: `trmenu.command.template`
* Arguments
    * &lt;Rows&gt; from `1` - `6`

## Action

> Test TrMenu Actions

* Permission: `trmenu.command.action`
* Arguments
    * \[ID\] Target (Player)
    * \[Action\] Action line
* Note
    * By default, the action results will be printed to the sender
    * You can hide it by adding `#` as prefix of the action line

## Item

> Items management

* Permission: `trmenu.command.item`
* Arguments
    * \[Method\] Type
        * toJson - Convert the item in hand to JSON text format
        * fromJson - Convert the JSON text to a item
        * save - save item to item repository
        * get - get item from item repository
        * delete - delete item from item repository
    * &lt;Value&gt;

## Sounds

> Preview sounds

* Permission: `trmenu.command.sounds`
* Arguments
    * &lt;Filter&gt;

## Debug

> Debug feature

* Permission: `trmenu.command.debug`

