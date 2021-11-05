# The Resurrected Frenzy IAS Calculator
Frenzy IAS calculator for Diablo 2 (Resurrected)

The calculator is live and usable at: [https://chthonvii.github.io/resurrectedfrenzyiascalc/](https://chthonvii.github.io/resurrectedfrenzyiascalc/)

Of all skills in D2, Frenzy has proven the most difficult for the community to fully unravel. It wasn't until 2010 that TitanSeal got the IAS calcuations finally figured out. Unfortunately, he never updated his popular calculator with the correct equations, and his lesser-known script with the correct equations seems to have disappeared along with the inDiablo.de forums. This calculator is based on formulae and empircal test results found in old forum posts on amazonbasin and diabloii.net by TitanSeal and onderduiker and a (flawed) matlab port of the script posted on d2jsp by Jink.

**Accuracy Status:**

This calculator has been verified against onderduiker's very rigorous empircal tests for cases where the average base weapon speed is an even number, and cases where the average base weapon speed is a negative odd number. It has not been verified against empirical tests for the case where average base weapon speed is a positive odd number, because no test data is available. (Everyone wants to use a phase blade...) If you'd like to contribute, please follow onderduiker's methodology and post your results to an issue ticket on the github page.

**Important Bugs:**

1. "First Swing Misses Bug": If Frenzy's first swing misses, then the second swing will use the frames-per-attack and chance-to-hit values from the first swing rather than its own values.
2. "WSM Bug": The bugged state is entered by picking up and re-equipping the weapon in the gloves-side slot (or by the exception noted below). The bugged state is visually indicated by the boots-side weapon appearing in the character model's right hand. An alternative weapon speed calculation is used in the bugged state. This alternative calculation yields a faster attack speed than the normal calculation if the boots-side weapon is faster than the gloves-side weapon. The wider the differential, the bigger the benefit. The bugged state will automatically end upon loading screen, death, or weapon swapping, unless the following exception applies. Exception: The bugged state will persist if you are only able to equip the gloves-side weapon due to a "reduced requirements" mod (e.g., you have an ethereal Death colossus sword in the gloves-side slot and less than 172 strength) and/or stat points from the boots-side weapon.

**Practical Notes:**

- Always put the weapon with the fastest base speed in the boots-side slot. If base speeds are the same, put the one with the most IAS in the boots-side slot.
- If using the popular Grief phase blade, the IAS roll is irrelevant in almost(?) all cases.
- If using the popular Grief phase blade + Death combo, use a colossus sword for Death. The colossus blade's slightly faster base speed is irrelevant.
- If using the popular Grief phase blade + Death combo, the 20% IAS on Highlord's Wrath is enough to reach the last realistic breakpoint

**Sources:**

- [TitanSeal's math summary](https://www.theamazonbasin.com/forums/index.php?/forums/topic/119196-calculator-inaccuracy-for-frenzy-attack-speed/&do=findComment&comment=1483417)
- [Rigorous experimental results by onderduiker](https://www.theamazonbasin.com/forums/index.php?/forums/topic/119196-calculator-inaccuracy-for-frenzy-attack-speed/page/2/&tab=comments#comment-1481252)
- [More experimental results](https://www.theamazonbasin.com/forums/index.php?/forums/topic/119196-calculator-inaccuracy-for-frenzy-attack-speed/&do=findComment&comment=1478263)
- [More experimental results](https://www.theamazonbasin.com/forums/index.php?/forums/topic/119196-calculator-inaccuracy-for-frenzy-attack-speed/&do=findComment&comment=1478347)
- [More experimental results, relevant to a tricky rounding issue](https://www.theamazonbasin.com/forums/index.php?/forums/topic/119196-calculator-inaccuracy-for-frenzy-attack-speed/&do=findComment&comment=1483559)
- [Jink's matlab port (buggy)](https://forums.d2jsp.org/topic.php?t=38476029&f=87&p=295852483#p295852483)
- [Useful summary for the popular Grief+Death combo.](https://www.diabloii.net/forums/threads/frenzy-qs.840692/#post-8659475)
- [Explanation of "first swing misses" bug](https://www.theamazonbasin.com/forums/index.php?/forums/topic/119196-calculator-inaccuracy-for-frenzy-attack-speed/page/2/&tab=comments#comment-1528433)
- [Explanation of WSM bug](https://www.diabloii.net/forums/threads/frenzy-qs.840692/)
