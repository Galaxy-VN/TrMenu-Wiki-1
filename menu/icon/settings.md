---
description: Icon Settings
---

# Setting

## Update

* Update interval for animated texture, name, lore, and slots

```yaml
# Same interval for all four properties
update: 20
```

```yaml
# Incomplete setting
# Here, only the material, name and lore are set to: 20, -1, 15
# The slot update interval will be set to the highest of the defined values, in this case: 20
update: [20, -1, 15]
```

```yaml
# Complete setting, the numbers will match in the same order the: Material, Name, Lore and Slot
update: [-1, 5, 25, 30]
```

* If the update interval is not set, the icon won't update at all
* Sub icons do not support custom update intervals
* In most cases, you can rest assured to use the first type of setting, the plugin will automatically determine the properties that need to be updated

## Refresh



* This property works only if there are any sub icons.
* During which the icon will recalculate by priority and display the first one which meets condition
* You can also use `refresh` action to refresh specific icon

```yaml
refresh: 20
```

## Slots

* For icons with static slots, it is recommended to define the icon slots through **layout**
* Manually configuring this property will overwrite the layout slots

```yaml
slot: 6
```

```yaml
slots:
 - 1
 - 2
 - 3
 # 4-6 = [4, 5, 6]
 - '4-6'
 - '${js: varInt("%player_health%")}'
 - 7
```

```yaml
# Animated slots
slots:
- - 0
  - 1
- - 1
  - 2
- - 2
  - 3
```

## \* Inherit

```yaml
inherit: true
```

* Every sub icon will inherit the material of the default icon whether configure or not
* By enabling this, sub icons will also inherit **name** and **lore**
* You still can configure sub icons' individual properties

## \* Condition

Sub icon may only be displayed when the result of its condition calculation is true

```yaml
condition: 'perm *trmenu.use'
```

## \* Priority

Determine the weight of the sub-icon \(the order in which the sub-icons are filtered\)

```yaml
priority: 20
```

* If not set, the default priority will be **0**
* When refreshing sub-icons, the sub-icons are calculated in ascending order of priority until the condition is met, that is, the icon with the lowest priority is calculated first

When actually configuring the YAML file, this property is optional

The plugin will automatically assign a certain priority in order according to the "configuration position" of the icon, for example

```yaml
Icons:
  'A':
    display:
      material: grass_block
    icons:
      - condition: 'perm *op'
        display:
          material: beacon
      - condition: 'perm *mvp.user'
        display:
          material: diamond block
      - condition: 'perm *vip.user'
        display:
          material: gold block
```

The sub icon with the condition of `perm *op` will be calculated first, and then `perm *mvp.user` , `perm *vip.user` in turn



