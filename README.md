# Stochastic-Optimization
MATLAB program to find the optimal policy

Suppose X={1,2}, 
U
=
{
1
,
2
,
3
}
, and 
W
=
{
1
,
2
,
3
}
. Let 
(
X
,
W
)
 be random variables taking values in 
X
×
W
 with joint distribution 
P
 shown below.


P
=
[
0.25	0.15	0.05	0.30	0.10	0.15 
]

Here the row corresponds to the value of 
x
 and the column corresponds to the value of 
w
. For example 
P
(
X
=
2
,
W
=
1
)
=
P
21
=
0.30
.

The cost function 
c
:
X
×
U
×
W
→
R
 is shown below


c
(
⋅
,
⋅
,
1
)
=
[
3	5	1	2	3	1 
]
,
c
(
⋅
,
⋅
,
2
)
=
[
4	3	1	1	2	8 
]
,
c
(
⋅
,
⋅
,
3
)
=
[
1	2	2	4	1	3 
]
.

Here the row corresponds to the value of 
x
 and the column corresponds to the value of 
u
. For example 
c
(
x
=
1
,
u
=
2
,
w
=
1
)
=
5
.

Find the policy 
g
:
X
→
U
 that minimizes 
E
[
c
(
X
,
g
(
X
)
,
W
)
]
.
