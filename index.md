## Welcome to Card Games

### Rating table

|Matchday|Date|Game|Rounds|I|R|GL|K|J|
|-
|1|November 3|7|Hearts|1535|1488|1465|1512|1500|
|2|November 6|2|Hearts|1535|1478|1461|1516|1510|
|3|November 8|6|Hearts|1508|1486|1488|1508|1510|

### Results
|Matchday|Date|Game|Rounds|I|R|GL|K|J|
|-
|1|November 3|7|Hearts|1|3|4|2|-|
|2|November 6|2|Hearts|-|4|3|2|1|
|3|November 8|6|Hearts|4|2|1|3|-|

### Rating calculation
Each player starts with a rating of 1500. We use the Elo system of card game rating. Basically, we take the mean rating $$M$$ of all players participating in the game, and for each player, their score is, based on their placing in the game $$p$$ and the number of players $$n$$:

$$S = 1 - \frac{p-1}{n-1}$$

Let $$R'$$ be the new rating and $$R$$ be the old rating. Then,

$$R' = R + K(S - \frac{1}{1 + 10^{(M-R)/400}})$$

where $$K = 10 \times \mathrm{number of rounds}$$.
