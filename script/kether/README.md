---
description: Learning Kether within 10 mins
---

# Kether

## Basics

Kether is a new scripting language based on **actions** 

It has very simple logical and easy to understand for all beginners



You can use Kether in **TrMenu** for **condition** check & **reaction**

## Usage

1. Find the action you need to use
2. Understand the type of its parameters, for example, the parameter itself can also be an action
3. Use it correctly

## Example for conditions

* Check whether the player has  certain permission
  * We go search for action **permission** and understood it needs another action as its parameter, and it returns true or false
  * Permission should be string, so we use action **literal** to parse the permission
  * `permission literal custom.permission` 
  * To make this look **simpler** & **clean**, we use **aliases** of these actions
  * `perm *custom.permission` 



* Check whether the player has certain permission or have a certain item
  * To achieve this, we need action **any**, **permission** and **item**
  * `any [` **`perm`** `*test` **`item`** `*mat:diamond,amt:16 ]`



