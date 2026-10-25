---
title: Why Is My Pour-Over Draining Slowly? Grind Size Isn't the Whole Story
author: Sunny Sun
date: Oct 12, 2026
source: https://mywirsh.com/blogs/coffee-facts/why-is-my-pour-over-draining-slowly-grind-size-isnt-the-whole-story
---
> 原文链接：[Why Is My Pour-Over Draining Slowly? Grind Size Isn't the Whole Story](https://mywirsh.com/blogs/coffee-facts/why-is-my-pour-over-draining-slowly-grind-size-isnt-the-whole-story) ｜ 首发于 [mywirsh.com](https://mywirsh.com/blogs)

GEIMORI | FULL SHOPIFY BLOG BODY | V2 | 2 USER-SUPPLIED CDN DIAGRAMS INCLUDED | 4 CTA LOCATIONS | NO H1
Grinding science / Real GU64 data
**Same grind setting. Same coffee dose. A completely different drawdown time.** If you've brewed pour-over for a while, you've probably seen it happen. The obvious fix is to turn the grinder coarser. But sometimes the dial isn't the whole story.
**We used real data from our GU64 tests for this guide.**
[See the original burr comparison →](https://mywirsh.com/blogs/buying-guide/geimori-gu64-mp-burr-vs-f-burr-one-grinder-two-different-cup-styles)
![Actual Geimori GU64 grinder photographed with MP and F burr sets](https://cdn.shopify.com/s/files/1/0569/8247/0796/files/geimori-gu64-mp-vs-f-burr-guide-hero-1600x900.webp?v=1788761813)
The Geimori GU64 with two factory burr options. This is a burr comparison, not a measured brew-flow experiment.
**The short answer:** Grind size is a distribution, not a single number. Two batches of grounds can have nearly identical median particle sizes yet differ in the range and shape of their particles. Those differences may affect how water moves through the coffee bed. But beans, pouring, filters, and brewing technique matter too.
## 1. Your grinder doesn't produce one particle size
Imagine filling a dripper with pebbles. If they're all similar in size, water finds spaces between them. Add sand and those passages can become narrower. Ground coffee isn't quite that simple - particles have irregular shapes, they move as water enters, and the filter can collect fines - but the picture is useful.
Every grinder makes a range of particle sizes: larger pieces, medium particles, and smaller fragments often called *fines*. The name for that range is **particle size distribution (PSD)**.
That is why a dial number cannot tell you everything about what lands in your brewer. Even a particle size measurement needs more than one number to describe the whole batch.
## 2. D50, Span and Skew: three different questions
Let's keep the statistics practical. In the GU64 measurements we published, the percentiles describe a **volume-based particle size distribution**:
- **D50:** the median diameter in the measured distribution. Half the measured particle volume is on each side of it.
- **D10 and D90:** the lower and upper percentile points. Together they show a useful part of the measured spread.
- **Span:** (D90 - D10) / D50. It describes relative width; it does not tell you which side of D50 stretches farther.
- **Skew, as defined by Barista Hustle:** (p50 - p10) / (p90 - p50). Above 1 means a longer distance toward the smaller-particle side; below 1 means a longer distance toward the larger-particle side.
One important distinction: this particular *Skew* is a percentile-distance ratio, not the standard statistical third-moment skewness. It also isn't a measurement of the percentage of fines below a chosen cutoff.
Barista Hustle's 2026 research examined **224 percolation brews** and reported a meaningful relationship between its Skew measure and total extraction time. The public report does not establish that a Skew of 1 is a flavor target, or that any specific grinder should produce a certain drawdown time. [Read the original research](https://www.baristahustle.com/research-papers/skew-the-missing-variable-in-coffee-grinding/).
## 3. We found an interesting example in our own GU64 data
When we compared the **GU64 MP (Multi-purpose) burr** with the **F (Filter) burr**, we measured particle size at several dial positions. The full tables are in our [GU64 MP vs F burr test](https://mywirsh.com/blogs/buying-guide/geimori-gu64-mp-burr-vs-f-burr-one-grinder-two-different-cup-styles).
Two samples stood out: **MP at setting 60** and **F at setting 50**. They're different dial positions, but their measured medians are almost the same.
| Metric | GU64 MP / 60 | GU64 F / 50 |
| --- | --- | --- |
| D10 | ~165.2 µm* | 183.6 µm |
| D50 | 515.3 µm | 521.2 µm |
| D90 | 854.2 µm | 883.1 µm |
| Span | 1.337 | 1.341 |
| Calculated Skew | ~1.03 | ~0.93 |
*MP60 D10 is estimated from the published rounded D50, D90 and Span. F50 D10 is reported in our full guide. Calculated Skew uses these published, volume-based percentile values, so it is approximate. Values may differ slightly due to rounding. GU64 Skew is not directly interchangeable with Barista Hustle's image-based metric.
The D50 values differ by only **5.9 µm, about 1.1%**. Their Spans are close too. Yet the lower and upper percentile distances are not the same, giving two different calculated Skew values. The difference is modest, not dramatic - but it makes the point: **the median and relative width don't describe every aspect of distribution shape.**
We should also be clear about what these results *don't* show. We did not run a controlled head-to-head drawdown test for these two samples, so we cannot claim one definitely brews faster, tastes sweeter, or has fewer sub-100 µm fines. D10 is not a fines-percentage measurement.
OUR GU64 DATA, VISUALIZED
![GU64 MP60 versus F50 measured D10 D50 and D90 percentile values; line segments visualize intervals rather than full PSD curves](https://cdn.shopify.com/s/files/1/0569/8247/0796/files/geimori-gu64-percentile-comparison.webp?v=1791798724)
Measured GU64 percentile comparison: MP setting 60 and F setting 50. D10 for MP60 is estimated from rounded source values; the graphic is not a full PSD curve.
![Real GU64 MP and F burr D50 laboratory results across grind settings](https://cdn.shopify.com/s/files/1/0569/8247/0796/files/geimori-gu64-mp-vs-f-burr-guide-d50-chart-1200x675.webp?v=1788761813)
Original Geimori GU64 data. D50 changes differently across the dial with the two burr types; the graph is not a brew-time comparison.
If you want to compare every setting, the [complete GU64 particle size article](https://mywirsh.com/blogs/buying-guide/geimori-gu64-mp-burr-vs-f-burr-one-grinder-two-different-cup-styles) includes D50, D90, Span, surface area, and brew-method starting regions for both burrs.
Dig into the measurements
### MP or F burr? Start with the data.
See how the two factory GU64 burr options behave across the dial, rather than choosing by labels alone.
Compare GU64 MP vs F Data →
Explore GU64 Gen2 →
## 4. Why could a different distribution change flow?
A brew bed is not a rigid filter. Water has to move through the openings between irregular coffee particles. Smaller particles can occupy some of those openings; brewing agitation can move fines around; and the paper filter can collect enough fine material to increase resistance.
There is experimental support for the broader role of fines. A 2024 study in *Scientific Reports* varied the amount of fines in **espresso** and found that more fines reduced bed permeability and flow rates under the tested conditions. That's useful physical context, but espresso is pressure-driven and is not the same experiment as gravity-fed pour-over. [Read the study](https://www.nature.com/articles/s41598-024-55831-x).
WHY WATER MAY FLOW DIFFERENTLY
![Conceptual schematic of coffee particles of different sizes in a brew bed and possible water flow paths](https://cdn.shopify.com/s/files/1/0569/8247/0796/files/coffee-bed-flow-conceptual.webp?v=1791798724)
Conceptual illustration of coffee-bed permeability. It does not represent a measured GU64 brew-flow test.
This is also why we wouldn't say "lower Span = better coffee" or "Skew = 1 is ideal." Particle distribution is part of a system that also includes the coffee, brewer, filter, water, and the person pouring it.
![Geimori GU64 MP and F burr Span measurements across grind settings](https://cdn.shopify.com/s/files/1/0569/8247/0796/files/geimori-gu64-mp-vs-f-burr-guide-span-chart-1200x675.webp?v=1788762081)
Geimori's measured relative distribution width. A lower Span describes the dataset; it cannot predict flavor or drawdown time by itself.
## 5. My pour-over is running slow. What should I check first?
Before moving the grinder two clicks coarser, try a simpler diagnostic. Change one variable at a time so you can tell what fixed the problem.
1. **Check the beans.** New coffee, a different roast, or changing rest time after roasting may change how the beans fracture and behave during brewing.
1. **Keep the recipe fixed.** Use the same dose, water amount, temperature, and dripper before comparing drawdown time.
1. **Watch your pour.** A stronger stream, more agitation, or a higher pour can move fines and change how the bed settles.
1. **Check the filter and brewer.** Switching paper filters or seating them differently can change resistance.
1. **Check the grinder.** Confirm the burrs are clean and the adjustment hasn't shifted. Different burr sets may require different useful dial positions.
1. **Then adjust by flow and taste.** A slow cup isn't necessarily a bad cup; bitterness, drying finish, sharp acidity, sweetness, and texture all help you decide what to change.
What if you're comparing two different grinders? Don't try to transfer a dial number. Start with a sensible brew recipe, make small changes, and judge the cup rather than assuming the same-looking grounds must behave identically.
Ready to dial in your own grinder?
Start with a grinder that fits the way you actually brew.
If pour-over is your daily routine, compare our flat-burr options and the GU64 MP / F data before choosing a starting setting.
Explore Geimori Grinders →
See the GU64 Data
## 6. What does this mean when choosing a grinder?
It doesn't mean every coffee drinker needs a particle-size analyzer. It means grinder decisions are more interesting than a single burr diameter, RPM figure, or grind-size setting.
On the [Geimori GU64 Gen2](https://mywirsh.com/products/geimori-gu64), the factory MP and F burrs are two ways to use the same 64 mm flat-burr platform. Our measured data shows the MP option reaches finer medians over more of its tested range, while the F option moves into common filter-size regions earlier. Both cover overlapping territory, and neither is a guaranteed shortcut to a particular flavor.
If you're comparing burr styles more broadly, start with our [flat vs conical burr guide](https://mywirsh.com/blogs/coffee-facts/how-to-choose-the-right-coffee-grinder-conical-burrs-vs-flat-burrs-what-s-the-difference-in-flavor). For the motor-speed question, see our [grinder RPM and extraction article](https://mywirsh.com/blogs/buying-guide/how-rpm-can-influence-grind-quality-flow-and-flavor). Speed and burr geometry may influence grinding, but either one by itself is too simple a predictor of what ends up in your cup.
## A few quick questions
### Does a slow pour-over always mean the grind is too fine?
No. Grinding too fine is one possible cause. Agitation, fines migration, paper filters, coffee changes, and pour technique can all contribute to slower drawdown.
### Is D50 the same as my grinder setting?
No. D50 describes a measured median particle size. Your dial is a mechanical adjustment, and identical dial numbers don't translate between burr sets or grinders.
### Does Skew tell me which burr makes better coffee?
No. It describes the asymmetry between three percentile points under a particular measurement method. It isn't a taste score, a direct fines percentage, or a substitute for brewing and tasting.
## The takeaway
The next time your V60 takes 40 seconds longer than usual, don't assume the grind dial must be wrong. The coffee has a whole particle distribution, and the brew has a whole flow system. **Grind size is a starting point, not the whole explanation.**
For curious home baristas
### Choose your burrs with a little more context.
Explore the GU64 Gen2 and the real MP vs F particle-size measurements. Then dial in for your coffee, brewer, and taste.
Explore the GU64 Gen2 →
Read Our GU64 Test →
## Sources and measurement notes
Our GU64 examples use Geimori's published laboratory particle-size tables and their volume-distribution D values. Barista Hustle analyzed 224 conical-device percolation extractions with a DiFluid Omni image-based method covering approximately 100-2500 µm. These measurement bases and particle detection limits differ; their Skew values should not be treated as directly interchangeable. Our two GU64 samples were *not* tested against each other for drawdown time, extraction yield, or blinded flavor in this article.
1. [Geimori: GU64 MP Burr vs F Burr - Full Particle Size Dataset](https://mywirsh.com/blogs/buying-guide/geimori-gu64-mp-burr-vs-f-burr-one-grinder-two-different-cup-styles).
1. [Martinez-Portilla and Ibarra-Hidalgo (2026), "Skew - The Missing Variable in Coffee Grinding," Barista Hustle](https://www.baristahustle.com/research-papers/skew-the-missing-variable-in-coffee-grinding/).
1. [Smrke, Eiermann, and Yeretzian (2024), "The Role of Fines in Espresso Extraction Dynamics," Scientific Reports](https://www.nature.com/articles/s41598-024-55831-x).
