# Effects

Effects in the game are modifiers that impact a character's attributes and abilities. These effects can vary widely, from beneficial boosts that enhance performance and rewards to harmful debuffs that may hinder progress.
### Types of Effects

Effects can be broadly categorized based on their duration:

- **Permanent Effects**: These are long-lasting changes that continuously affect the character. They remain active unless specifically altered or removed through gameplay mechanics.
- **Temporary Effects**: These effects have a time-limited impact on the character. They automatically expire when their duration reaches zero, after which the character returns to their normal state.

### Sources of Effects

Characters may acquire effects through various in-game mechanics, including:

- **Membership Perks**: Holding a membership grants a character a slight, yet consistent boost, enhancing their ability to earn rewards more efficiently. These effects will be removed when the membership status expires.
- **Class-Specific Bonuses**: Different classes may bestow unique effects and enhancements, particularly amplifying certain skills or attributes.
- **Potion Consumption**: Drinking potions can temporarily alter a character's abilities, offering either positive or negative effects depending on the potion's nature.
- **Gameplay Duration**: Extensive gameplay without breaks can lead to fatigue, resulting in negative effects due to exhaustion.

-----------
## Magic Find

Magic Find is a modifier that boosts your chances of finding higher-quality items from enemies. However, when Magic Find increases item drop rates beyond **100%**, adjustments are made to ensure a balanced system.

### How It Works

When you apply a Magic Find modifier, each item's drop rate increases based on its original percentage. For instance, with a **200%** Magic Find modifier, each item’s drop rate is tripled.

#### Example One

Let’s take an enemy with these base drop rates:

- **1%** Stick
- **5%** Food
- **15%** Recipe
- **70%** Collectable

Applying a __+100%__ Magic Find modifier to these rates doubles each item’s chance, resulting in:

- **2%** Stick
- **10%** Food
- **30%** Recipe
- **140%** Collectable

Now, because the total drop rate exceeds 100%, the system will trim the rates, starting with the most common items. This results in:

- **2%** Stick
- **10%** Food
- **30%** Recipe
- **58%** Collectable


#### Example Two

When the total item drop rates exceed **100%** and adjusting them still requires removing an item, the most common item is removed entirely.

For example, take an enemy with these base rates:

- **1%** Stick
- **4%** Food
- **40%** Recipe
- **55%** Collectable

With a **200%** Magic Find modifier, the modified rates are:

- **3%** Stick
- **12%** Food
- **120%** Recipe
- **165%** Collectable

Following our trimming process, the game starts with the most common item (in this case, Collectable), removing it to meet the **100%** threshold. The final drop rates become:

- **3%** Stick
- **12%** Food
- **85%** Recipe

Here, Recipe is adjusted to fit within the 100% limit, and Junk is removed entirely.


#### Additional Notes
- The magic bonus **does not** affect the UI in situations where loot chances are visible. For example, if you view an enemy that has a **30%** chance to drop a collectible item, this displayed value will not change, even if your character has a **200%** magic find bonus.

------------

## Exhaustion

Excessive gameplay, defined as engaging in more than __20 hours__ of active in-game actions within a single day, triggers an "exhaustion" effect. This effect imposes certain debuffs on the character, lasting for a period of __4 hours__. After the exhaustion effect wears off, the character's condition resets, and they can resume normal gameplay.

As of the time of writing, the current effects are applied:

- __-35%__ Dungeon EXP
- __-35%__ Skill EXP 
- __-50%__ Skill Efficiency
- __-50%__ Hunting Efficiency
- __-35%__ Battle EXP

A single day is `00:00am UTC` to `11:59PM UTC` and the limit will reset as soon as it hits `0:00am UTC`.

### Examples

Your character becomes "exhausted" after 20 hours of active playtime, beginning at `00:00 AM` and ending at `08:00 PM`. Once exhausted, this effect lasts for 4 hours, completing a 24-hour cycle. The exhaustion effect persists through the end of its 4-hour duration, even if a new day begins during this period.

Should you play while your character is exhausted, any playtime within the same calendar day does not count towards the next day's 20-hour active time limit. 

For instance, if your character reaches the 20-hour limit at `11:00 PM UTC`, they become exhausted until `3:00 AM` the following day. Playing between `11:00 PM` and `11:59 PM` on that same day won't affect the next day's active time. However, if you play after `12:00 AM`, this time will count towards the next day's 20-hour limit, even though your character is still under the exhaustion effect.

