*It's not a bug, it's a feature.*  
Overflow is also computation.

# Toroidic Attention

**Exploring a hypothetical solution by using bit overflow logic as an advantage.**

This project is an open-ended experiment in rethinking how neural computation could work beyond traditional 2D matrix constraints.

Instead of linear tensors and rectangular attention windows, I'm exploring **circular structures** — where memory wraps around, overflow is meaningful, and the "shape" of computation becomes dynamic.

<video autoplay muted loop playsinline controls filename="" src="./assets/video.mp4" width="500">Your browser does not support the video tag.</video>

Imagine:
- A 2D Matrix of for example 32 x 32, which are 32 node columns (nodes) and 32 node rows (lets call them layers)
- The 2D Matrix curving into a cylinder
- the cylinder curving into a ring shape (Toroid)
- A "fixed-width" toroidal memory pipe forming
- Each node only storing a tiny state — maybe 16 or 128 bits, depending on what it will perform
- Where the 2D Matrix would overflow, the toroid flips signals instead of breaking them
- Neighboring logic becomes the basis for attention, not full-matrix dot products.
  Therefore each node takes into account its neighboring nodes ([n-1]) and (layer[n+1])
- On each iteration, where the matrix would reach its bottom 32th row, it would continue with row 33
- As there is no layer 33, it continues with Layer 1 (or index[0])

I'm learning and building as I go. This isn't production code — it's a blueprint for a different way to think about AI.

PRs welcome. Thought experiments encouraged.
Commercial use? **Nope.** See license.
