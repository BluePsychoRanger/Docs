| Input Name         | Input Type | Input Source | Input Objective/Path | 
| ---                | ---        | ---          | ---                  | 
| 'Amount of damage' | score      | @s           | smithed.damage       | 


This function applies the specified amount of damage in half-hearts to the executing entity,
respecting armor, the protection enchantment, and the resistance effect
```mcfunction
scoreboard players set @s smithed.damage 3          # Does 1.5 damage (3 half-hearts) to a player without any armor or resistance
function #smithed.damage:entity/apply/armor         # Apply the damage
```
To apply damage that bypasses armor or respects other enchantments, use their specific commands:
* [`function #smithed.damage:entity/apply`](../apply.md): Ignores armor, enchantments, and resistance
* [`function #smithed.damage:entity/apply/projectile`](projectile.md): Respects armor, protection, resistance, and projectile protection
* [`function #smithed.damage:entity/apply/explosion`](explosion.md): Respects armor, protection, resistance, and blast protection