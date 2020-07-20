#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a)

Constant O(1)

The runtime or space used is unaffected by the size/numeric value of 'n'

b)

Linear O(n)

As the size/numeric value of 'n' increases, the runtime or space used will grow at the same rate.

c)

Exponential O(c^n)

As the size/numeric value of 'n' increases, the runtime or space used will grow at a much faster rate

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

Understand -

    If I drop an egg higher then floor (f) it will break.
    If I drop the egg lower than floor (f) it won't

    Solution: Find at which floor (f) is the number of broken eggs at a minimum

    Question:
    Do we already know how many eggs are broken at each floor - or are we dropping them as part of this alogrithm?
    How many eggs are we dropping?
    Does the size of the egg matter?

    Inputs:
    1. Egg
    2. Floor

    Output:
    1. Boolean (Broken Egg)

Plan -

    I'm assuming that we are dropping an egg at each floor.

    This plan reminds me of the cookie monster in that we need to record if the egg we dropped at floor (f) broke or not.  We could memoize the counter.

    So, we'd cycle through each floor - dropping an egg on each floor and recording if the egg broke or not.

    pseudo code -

    would do a recursive function

    def floorCounter(f, chache):

        base case
        if floor (f) == 0:
            return the (f) key with the minimum value

        if dropEggBroken():
            if in cache:
                cache[f] = cache[f]+1
            else:
                cache[f] = 1

        floorCounter(f-1, cache)
