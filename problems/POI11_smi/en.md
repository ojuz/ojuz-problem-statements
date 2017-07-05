The Byteotian Waste Management Company (BWMC) has drastically raised the price of garbage collection lately. This caused some of the citizens to stop paying for collecting their garbage and start disposing of it in the streets. Consequently, many streets of Byteburg are literally buried under litter.

The street system of Byteburg consists of $n$ intersections, some of which are directly connected with bidirectional streets. No two streets connect the same pair of intersections. Some of the streets are littered while others are not.

The mayor of Byteburg, Byteasar, has decided on an unprecedented action to persuade the citizens to pay for waste collection. Namely, he decided to clean only some of the streets - precisely those that the majority of people living on paid for garbage collection. The streets that the majority of people living on did not pay for waste collection, on the other hand, will thus remain littered - or if it is called for - will become littered by the garbage collected from other streets! Byteasar has already prepared a city map with the streets to be cleaned and to remain or become littered marked on. Unfortunately, the BWMC employees cannot comprehend his master plan. They are, however, quite capable of carrying out simple instructions.

A single such instruction consists in driving the garbage truck along a route that starts on an arbitrary intersection, goes along any streets of choice, and ending on the very same intersection that it started on. However, every intersection can be visited at most once on a single route, except for the one it starts and ends with-the garbage truck obviously appears twice on that one. The truck cleans a littered street it rides along, but on the other hand it dumps the waste on the clean streets along its route, making them littered.

Byteasar wonders if it is possible to execute his plan by issuing a number of aforementioned route instructions. Help him out by writing a program that determines a set of such routes or concludes that it is impossible.

### Input

There are two integers, separated by a single space, in the first line of the standard input: $n$ and $m$ ($1 \le n \le 100\,000$, $1 \le m \le 1\,000\,000$), denoting the number of intersections and the number of streets in Byteburg, respectively. The intersections are numbered from $1$ to $n$. The following m lines specify successive streets, one per line. Each of those lines holds four integers separated by single spaces: $a$,$b$,$s$ and $t$ ($1 \le a < b \le n$, $s,t \in \{0,1\}$). Such a quadruple specifies that the intersections $a$ and $b$ are connected with a street, $s$ tells if the street is currently littered ($0$ means clean, while $1$ means littered), and $t$ tells if the street should be littered according to Byteasar's plan.

You may assume that if there exists a set of routes to carry out Byteasar's plan, then there is one in which the total number of streets that the garbage truck follows does not exceed $5 \cdot m$.

In tests worth 60% of the points it additionally holds that $m \le 10\,000$.

### Output

If there is no set of routes for the garbage truck to execute Byteasar's plan, then the word "`NIE`" (*no* in Polish) should be printed out to the first and only line of the standard output. Otherwise, an arbitrary set of routes that does execute Byteasar's plan and has the truck move along no more than $5 \cdot m$ streets in total should be printed out. Then the first line should hold the number $k$ of routes in the set. The following $k$ lines should describe the routes, one per line. The $(i+1)$-th line should start with a positive integer $k_i$ equal to the number of streets in the $i$-th route. After a single space, $k_{i+1}$ numbers of successive intersections along the route should follow, separated by single spaces.

### Example

The clean streets are drawn with a thin line in the figure, whereas the littered streets are drawn with a thick line. The streets that are to be clean are drawn with a dashed line, while those that are to be littered are drawn with a solid line.

For the input data
```
6 8
1 2 0 1
2 3 1 0
1 3 0 1
2 4 0 0
3 5 1 1
4 5 0 1
5 6 0 1
4 6 0 1
```

![]([[file:smizad1.gif]])

one of correct results is:
```
2
3 1 3 2 1
3 4 6 5 4
```
whereas for the following input data:
```
6 8
1 2 0 1
2 3 1 0
1 3 0 1
2 4 0 0
3 5 1 1
4 5 0 1
5 6 0 1
4 6 0 0
```

![]([[file:smizad2.gif]])

the correct result is:
```
NIE
```

*Task author: Michal Pilipczuk.*