---
expanded: true
label: Fees
order: 1
---

To complete an incubation process, player has to pay the required fees that are calculated for the selected snails.

| Owned By Player | Fees                                  |
|-----------------|---------------------------------------|
| Only Female     | Incubation Fee + Male Genome Price      |
| Female and Male | Incubation Fee                          |

---

## Incubation Fee

Incubation fee is dynamic and will be shown to users during incubation. There are several factors that can affect the Incubation fee:

* Genes of Male & Female Snail
* Breed Counts (Male + Female)
* Protocol Coefficient

$$
IncubationFee =\sum_{i=1}^{20} ({MaleGene}_{i}+{FemaleGene}_{i}) * (1 + 0.1 * BreedCount_{male+female} ) * (ProtocolCoefficient)
$$

==- **Genes**

Each gene has a different coefficient. Superior genes are more expensive.

| Atlantis (X) | Agate (A) | Milk (M) | Helix (H) | Garden (G) |
|:------------:|:---------:|:--------:|:---------:|:----------:|
|       6      |     5     |     4    |     3     |      2     |

==- **Protocol Coefficient**

Protocol Coefficient (PC) is a dynamic global value that changes with respect to; 
* Snail Population
* Daily Growth Rate

Snail population determines the daily threshold value; 

$$
T = \dfrac{population*0.2}{30}
$$

which represents the mean daily growth amount for the snail
population. 

Let's understand the math with an example;
If the population is 7500, then mean targeted growth amount for a month is 1500 snails, which translates to 50 snails per day. 50 is the threshold value for the given example.

---

Protocol coefficient is calculated with following formula;

$$
\displaystyle PC_{next}= \begin{cases} {PC_{current} * (1 + \dfrac{0.1}{T})},& \text{} BreedingEvent\\ PC_{current} * 0.9,              & \text{if BreedCount}_{daily} \lt T  \end{cases}
$$

* If a breeding event happens, protocol coefficient for the next breeding event is increases slightly which also means $T$ cumulative breeding event is nearly equal to 10% increase in total.
* If in a single day, the amount of breeding event stays under the threshold value $T$, then $PC$ decreases by 10%.
* Days are calculated with respect to GMT timezone.

===
---
## Male Genome Price

Male genome price is determined by the sellers on the market.