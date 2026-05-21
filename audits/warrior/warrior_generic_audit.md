# Audit: Warrior Generic

> **Status:** Alpha 0.0.1
> **Objective:** Validation and custom scripting of Warrior utility spells.

---

### ✅ Working (Opérational)
```cpp
// Verified and functional spells and passives
SPELL_WARRIOR_RALLYING_CRY = 97462,

🛠️ Needs Scripting / Investigation
// Bugged, poorly scaled, or unimplemented spells
SPELL_WARRIOR_RALLYING_CRY = 97462, // Tooltip showing 0% granted in any circumstances.

📝 Diagnostic Journal

    [05/21/26]: Initial audit started.

    [05/21/26]: Resolved dynamic scaling for Rallying Cry (97462).

    What was done: Modified the HandleScript function in spell_warrior.cpp to implement a conditional logic check. The spell now verifies the caster's group status using the Group::isRaidGroup() API.

    How it was done: 1. Defined a base percentage variable (int32 percent = 10;).
    2. Implemented a safety check to confirm the caster is a player and retrieved their associated group.
    3. Applied a condition: If the player is not in a raid group (!group->isRaidGroup()), the percentage is adjusted to 50%.
    4. Passed this dynamic value to AddSpellMod and executed the spell, ensuring the server calculates the health bonus based on the current context rather than a fixed value.

    Why it was done: The default implementation provided a static 10% health bonus, which felt underwhelming for solo gameplay. By introducing contextual scaling, the spell remains balanced for raid environments (10%) while offering significant survivability for solo content (50%).
