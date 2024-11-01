# Hunting and Battling

## Hunting

Before you jump into combat, you'll first need to locate a group of enemies by going on a hunt. How long your hunt lasts depends on two things: your `Movement Speed` and your `Hunting Mastery`. The faster you move and the more skilled you are at hunting, the longer you'll be able to keep up the chase.

The longest you can hunt is tied to your character’s maximum idle time. For example, if your character is marked as the "main character" and has an active membership, they can stay in action for up to **180** minutes.

You can increase your `Movement Speed` with the help of [Pets](/wiki/activities-and-challenges/pets) and you can increase your `Hunting Mastery` by completing hunts.

#### Ending Hunts Early

If you need to stop a hunt, just click `Cancel Hunt`. You'll still receive part of the rewards, based on how long you spent hunting.

For example, if you were hunting **200** enemies over **100** minutes and canceled after **50** minutes, you’d get rewards for **100** enemies since you completed **50%** of the hunt.

You can restart a hunt at any time, and it will continue from where you left off. Any new enemies you hunt will be added to what you’ve already hunted. So, if you’ve already hunted **50** `Goblins` and start again, the new enemies will stack on top of those 50.

#### Enemy Decay
Enemies will flee over time if you're not fast enough to engage them in battle. The rate at which they run away depends entirely on your hunting level - the higher your hunting mastery, the fewer enemies will escape.

The scale ranges from **25%** to **10%**. At Hunting Mastery level 1, **25%** of discovered enemies will flee every **3 hours**. At Hunting Mastery level 100, only **10%** will flee in the same timeframe.

The timer starts when the enemy is first discovered, and you’ll see a countdown in the enemy's dialog box to show you exactly when they are expected to flee.

#### Notes

- You can only hunt enemies that match your combat level. For example, if your combat level is **20**, the highest level enemies you can hunt are level **20**. Enemies above level **20** will not be hunted. So, if you try hunting in higher-level areas without the required combat level, you may end up with no enemies.
- Since `v0.23.0`, pets can no longer hunt for enemies on behalf of your character. Only your characters can hunt.
- Since `v0.23.5`, there are no limits to the number of enemies you can hunt. Instead, the slowly decay over time.

## Battling

Once you've located a mob, you can start a battle by selecting an enemy and clicking `Battle`. You may only select one enemy at a time to battle.

#### Battle Mechanics

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

All of these values are dependent on your stats, equipment, the enemies stats, and the food you brought with you.

#### Food

Before starting a battle, you can choose various food items to take with you. These items increase your overall **effective health**, allowing you to fight for longer.

For example, if your character has **100** HP and you bring **20** food items, each adding **10** HP, your total effective health becomes **300** HP `(100 + (20 * 10) = 300)`. With more effective health, you can take on more enemies without being defeated. If you bring enough food, you might even be able to fight all the way up to your character’s maximum idle time.

If you end a battle early, any unused food will be returned to your inventory. The system will attempt to prioritise using the weakest food items first. For example, if you have 1x **500** HP food item and 100x **100** HP food items, it will try to use the **100** HP items before the **500** HP item. However, this may not always happen exactly like this, as it depends on the battle and when you choose to stop it.

#### Stance
Stance lets you choose which stat you want to focus on when earning EXP rewards after defeating an enemy.

Here are the five stances you can select:

**Balanced**: Obtains EXP for every primary stat. for instance, if you get 20 EXP, then each stat will get 5 EXP.\
**Offensive**: Obtains EXP only for `Strength`.\
**Defensive**: Obtain EXP only for `Defence`.\
**Agile**: Obtains EXP only for `Speed`.\
**Dexterous**: Obtains EXP only for `Dexterity`.

You can choose your stance when you start a battle, but you can't change it once the battle begins. If you want to switch stances, you’ll need to end the current battle and start a new one.

When you defeat an enemy, both your `Combat Level` and selected stats will increase. For example, if you earn 20 EXP from defeating an enemy, `20 EXP` will be applied to the stats based on your selected stance, and another `20 EXP` will be added to your `Combat Level`.

#### Notes

- Taking a lot of food with you will increase your effective health, allowing you to battle for longer.
- Improving your stats with better equipment means you can defeat enemies faster and with less damage taken. This also means you don't need to use as much food - saving additional time and money.
- Using the `Balanced` stance may result in less EXP if it cannot be divided evenly. For instance, if you defeat an enemy and you obtain `25 EXP`, that means each stat will get `6 EXP` totalling at `24 EXP` and the remaining `1 EXP` will be lost.
- There is a limit of __8 seconds__ seconds per enemy. It's not possible to defeat enemies quicker than __8 seconds__.
- There is a minimum of _1 damage__ taken per battle. It's impossible to encounter a battle and leave unharmed.