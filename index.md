## Welcome to Card Games

### Overall rating

|Matchday|Date|Game|Rounds|I|R|GL|K|J|
|-
|1|November 3|Hearts|7|1535|1488|1465|1512|1500|
|2|November 6|Hearts|2|1535|1478|1463|1515|1510|
|3|November 8|Hearts|6|1501|1490|1497|1503|1510|

### Results

|Matchday|Date|Game|Rounds|I|R|GL|K|J|
|-
|1|November 3|Hearts|7|1|3|4|2|-|
|2|November 6|Hearts|2|-|4|3|2|1|
|3|November 8|Hearts|6|4|2|1|3|-|


### Hearts rating

|Matchday|Date|Game|Rounds|I|R|GL|K|J|
|-
|1|November 3|7|1535|1488|1465|1512|1500|
|2|November 6|2|1535|1478|1463|1515|1510|
|3|November 8|6|1501|1490|1497|1503|1510|

### Rating calculation
Each player starts with a rating of 1500. We use the Elo system of card game rating. Basically, we take the mean rating $$M$$ of all players other than the player being rated participating in the game, and for each player, their score is, based on their placing in the game $$p$$ and the number of players $$n$$:

$$S = 1 - \frac{p-1}{n-1}$$

Let $$R'$$ be the new rating and $$R$$ be the old rating. Then,

$$R' = R + K(S - \frac{1}{1 + 10^{(M-R)/400}})$$

where $$K = 10 \times \text{number of rounds}$$.

### Formal description
Formally, let $$\{R_1, R_2, \dots R_n\}$$ be the ratings of the players participating, $$K = 10 \times \text{number of rounds}$$, and $$\{p_1, p_2, \dots, p_n\}$$ be the placings of the players. Then, to update the ratings to the new rating $$\{R'_1, R'_2, \dots, R'_n\}$$

$$R'_i = R_i + K((1 - \frac{p_i-1}{n-1}) - \frac{1}{1 + 10^{(\frac{1}{n-1}\sum_{r \in \{R_1, R_2, \dots, R_{i-1}, R_{i+1}, \dots, R_n\}}-R_i)/400}})$$
