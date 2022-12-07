Player damage events happen when a player is damaged.
You can add damage events by adding your function to the tag `#smithed.damage:event/player/on_damage`.
This library tracks the type of damage dealt to the player and stores it as a string in data storage `smithed.damage:main io.damage.type`.
The following damage types are as follows:
* `'generic'`
* `'bypass_armor'`
* `'bypasses_invulnerability'`
* `'bypasses_magic'`
* `'is_explosion'`
* `'is_fire'`
* `'is_lightning'`
* `'is_magic'`

# Example Implementation
`function: example:damage_event`
```mcfunction
# give players with the fireproof tag fire resistance if they took damage by fire
execute if entity @s[tag=fireproof] if data storage smithed.damage:main {io.damage.type:'is_fire'} run effect give @s fire_resistance 10 0 true
```
`tag: #smithed.damage:event/player/on_damage`
```json
{
"values": [
"example:damage_event"
]
}
```