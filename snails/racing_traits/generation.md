---
label: Generation
order: 10
---
The generation of a snail represents how far down a snail is from the first ancestor on its family tree. A snail can be brought to Earth in two different ways: as an **Incubator** or a **Laboratory** snail.

***

### Incubator
Let's say;
* G is the generation of a newborn.
* A is the generation of Parent A.
* B is the generation of Parent B.
  
| Chance | When breeding two snails together, the new generation is calculated as follows: | Algorithm Tag |
|--------|---------------------------------------------------------------------------------|---------------|
| 45%    | G = $\max{(A, B )}$ + 1                                                           | Max           |
| 25%    | G = $\max{(A, B )} + \lfloor\sqrt{(\mid A-B\mid) + 1} \rfloor$                    | Root          |
| 16%    | G = $\max{(A, B )} + \lfloor\log_2({\mid A-B\mid +1)+1} \rfloor$                  | Log           |
| 9%     | G = $\min{(A, B )} + \lfloor\mid A-B\mid /2 + 1\rfloor$                           | Double        |
| 4%     | G = $\min{(A, B )} + \lfloor \mid A-B\mid /3 + 1\rfloor$                          | Triple        |
| 1%     | G = $\min{(A, B )}$ + 1                                                           | Min           |

Seems quite complex, no? Don't worry about the formulas though; the odds for each Algorithm Tag will be shown during the Incubation.

***

### Laboratory
This topic is covered in the [Laboratory]() section.
