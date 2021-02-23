---
description: Bind the menu to commands or items
---

# Bindings

## Usage

```yaml
#
# Ways to open the menu. 
#
Bindings:
  # Defines the commands used to open this menu.
  # Regex supported
  Commands:
    - 'tester'
  #  Defines the items which will open this menu when clicked.
  Items:
    - 'material:compass'
```

## 注意

* Binding commands support **regex**
* Binding commands will not be registered as real command
* To understand the syntax of **ItemMatcher**, please see the following wiki page:

{% page-ref page="../../usage/item-matchers.md" %}

