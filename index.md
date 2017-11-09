## Welcome to Card Games

### The Elo rating system
The Elo rating system rates players based on previous skill shown in games. Every player starts with a rating, which we will call \[R_I\]. Let \[R_A\] be your rating and \[R_B\] be the opponent's rating. Then, $$E_A = \frac{1}{1 + 10^{(R_B - R_A)/400}}$$ and $$E_B = 1 - E_A$$.

To update a rating, let \[S\] be the score of the player with rating \[R_A\]. Set a volatility coefficient \[K\]. Then, $$R_A = R_A + K(S-E_A)$$ and $$R_B = R_B - K(S-E_A)$$.
