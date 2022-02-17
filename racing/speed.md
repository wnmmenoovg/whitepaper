---
label: Speed
order: 1
---

Speed is the secret sauce of the game. Each snail's speed is calculated based on various **racing traits**, **coefficients** and **randomness**. Snail owners should experiment with their snails to find or breed the perfect ones for racing. Superior traits make a snail better on average, however it does not make a snail strictly better than the another one.

Each snail have the following traits that affect its racing performance:

|        Trait        |           Importance           |    How to target?    |
|:-------------------:|:------------------------------:|:--------------------:|
|    Family & Genes   | :star::star::star::star::star: | Reproduction Systems |
| Genome Coefficients |    :star::star::star::star:    |        Random        |
|        Purity       |    :star::star::star::star:    | Reproduction Systems |
|     Adaptations     |    :star::star::star::star:    |    Decision Making   |
|   Trail Preference  |       :star::star::star:       |    Decision Making   |
|        Class        |          :star::star:          | Reproduction Systems |
|      Generation     |             :star:             | Reproduction Systems |


### Family
Each gene has a value and it is multiplied with snail's secret genome coefficient then used in the speed formula. Family and Gene superiority is stated in the following document.
[!ref](../snails/racing_traits/family.md)

### Purity
Purity is calculated from occurance of genes in the genetic sequence. Snail with greater purity value is superior to a lesser one.

### Class
Class superiority is stated in the following document.
[!ref](../snails/racing_traits/class.md)

### Generation
A snail's generation affects its racing performance. A snail with lesser generation is superior to a greater one.
[!ref](../snails/racing_traits/generation.md)


### Genome Coefficients
Each snail has 20 genes. For these 20 genes there are also **genome coefficients** array.
* This array contains **same** values for every snail.
* It's order is randomized at birth for every snail
* Genome Coefficients array does not change for a season.
* An encrypted version of a snail's genome coefficient array is publicly available in the NFT metadata. However, plaintext version will be revealed once the season ends. This way users will be able to verify it.
* Numbers in the array are given below table for each season. Keep in mind that, numbers do not necessarily represent a linear change.


| Season      | Seed Genome Coefficients                                        |
|-------------|-----------------------------------------------------------------|
| Beta Season | [4, 3, 3, 2, 2, 2, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, -1, -2, -3] |

* There are 17 positive and 3 negative coefficients. 
* If a snail have a superior gene for a greater coefficient then that combination might add more value to its speed than a lesser gene and greater coefficient combination.

### Adaptations
Adaptations increase a snail's speed. This happens in two ways:
* **Default:** Just having an adaptation turns a negative gene coefficient into a positive one. If a snail have 3 adaptations then all the values on its genome coefficient array will be positive. This effect will convert numbers in following order `(-1, -2, -3)`. If a snail has;
  *  3 adaptations, negative coefficients will be `1, 2, 3`
  *  2 adaptations, negative coefficients will be `1, 2, -3`
  *  1 adaptations, negative coefficients will be `1, -2, -3`
* **Counter:** If a snail counters a track's conditions with its adaptations then related coefficient bonus is doubled for that snail. This effect will boost numbers in following order `1, 2, 3`. If a snail counters;
  *  3 conditions, bonus will be `2 & 4 & 6`
  *  2 conditions, bonus will be `2 & 4`
  *  1 condition, bonus will be `2`

### Trail Preference
There are 9 different distances for racing. Each snail performs better than its usual at 2 different distances.
* Trail Preference is secret for all snails.
* An encrypted version of a snail's trail preference is publicly available in the NFT metadata.

!!!dark Reminder
* Some traits are subject to seasonal resets.
* New variables will be introduced with upcoming patches. 
* Some traits might be more useful with in the future game modes.
!!!