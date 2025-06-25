# Meditation

Meditation is a unique skill in idleMMO that is entirely based on the concept of selflessness and the helping of others, rather than yourself.

---

#### How It Works

Getting started is easy:

- Just press **Start** to begin meditating.
- You’ll gain EXP at a base rate of **0.8 EXP per second**.

---

#### Guidance Scrolls (Unlocked at Meditation Level 35)

At level 35, you unlock the ability to create **Guidance Scrolls** - powerful items designed to **boost other players**.

Here’s how they work:

- You’ll earn **0.1 EXP/s** while writing guidance scrolls.
- You need a **Blank Scroll** to write one. You can buy these from the vendor.
- You **can’t** use a guidance scroll on yourself or your alts - this skill is all about helping *others*.
- The higher your Meditation level, the **stronger the boost** in the scroll.
- Once given, the scroll’s effect is applied **instantly** and lasts for **2 hours**.
- Writing a scroll takes **60 minutes**.
- You can’t write more scrolls than your **maximum idle time** allows. For example:
    - If your idle time cap is 2 hours, you can’t queue up 5 scrolls (which would take 2.5 hours total).
- If you cancel a scroll mid-way:
    - Any **unused blank scrolls** are refunded.
    - Any scrolls already **in progress** are *not* refunded.
  
>!!banner The effects of the guidance scrolls scale from **1%** to **15%** based on your Meditation level.

>!!banner Trade-locked classes such as Banished and Cursed cannot write scrolls.

>!banner Users that are trade-locked can write scrolls, but cannot send them.

---

#### Buufs

Guidance Scrolls give the following bonus:
+#% World Boss Magic Find
+#% Dungeon Magic Find
+#% Battle Magic Find
+#% Hunt Efficiency
+#% Guild Mastery EXP
+#% Hunt EXP
+#% Combat EXP
+#% Primary Skill EXP

---

#### Enlightenment

Reach **level 100** and you’ll achieve **Enlightenment** — a prestigious milestone with a cosmetic twist.

- Your character will float slightly on its profile page giving it an ethereal aura.

>!banner We’re planning to add even more cosmetic-only features for Enlightened players in the future.

---

#### Sound Effects

While meditating, you can listen to various sound effects to help you relax.

- __Rain__ - The sound of rain falling.
- __Snowfall__ - The sound of snow falling.
- __Fireplace__ - The sound of a crackling fireplace.
- __Thunderstorm__ - The sound of a thunderstorm.

>!banner Due to technical limitations with the web browser, the sound effects must be manually enabled.

---

#### Notes

- The Meditation skill is **purely focused on helping others** - it’s not designed to benefit your own character directly.
- Progression is intentionally slow - not only does it take months of dedication, but it also means you're sacrificing time that could’ve been spent on other skills.
- Reaching **Enlightenment** is meant to be a rare and meaningful achievement that reflects **patience, dedication, and selflessness**.

---

#### Guidance Scroll Scaling Formula

The meditation skill is exponential in nature, meaning that the effect of the guidance scrolls increases at a faster rate as you level up. 

Below is a breakdown of the formula and what each variable represents:

- **current_level**: The player's current Meditation level (ranges from 1 to 100).
- **minimum_value**: 1% — the effect at the lowest level.
- **maximum_value**: 15% — the effect at the highest level.
- **exponent**: 3.5 — this controls the steepness of the curve. A higher exponent means that improvements become more significant at higher levels.


Here’s a step-by-step breakdown of how the effect is calculated:

1. **Normalize the Level**  
   Convert your current Meditation level into a value between 0 and 1.
    - **How:** Subtract the minimum level (1) from your current level, then divide by the range (maximum level minus minimum level).
    - **Formula:**
      ```
      normalized_level = (current_level - 1) / (max_level - 1)
      ```

2. **Apply the Exponential Curve**  
   To create a curve where improvements are more noticeable at higher levels, raise the normalized value to an exponent (for example, 3.5). This makes early level increases smaller and later level increases larger.
    - **Formula:**
      ```
      adjusted_value = normalized_level^exponent
      ```

3. **Scale to the Final Effect Value**  
   Convert the adjusted value into the actual effect percentage by scaling it between the minimum effect (1%) and the maximum effect (15%).
    - **How:** Multiply the adjusted value by the difference between the maximum and minimum values, then add the minimum value.
    - **Formula:**
      ```
      effect_value = minimum_value + (maximum_value - minimum_value) * adjusted_value
      ```