### Calculation

The game employs a straightforward method to calculate the net impact of various effects on a character's attributes. This is achieved by aggregating all the effects that apply to a particular attribute and then determining the final modified value of that attribute. Here's how it works:

#### Summation of Effects

All effects, whether positive or negative, are summed up to calculate the total impact. This total represents the net effect on the character's attribute.

#### Examples
##### Both Postive and Negative Effects
 Imagine a character is under the influence of a __+80%__ EXP boost effect and also a __-20%__ EXP effect. These effects are combined to give a final EXP boost of __+60%__. The calculation is simple: `+80% (positive effect) + -20% (negative effect) = +60% (net effect)`.

##### Equally Opposing Effects
In cases where a character experiences opposing effects on the same attribute, these effects can negate each other. For instance, if a character has a __+50%__ efficiency boost and a __-50%__ efficiency reduction, the net effect on efficiency is nullified. The final value for efficiency, in this case, would be __0%__, as `+50% + -50% = 0%`.

------------

## Efficiency
Efficiency dictates the speed of performing an action. An efficiency of 100% allows you to complete a 10-second action twice as fast, reducing the time required to 5 seconds.

However, its important to know that the rate of decrease diminishes as the efficiency grows – each additional percentage point of efficiency has a smaller impact than the last.

### Understanding Efficiency vs. Percentage Reduction in Time
Subtracting a percentage from a time value reduces that time by a certain fraction.

#### Examples
- **15% Percentage Reduction (100 Seconds):** Removing 15% from 100 seconds results in __85__ seconds. `(100 - 15% = 85)`
- **15% Efficiency Reduction (100 Seconds):** Being 15% efficient at a 100 second task results in __86.9__ seconds. `(100 / 1.15 = 86.9)`

#### Comparison
- **Efficiency** is about improving the speed of task completion. Higher efficiency means the character completes it faster. It doesn't directly affect the time value itself. Efficiency is all about how _efficient_ the character is at the task.
- **Removing a Percentage** directly decreases the duration of the time value.

### Formula

The formula used to calculate the final value based on efficiency is:

`Final Value = Initial Value / ((Efficiency Percentage + 100) / 100)`

#### Components of the Formula

- **Initial Value**: This is the starting point or the original value before any efficiency is applied. For example, it can be the time taken to complete a task without any efficiency.
- **Efficiency Percentage**: This is the percentage that represents how much more efficient the process is compared to the base efficiency. For example, 15% means 15% more efficient than the base.

#### Breakdown

1. **Adding 100 to Efficiency**: We start by adding 100 to the efficiency percentage. This is because a 100% efficiency in this formula means twice as fast as the normal speed. So, adding 100% ensures that our base (100% efficiency) doubles the speed.
2. **Dividing by 100**: We then divide this total by 100 to convert it into a multiplier. For example, 115% efficiency becomes 1.15 as a multiplier.
3. **Dividing the Initial Value**: Finally, we divide the initial value by this multiplier. This step calculates the final value after applying the efficiency. If the efficiency is high, the multiplier is larger, and thus, the final value is smaller, indicating a faster or more efficient outcome.

#### Examples
- **100% Efficiency**: With 100% efficiency, the formula becomes `Initial Value / 2`. This means the task is done twice as fast as the result is half.
- **300% Efficiency**: For 300% efficiency, the formula becomes `Initial Value / 4`. So, a task that initially took 100 seconds will now take only 25 seconds.

You can increase your efficiency by drinking [Potions](/wiki/learn-more/item-types), consuming [Essence Crystals](/wiki/learn-more/item-types) and obtaining equipment.

-----

### Applying Effects on Idle Actions

When a player initiates an action, like chopping wood or entering a dungeon, the game calculates the rewards immediately. This method is chosen for efficiency, as pre-calculating rewards is significantly faster than doing so during the action. This intentional design enables scalability for the game to accommodate unexpected levels of activity.

This system, despite its speed and ability to scale, comes with a slight trade-off. If a character receives any effects after starting an action, these effects won't influence the action’s outcome until a new action begins. 

For instance, if you're engaged in a 60-minute woodcutting task and a global boost grants +100% experience during this time, this bonus won't apply to this action. To take advantage of the boost, you need to manually restart the action. This requirement means you won’t benefit from the extra experience for the ongoing action unless you refresh it.
