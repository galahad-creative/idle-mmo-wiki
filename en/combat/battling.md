# Battling

Once you've located a mob, you can start a battle by selecting an enemy and clicking `Battle`. You may only select one enemy at a time to battle.

---

### Battle Mechanics

Here’s how it works: after selecting an enemy to battle, your character will keep fighting through the entire stack of enemies until one of three things happens:

- Your character gets defeated (meaning they’ve run out of effective health).
- Your character defeats all the enemies in the stack.
- Your character reaches its maximum idle time, which is determined by its `Main Character` status and membership subscription.

When a battle begins, the UI will show you the following key information, so you can track how well your character is performing during the fight:

- Your characters hit chance
- How much damage your character deals per hit
- How much damage your character receives per hit
- How many hits you need to defeat the enemy
- The enemies hit chance
- How many enemies you have already defeated according to the time that has elapsed
- How many enemies you have left to defeat

>!banner All of the above values are dependent on your stats, equipment, the enemies stats, and the food you brought with you.

---

### Food

Before starting a battle, you can choose various food items to take with you. These items increase your overall **effective health**, allowing you to fight for longer.

For example, if your character has **100** HP and you bring **20** food items, each adding **10** HP, your total effective health becomes **300** HP `(100 + (20 * 10) = 300)`. With more effective health, you can take on more enemies without being defeated. If you bring enough food, you might even be able to fight all the way up to your character’s maximum idle time.

If you end a battle early, any unused food will be returned to your inventory. The system will attempt to prioritise using the weakest food items first. For example, if you have 1x **500** HP food item and 100x **100** HP food items, it will try to use the **100** HP items before the **500** HP item. However, this may not always happen exactly like this, as it depends on the battle and when you choose to stop it.

---

### Stance
Stance lets you choose which stat you want to focus on when earning EXP rewards after defeating an enemy.

Here are the five stances you can select:

**Balanced**: Obtains EXP for every primary stat. for instance, if you get 20 EXP, then each stat will get 5 EXP.\
**Offensive**: Obtains EXP only for `Strength`.\
**Defensive**: Obtain EXP only for `Defence`.\
**Agile**: Obtains EXP only for `Speed`.\
**Dexterous**: Obtains EXP only for `Dexterity`.

You can choose your stance when you start a battle, but you can't change it once the battle begins. If you want to switch stances, you’ll need to end the current battle and start a new one.

When you defeat an enemy, both your `Combat Level` and selected stats will increase. For example, if you earn 20 EXP from defeating an enemy, `20 EXP` will be applied to the stats based on your selected stance, and another `20 EXP` will be added to your `Combat Level`.

---

### Enemy Scaling

**IMPORTANT:** This feature is currently experimental and available only to characters with membership status for a limited time during testing.

Once a character reaches Combat Level **80**, they unlock the option to scale enemies to their level or higher.

#### Scaling Tiers

- **Level 80-99**: Characters can scale enemies up to their current level using a simple toggle switch
- **Level 100+**: Characters unlock advanced scaling with a slider, allowing them to scale enemies from their current level up to Level **150**

#### Benefits

Scaling enemies offers several benefits:

- **Improved loot** - loot increases based on how much the enemy is scaled. This boost is applied through a [Magic Find](/wiki/character/effects?same_window=true#magic-find) bonus to the character's battle session.
- **More EXP gains** - experience points are scaled to the selected level rather than the enemy's base level.
- **Greater challenge** - Level 100+ characters can scale enemies above their own level for additional difficulty and rewards.

#### Magic Find Calculation

The difference between the enemy's original level and the scaled level determines the loot boost amount - the greater the level gap, the larger the loot increase. Currently, the bonus magic find scales from **+0% to +40%**, depending on this distance. 

Examples:
- A Level 100 character scaling a Level 1 enemy to Level 100 receives a significant magic find boost
- A Level 100 character scaling that same Level 1 enemy to Level 150 receives the maximum **40%** magic find boost
- A Level 100 character scaling a Level 99 enemy to Level 100 receives minimal magic find boost (due to small level difference)

This scaling approach is designed to avoid major imbalances in loot frequency. The magic find bonus is proportional to the level difference between the enemy's base level and the scaled level, not the character's level.

[Magic Find](/wiki/character/effects?same_window=true#magic-find) only applies to the loot rates for each item, it does not apply to the chance of obtaining a drop. Scaling an enemy will not increase the "Chance of Loot" value.

---

### Notes

>!banner Taking a lot of food with you will increase your effective health, allowing you to battle for longer.


>!banner  Improving your stats with better equipment means you can defeat enemies faster and with less damage taken. This also means you don't need to use as much food - saving additional time and money.


>!banner Using the `Balanced` stance may result in less EXP if it cannot be divided evenly. For instance, if you defeat an enemy and you obtain `25 EXP`, that means each stat will get `6 EXP` totalling at `24 EXP` and the remaining `1 EXP` will be lost.


>!banner There is a limit of __8 seconds__  per enemy. It's not possible to defeat enemies quicker than __8 seconds__.


>!banner There is a minimum of _1 damage__ taken per battle. It's impossible to encounter a battle and leave unharmed.
