### Day 1

Straightforward. Mistakenly over part1 with part2. I enjoyed the small optimization made when comparing 'average' depth for part2. Instead of recalculating three number sums in each iteration, I opted to copy the current depth to 'prev' and update the new depth via curr = prev - input[i-3] + input[i];

### Day 2

Straightforward. Not much to say here!

### Day 3

Really enjoyed this one! Building a trie was a fun solution and the idea came to me pretty quickly! Definitely had to refactor it once or twice, but we made it there in the end and the final Trie class and main() look really clean.

### Day 4

A good exercise in OOP, I did well, but there were definitely some improvements that could be had.

I got some great feedback from someone on ways to improve this solution:

> You have some needless copies e.g. copying boards[draw] to toBeMarked;
> When passing in read-only references to functions always use const otherwise you don't know if the function will mutate it
> Since you seem to be making an attempt to make it efficient with the unordered_map stuff, why not store the index of the number in the map too? you can have unordered_map<int, vector<tuple<Board\*, size_t, size_t>>>
> You seem to be using hardcoded sentinel values like -5, best to put those in a > constexpr constant at the top of some file. also your code will fail if there are negative numbers in the input
> Also you have trivial getters which are not good: https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Rh-get
> Better to make a const member if you want something to be read-only
> Your getVals function has for (int j=0; j < this->board[0].size(); j++) { instead of board[i].size() but nowhere do you seem to check that each row is the same length

### Day 5

Really sloppy with this one. Not proud of it either. The plus side is that I took a moment to finally learn a bit about regex! ...even if the regex I ended up writing was extremely basic.

### Day 6

This was a fun one. Used direct simulation for part 1. Part 2 completely tore that apart thanks to exponential explosion. The fix came within a few seconds of thought, which I'm pretty happy about. Anyways, not a bad day overall.