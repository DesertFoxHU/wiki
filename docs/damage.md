# Damage Calculations

## Melee Damage

Melee Damage only performed when a player attacks an enemy with<br>
the correct melee weapon<br>
Attacking with an empty hand will result in no damage nor hurt animation<br>

> 1. Start Damage = [Weapon's melee damage] + [Player's melee damage value]
> 2. Apply any additional damage from the weapon's logic (for instance: it's passive ability)
> 3. Iterate over perks and handle their effects
> 4. If the perks not changed the damage to crit then roll the chance to crit with [Player's crit chance] + [Additional chance from perks]
> 5. If it is a crit then notify perks then apply perks' logic again
> 6. Iterate over influences to apply their logic too on the damage
> 7. Reduce the damage by the monster's resistance (if it has resistance)
> 8. Damage the entity
> 9. Apply cooldown to the player (Attack Speed) 

## Ranged Damage

Ranged Damage only comes when a player shot arrow hits an entity<br>
not when a player launches an arrow<br>
The logic is split between launch and actual hit<br>

On Launch
> 1. Start Damage = [Weapon's ranged damge] + [Player's ranged damage value]
> 2. Iterate over perks and handle their effects
> 3. Apply any additional logic from the weapon
> 4. If the perks not changed the damage to crit then roll the chance to crit with [Player's crit chance] + [Additional chance from perks]
> 5. If it is a crit then notify perks then apply perks' logic again
> 6. Iterate over influences to apply their logic too on the damage
> 7. Handle some special perks (ex: Font Arrow)
> 8. Apply cooldown to the player (Attack Speed) 
On Hit
> 9. Get the damage from the launch
> 10. Apply any additional logic from the weapon
> 11. If it's the victim is the same as the shooter deal 0 damage and break the logic
> 12. Reduce the damage by the monster's resistance (if it has resistance)
> 13. Damage the entity, remove the projectile

## Defense

Defense is when instead of a monster a player receives the damage<br>
the source of the damage is not important<br>
It activates even when you fall or when you hit by an arrow<br>

> 1. If the damage comes from projectile and it is the victim cancel the logic and deal 0 damage
> 2. If the player is blocking with a shield then damage the item and reflect the damage to the source then break the logic
> 3. Summarize the armors' armor and defense value
> 4. Add [Player's defense value] to the logic
> 5. Reduce armor and defense by the monster's (if viable) ignore values (substraction but it can't result can't be lower than 0)
> 6. Get damage by [Damage - Armor] * [(100 - Defense)/100]
> 7. If player's health would fall below or equals to 0 then roll [Evasion] chance
> 8. (Optional) if evasion activated then half the damage
> 9. Iterate over perks and handle their effects
> 10. Iterate over influences to apply their logic too on the damage
> 11. Damage the player