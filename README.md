# TheatriaEnchants Plugin

## Overview
TheatriaEnchants is a Minecraft plugin designed to introduce powerful, custom enchantments that can be fueled by Power Crystals. With TheatriaEnchants, players can imbue their tools with extraordinary capabilities. As players use their enchanted tools, the charge provided by the Power Crystals is consumed, gradually depleting until the tools return to their default abilities.

## Design Philosophies

### Modularity
The plugin architecture is designed around modular components which represent the enchantments. Instead of classes extending a specific tool type, classes extend a `TitanEnchant` abstraction, embodying behaviors granted by each enchantment.

### Separation of Concerns
The plugin separates its enchantments and tool handling, promoting better maintenance and extensibility. Each component in the plugin has its own purpose, be it handling tool usage, managing enchantments, or providing the link between tools and their enchantments.

### Performance Conscious
TheatriaEnchants aims to be performance-conscious, opting to use the Persistent Data Container (PDC) of the Paper/Spigot API for handling enchantment states and charge level of the tools. This eliminates the need for string manipulation on item lore, which is known to be less efficient.

### Extensibility
As each enchantment is a modular component, new enchantments can easily be added to the system without disturbing the existing structure. Similarly, new tool types can be introduced without having to redefine or reimplement enchantment behaviors.

## Features
1. Custom Enchantments: Enchant tools with custom, unique abilities, fuelled by Power Crystals.
2. Power Crystals: The fuel source that powers up enchantments on tools.
3. Persistent Storage: Use of Persistent Data Container (PDC) for efficient and consistent storage of tool states and charge levels.
4. Modular Enchantment Management: Each enchantment is a self-contained, modular component, allowing for easy expansion and modification of enchantment offerings.
5. Compatible with all major tools: Picks, shovels, fishing rods, hoes, and axes can all be enhanced with our enchantments.
