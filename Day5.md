## Neetcode: Maximum Difference Between Even and Odd Frequency I:

Your task is to find the maximum difference diff = freq(a1) - freq(a2) between the frequency of characters a1 and a2 in the string such that:

    a1 has an odd frequency in the string.
    a2 has an even frequency in the string.

Return this maximum difference.

#### Mistake : it.first is the character, not its frequency
In:

#### for(auto it : mp)

If the map contains:

'a' → 5
'b' → 2
'c' → 1

Then:

it.first   // character: 'a'
it.second  // frequency: 5

So this is wrong:

diff = it.first - it.second;

Because you are doing:

#### character - frequency

You need to compare frequencies.
- so i have to do EvenFreq - OddFreq;

### in hashMaps for loop:
for(auto it : mp)
here:
- it.first = Character
- it.second = frequency of charcter;

### maxOdd and minEven:
for maxOdd 
max(maxOdd, freq)

for minOdd 
min(minOdd, freq)



## Problem 387 : First Unique Character in a String:

In this problem, we have to find the first unique character, which means the first character that appears only once in the string.

My Approach:
First, I used map<char, int> to count the frequency of every character.
Then, I traversed the original string from left to right.
For every character, I checked its frequency using mp[s[i]].
If the frequency is 1, it means the character appears only once, so I returned its index

Important Learning:
mp[s[i]]
is used to retrieve the frequency of the character at index i.

For example:
s = "leetcode"

mp['l'] = 1
mp['e'] = 3
So:

if(mp[s[i]] == 1)
means:
If the current character appears exactly once in the string, return its index.

#### Mistake:
Mistake/Confusion:

Initially, I was confused about using > 1, but unique means exactly one occurrence, so we use:

mp[s[i]] == 1

Also, directly traversing a map gives characters in sorted order, not their original order in the string. Therefore,
to find the first unique character, we need to traverse the original string again.
