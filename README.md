# minigame 2
## Devlog
1.In the ColorChange script, step 4 asked me to declare a new float named 'r' with a value of 1. I wrote private float r = 1.0f; because I remembered the variable format as: modifier, type, name = value. But I got a compile error and the code wouldn't run. Unity said: The modifier 'private' is not valid for this item. The reason is that private only works on class-level member variables, but r is a local variable inside a method. It's only visible inside that method, so adding a modifier is meaningless. I removed private and changed it to float r = 1.0f;, and it worked.

2.I guess this line sets the chest's color. _spriteRenderer is the rendering component on the chest, .color accesses its color property, and = assigns the color on the right to it. new Color(r, 0.2f, 0.2f) creates a new color: red uses the current value of r, green and blue stay at 0.2. Since this line is inside the on-hit function, it runs every time the spell hits, and the chest changes color as r changes.

## Open-Source Assets
- Pixel art environment & character sprites: https://assetstore.unity.com/packages/2d/environments/pixel-art-top-down-basic-187605
