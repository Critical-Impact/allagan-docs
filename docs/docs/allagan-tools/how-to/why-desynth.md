# Why is my craft list telling me to desynth?

When a craft list sources a material by desynthesis (or any other unexpected method), it's because of where that method sits in the list's **Ingredient Sourcing** order.

## Why this happens

A craft list resolves each material by walking down its ingredient sourcing list and using the first method that can obtain the item. It never loops back through the sources, so a single high-priority entry like **Desynthesis** can produce a solution that looks odd — but there's no way for the list to know what's "weird" versus a route you actually want.

New lists place **Desynthesis** low in the sourcing order by default. If you've been using Allagan Tools for a while, your existing lists likely still have it higher up, which is why they keep choosing it.

## See how items are being sourced

In the crafts window, use the **tree view** button to visualise the list. The tree shows how each item is sourced and where it sits in the dependency chain, making it easy to spot which materials are being routed through desynthesis.

## Fix it for the whole list

Move desynthesis lower in the sourcing order:

1. Click the **pencil icon** to edit the list's configuration.
2. Open the **Ingredient Sourcing** tab.
3. In the **Default Ingredient Sourcing** list, drag the **=** handle next to **Desynthesis** to move it below the methods you'd rather use.

The list re-resolves materials against the new order, so anything that has another valid source will now use it.

## Override a single item

If you do want to desynth a specific item, you don't need to change the list default. In the crafts window, each item has a **gear icon** in its settings column. Click it to override the sourcing for that item alone, leaving the rest of the list untouched.