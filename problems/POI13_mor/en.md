Young Bytensson loves to hang out in the port tavern, where he often listens to the sea dogs telling their tales of seafaring. Initially, he believed them all, however incredible they sounded. Over time though, he became suspicious. He has decided to write a program that will verify if there may be any grain of truth in those tall stories. Bytensson reasoned that while he cannot tell if the sailors indeed weathered all those storms, he can at least find out if their travel itineraries make sense. This is a task for a programmer, which Bytensson, unfortunately, is not. Help him out!

There are n ports and m waterways connecting them in the waters frequented by the sailors Bytensson listened to. If there is a waterway between two ports, then sailing from one to the other is possible. Any waterway can be sailed in **both directions**.

Bytensson got to know $k$ seafaring tales. Each tells of a sailor who began his journey in one port, sailed a number of waterways, and ended up in another port, which may have been the one he initially set sail from. The sailor in question may have sailed through the same waterway many times, each time in any direction.

### Input

In the first line of the standard input, there are three integers, $n$, $m$, and $k$ ($2 \le n \le 5\,000$, $1 \le m \le 5\,000$, $1 \le k \le 1\,000\,000$). These denote, respectively: the number of ports in the waters frequented by the sailors who told Bytensson their stories, the number of waterways, and the number of tales.

The $m$ lines that follow specify the waterways. A single waterway's description consists of a single line that contains two integers, $a$ and $b$ ($1 \le a,b \le n$, $a \neq b$), separated by a single space; these specify the numbers of ports at the two ends of this particular waterway.

The $k$ lines that follow specify the tales that Bytensson has heard. A single tale's description consists of a single line with three integers, $s$, $t$, and $d$ ($1 \le s,t \le n$, $1 \le d \le 1\,000\,000\,000$), separated by single spaces. These indicate that the tale's protagonist set sail from port no. $s$, ended the journey in port no. $t$, and sailed **exactly** $d$ times through various waterways.

In tests worth 50% of the total points, the additional condition $n \le 800$  holds.

### Output

Your program should print exactly $k$ lines to the standard output; the $i$-th of them should contain the word `TAK` (Polish for *yes*) if the journey described in the $i$-th tale (in input order) could have taken place. If it could not, then the line should contain the word `NIE` (Polish for *no*).

### Example

For the input data:

```
8 7 4
1 2
2 3
3 4
5 6
6 7
7 8
8 5
2 3 1
1 4 1
5 5 8
1 8 10
```

the correct result is:

```
TAK
NIE
TAK
NIE
```

![](https://attach.oj.uz/problems/jas62k6l6gmwun4i734wkga084562zxb/morrys-crop.gif)

*Task author: Wiktor Kuropatwa.*