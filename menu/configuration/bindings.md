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

* 绑定命令支持**正则匹配**，例如 添加 \(?i\) 前缀可以忽略大小写
* 绑定命令支持**空格 & 其它参数**，插件将自动匹配并读取玩家提供的真实参数
* 了解绑定 **物品特征** 的详细写法，请查看下面章节

{% page-ref page="../../usage/item-matchers.md" %}
