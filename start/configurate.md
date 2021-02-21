# Configurate

## Files

{% tabs %}
{% tab title="lang/en\_US.yml" %}
TLocale language file. You can edit most of the plugin's messages in it
{% endtab %}

{% tab title="data/globalData.yml" %}
The feature `global data` storage file
{% endtab %}

{% tab title="data/itemRepository.yml" %}
The feature `item repository` storage file
{% endtab %}

{% tab title="menus" %}
Default menu loading path
{% endtab %}

{% tab title="settings.yml" %}
TrMenu's main settings file
{% endtab %}
{% endtabs %}

## Settings

{% code title="settings.yml \(v3.0 BETA-2\)" %}
```yaml
#
# Plugin's options
#
Options:
  #
  # The language you want to use
  #
  Language: en_US

#
# Loading menu
#
Loader:
  # Custom loading paths
  Menu-Files:
    - 'plugins/CustomMenusFolder'

#
# Menu settings
#
Menu:
  Settings:
    # The minimum interval for the bound item to trigger
    Bound-Item-Interval: 3
  Icon:
    # Whether sub-icons should inherit the main icon by default
    Inherit: false
    # Display part
    Item:
      Default-Name-Color: "&7"
      Default-Lore-Color: "&7"
      # If enabled, plugin will first replace the color and then process the functions
      Pre-Color: false


Action:
  Inputer:
    Cancel-Words:
      - 'cancel|quit|end'
      - 'q'

Shortcuts:
  Offhand: []
  Sneaking-Offhand:
    - condition: 'perm *trmenu.shortcut'
      execute: 'open: Example'
      deny: 'return'
  Right-Click-Player: 'open: Profile'
  Sneaking-Right-Click-Player: [ ]
  PlayerInventory-Border-Left: [ ]
  PlayerInventory-Border-Right: [ ]
  PlayerInventory-Border-Middle: [ ]

RegisterCommands:
  openMenus:
    aliases: [ ]
    permission: null
    execute:
      - 'tell: &7Argument `example` Required!'
    arguments:
      example: 'open: example'
```
{% endcode %}



