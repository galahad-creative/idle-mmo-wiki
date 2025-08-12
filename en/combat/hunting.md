# Hunting

Before you jump into combat, you'll first need to locate a group of enemies by going on a hunt. How long your hunt lasts depends on two things: your `Movement Speed` and your `Hunting Mastery`. The faster you move and the more skilled you are at hunting, the longer you'll be able to keep up the chase.

The longest you can hunt is tied to your character’s maximum idle time. For example, if your character is marked as the "main character" and has an active membership, they can stay in action for up to **8** hours.

You can increase your `Movement Speed` with the help of [Pets](/wiki/activities-and-challenges/pets) and you can increase your `Hunting Mastery` by completing hunts.

---

### Ending Hunts Early

If you need to stop a hunt, just click `Cancel Hunt`. You'll still receive part of the rewards, based on how long you spent hunting.

For example, if you were hunting **200** enemies over **100** minutes and canceled after **50** minutes, you’d get rewards for **100** enemies since you completed **50%** of the hunt.

You can restart a hunt at any time, and it will continue from where you left off. Any new enemies you hunt will be added to what you’ve already hunted. So, if you’ve already hunted **50** `Goblins` and start again, the new enemies will stack on top of those 50.

---

### Enemy Decay
Enemies will flee over time if you're not fast enough to engage them in battle. The rate at which they run away depends entirely on your hunting level - the higher your hunting mastery, the fewer enemies will escape.

The scale ranges from **10%** to **2.5%**. At Hunting Mastery level 1, **10%** of discovered enemies will flee every **4 hours**. At Hunting Mastery level 100, only **2.5%** will flee in the same timeframe.

The timer starts when the enemy is first discovered, and you’ll see a countdown in the enemy's dialog box to show you exactly when they are expected to flee.

---

### Power Hunting

Power hunting is an optional interactive twist to hunting that gives you the ability to hunt for more items by tapping on enemies that appear on the screen.

- Power hunting lasts between **10** and **25** minutes depending on your hunting mastery level.
- The experience obtained from power hunting is between **1** and **18** depending on your hunting mastery level. 
- Enemies spawn between **6** and **11** seconds apart.
- After a power hunt has ended, you will have to wait **1** hour before you can start another one.

---

#### Notes

>!banner You can only hunt enemies that match your combat level. For example, if your combat level is **20**, the highest level enemies you can hunt are level **20**. Enemies above level **20** will not be hunted. So, if you try hunting in higher-level areas without the required combat level, you may end up with no enemies.

>!banner Since `v0.23.0`, pets can no longer hunt for enemies on behalf of your character. Only your characters can hunt.

>!banner Since `v0.23.5`, there are no limits to the number of enemies you can hunt. Instead, the slowly decay over time.

---

### Formulas

#### Enemies Per Second

**Base Spawn Rate**: 0.03\
**Max Level**: 100\
**Minimum Movement Speed**: 1\
**Max Movement Speed**: 50\
**Normalized Level**: (_Character Level_ - 1) / (_Max Level_ - 1)\
**Normalized Movement Speed**: (_Movement Speed_ - _Minimum Movement Speed_) / (_Max Movement Speed_ - _Minimum Movement Speed_)\
**Scaling Factor**: 1 + _Normalized Level_ + _Normalized Movement Speed_\
**Enemies Per second**: _Base Spawn Rate_ × _Scaling Factor_
