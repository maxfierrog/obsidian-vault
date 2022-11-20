**Sunday Nov 20, 2022** #math 

---

### Objective

Develop strategies to count elements in a set.

---

### Rules of Counting

1. If an element can be made by a succession of $k$ choices, where there are $n_{i}$ ways of making the $i$'th choice for every way of making the previous choice, then the total number of distinct elements that can be made in this way is $n_{1} \times n_{2} \times n_{3} \times \dots \times n_{k}$. 

3. If an element is made by a succession of choices whose order does not matter, we can count the number of objects pretending order does matter, and then divide by the amount of extra elements we count for every choice where we pretend order does matter. 

5. If there is a bijection between two sets, they are of the same magnitude (obviously).

---

### Sampling With Replacement

Scenario where we count the number of ways of constructing $k$-length elements out of a set $S$ of pieces, where every time we take one out of the set it is still available to be used (we replace it every time we take it out).
$$
|O| = |S|^k
$$

---

### Sampling Without Replacement

Scenario where we do the same thing, but we can no longer use a piece after we put it into an element we are constructing.
$$
|O| = \frac{|S|!}{(|S| - k)}
$$

---

### Sampling With Replacement Without Order

Scenario where we do the same thing, but we do not care about the order in which the elements appear. For example, the number of 5-fruit baskets you can make with $A$ apples, $B$ bananas, and $C$ oranges.

To do this, we picture a balls-and-bins scenario, where we have three bins (one for each type of fruit) and 5 balls (the amount of fruits in our possible baskets). Then, we count the amount of ways to throw 5 balls into 3 bins.

To do this, we add an extra two balls, and choose two of them to be 'dividers'. Then, there will be three intervals of balls separated by dividers, which represent each bin. This is a bijection to the original problem, so it works.

$$
|O| = {5 + 2 \choose 2}
$$

---

### The Principle of Inclusion-Exclusion

This essentially deals with counting the right amount of things in a union. We know that we overcount intersections, so this boils down to subtracting what we overcount. For example, when we have two sets $S_{1}$ and $S_{2}$,

$$
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}| - |S_{1} \cap S_{2}|
$$
