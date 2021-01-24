# Journal-05 - 1/23/2021

I learned JS Array methods such as push, pop, shift, and unshift. We also went over CSS selectors and positioning and git flow - working on a branch. Lab-5a was not hard, I just needed to write 6 functions that I was asked. I completed the stretch goal, the last 3 functions can take an array with any length as an argument.

## Native JS Array Methods - comes with/build-in JS

- `push(<something>)` - inserts into the BACK of the Array
- `pop()` - removes from the BACK of the Array
- `shift()` - removes an item from the FRONT of an array - note it reassigns ALL of the indexes
- `unshift(<something>)` - inserts into the FRONT of the Array
- `splice(<starting index>, <number of items to remove>, <what to add - if anything>)` - remove and add ANYWHERE in an array

## CSS selectors and positioning

- position - static, relative, absolute, fixed
- float - left, right
- display - block, inline, inline-block, flex

## Git flow - working on a branch

1. make branch: `git checkout -b <branch-name>`
2. ACP: `git push origin <branch-name>`
3. make PR request
4. merge the code
5. checkout to the main branch: `git checkout main`
6. sync local main branch with GitHub main branch: `git pull origin main`
