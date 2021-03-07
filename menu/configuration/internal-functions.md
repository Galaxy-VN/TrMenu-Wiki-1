---
description: Custom JavaScript Functions which can be used as inline variable easily
---

# Internal Functions

{% hint style="info" %}
To use this function, you need some basic JavaScript knowledge
{% endhint %}

## Usage

```yaml
Functions:
  flash: |-
    function flash() {
      var display = new Date().getSeconds() % 2 == 0
      return display ? args[0] : "  "
    }
    flash()
```

## Note

* You can use `${[funcName]_[Arg1]_[Arg2]}` to get returned value by a custom function, e.g. ${flash\_&gt;}
* We provide `args` \(an Array of String\) which you can use the parameters from the identifier



#### Advanced Usage Example

```yaml
bStats:
  servers: 'vars("${bStats.query_servers_&a_&7 servers}")'
  players: 'vars("${bStats.query_players_&6_&7 players}")'
  menus: 'vars("${bStats.query_menus_&2_&7 menus}")'
  opens: |-
    function opens() {
      var data = utils.query("https://bstats.org/api/v1/plugins/5742/charts/menu_open_counts/data?maxElements=1")
      if (data.has()){
        return "&b" + data.asJson().getAsJsonArray().get(0).getAsJsonArray().get(1) + "&7"
      }
      return "&8Loading." + vars("${flash_.}") + "&7"
    }
    opens()
  query: |-
    function query() {
      var data = utils.query("https://bstats.org/api/v1/plugins/5742/charts/" + args[0] + "/data?maxElements=1")
      if (data.has()){
        return args[1] + data.asJson().getAsJsonArray().get(0).getAsJsonArray().get(1) + args[2]
      }
      return "&8Loading." + vars("${flash_.}")
    }
    query()
```

