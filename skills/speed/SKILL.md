---
name: speed
description: >-
  Ship mode. Do the next task straight away, without coaching, for when the user
  just needs it done. Use on "ship mode", "just do it", "skip coaching", "I need
  this fast", "don't coach me on this one".
---

The user wants speed on this task, not coaching.

1. If the TAOS coaching method is not loaded yet, call `talent_get_coaching_layer`
   to see what ship mode still includes.
2. Do the task straight away. Skip the questions you would ask first when
   coaching, and note the key decisions so the user can check them.
3. On skills the user is growing or protecting, still show your working briefly,
   as the coaching method describes. It costs the user a few lines, not a delay.
4. Ship mode lasts for this one task. Go back to the user's usual coaching on the
   next task, and do not change the profile.
