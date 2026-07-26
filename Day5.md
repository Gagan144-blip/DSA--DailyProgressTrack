## Maximum Difference Between Even and Odd Frequency I:

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
