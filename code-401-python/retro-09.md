# Retro: 09 - Game of Greed IV - 01/08/2022

Lab 09 was ok. I pass all the tests and game runs ok but bot couldn't use my `game.py` to simulate the game because I used recursion in my implementation and it caused
`maximum recursion depth exceeded in comparison` error. It was a good example that sometimes recursion is not a good solution especially for simulation tests (default python recursion depth is 1000).

There are some improvements I could do, such as input validation. Current lab only requires us to validate right inputs such as `r, b, q`, but technically player can pass anything they want or sometimes just typo.

For me `get_scorer` method doesn't make much sense. It assumes plays would redeem the combination that would give them highest points. For example, for dice `1, 1, 3, 4, 5, 6`, player can redeem `1` or `1, 5` or `1, 1, 5`. But current implementation only take `1, 1, 5` as valid input. If player redeem `1` or `1, 5`, it would prompt player that they are cheater.
