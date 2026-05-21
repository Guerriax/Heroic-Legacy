# Audit : Guerrier - Armes (Arms Warrior)

> **Status:** Alpha 0.0.1
> **Objective:** Validation of spells and talents for level 60 content.

---

### ✅ Working (Opérational)
```cpp
// Verified and functional spells and passives
SPELL_WARRIOR_MORTAL_STRIKE = 12294,
SPELL_WARRIOR_OVERPOWER     = 7384,

🛠️ Needs Scripting / Investigation
// Bugged, poorly scaled, or unimplemented spells
SPELL_WARRIOR_DIE_BY_THE_SWORD = 118038, // Major defensive (check absorption)
SPELL_WARRIOR_BLADESTORM       = 46924,  // Requires full script

🌳 Talents (Arms Tree)
✅ Working
// Functional talents
SPELL_WARRIOR_IMP_REND         = 12834,
SPELL_WARRIOR_TACTICAL_MASTERY = 12678,
SPELL_WARRIOR_DEEP_WOUNDS      = 12834,
🛠️ Needs Scripting / Investigation
// Talents requiring fixes (proc rate, damage, or trigger)
SPELL_WARRIOR_IMP_MORTAL_STRIKE = 29590,
SPELL_WARRIOR_BLOOD_FRENZY      = 29859,
SPELL_WARRIOR_TRAUMA            = 46867,
SPELL_WARRIOR_STRENGTH_OF_ARMS  = 12323,
SPELL_WARRIOR_DEADLY_CALM       = 85730,
📝 Diagnostic Journal

    [05/21/26]: Initial audit started.

    [Date]: Observation on spell X...