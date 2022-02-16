---
label: ELO Ranking
order: 1
---

### Basics
When snails enter the world of racing, they will not be part of any League. They will be born with a default score and it will change entirely by win/loss stats in relation to other players. A Sorting Hat will determine the league of the snail after its 5th race. After the replacement, the journey begins.

It is expected that, on average, snails that have higher Elo will perform better than lower ones. After every match, the actual outcome will be compared with the expected outcome, and consequently, the snail rating will be adjusted. Don't forget that your snail can also shine in Bronze League and might bring a treasure back home.

The Elo system that is being used in this game might differ from the classic chess approach. If **Player A** has a rating $R_{a}$ and Player B a rating $R_{b}$ , the formula will be similar to the following (expect the coefficient might change) for the expected score of Player A;

$$ 
E_{a}  = 1 / (1 + 10^{ ( R_{b} -  R_{a}) /400 } )
$$

and Player B will be;

$$ 
E_{b}  = 1 / (1 + 10^{ ( R_{a} -  R_{b}) /400 } )
$$

Considering the maximum possible adjustment per game is K-factor.
The formula for updating that player's rating is;

$$
R'_{A} = R_{A} + K(S_{A} - E_{A})
$$

### Multiplayer
 
Above approach is a simple calculation of the ELO for a two player match-up. In Snail Trail, this fromula is extended to calculate the ELOs after a 10-player race.

In which each players score functions will be;

$$
S_{A}(p_A) = \dfrac {N-p_A }{N(N-1)/2}
$$

The formula for updating a player's rating is almost identical to standard two-player Elo version;

$$
R'_{A} = R_{A} + K(N-1)(S_{A} - E_{A})
$$

The update will happen after any suitable rating period. 

--- 

### Placement

* A snail's ELO and league will be detemıned after its first 5 race.
* First 5 races will be the most important races to determine the base elo of each snail.