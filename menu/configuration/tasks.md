---
description: Custom tasks executed at the set interval for the time when the menu is opened
---

# Tasks

## Usage

```yaml
#
# Custom menu periodic tasks
#

Tasks:
  # Task identifier
  tikTok:
    # Execution interval (In Ticks)
    period: 20
    # Actions executed
    task:
      - requirement: 'isOperator.'
        actions:
          - 'sound: BLOCK_NOTE_BLOCK_BIT-1-2'
```

## Note

* Each task is made of 3 parts: the identifier, the interval, and the reaction
* After opening the menu, all tasks will start and then stop when the menu is closed

