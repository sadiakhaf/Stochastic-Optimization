# Stochastic-Optimization
MATLAB program to find the optimal policy
The questions can be found here: https://adityam.github.io/stochastic-control/assignments/01/

Suppose X={1,2}, U={1,2,3}, and W={1,2,3}
. Let (X,W) be random variables taking values in 
X×W with joint distribution P shown below.

P = [ 0.25  0.15  0.05  ; 0.30  0.10  0.15 ]

Here the row corresponds to the value of x and the column corresponds to the value of w. For example P(X=2,W=1)=P21=0.30.
The cost function c:X×U×W→R is shown below
 
 c(⋅,⋅,1)=[3	5	1	2	3	1 ],c(⋅,⋅,2)=[4	3	1	1	2	8 ],c(⋅,⋅,3)=[1	2	2	4	1	3 ]. Here the row corresponds to the value of x and the column corresponds to the value of u. For example c(x=1,u=2,w=1)=5. Find the policy g:X→U that minimizes E[c(X,g(X),W)].
 
 %%%%%%%%%%%%%% ELEC 5 0 6 A s s i g n m e n t −1 %%%%%%%%%%%%%%%%%%% 
 % Submitted by: Sadia Khaf %  
 %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
clear all , close all , clc
%%%%%%%%%% P r o b l e m −1 %%%%%%%%%%%%%%%%%% 
% Defining given information
X=[1,2];
U= [1,2,3];
W=[1,2,3];
P xw = [0.25 0.15 0.05;0.30 0.10 0.15]; c xu1 = [3 5 1;2 3 1];
c xu2 = [4 3 1;1 2 8];
c xu3 = [1 2 2;4 1 3];
%J(g)=E[c(X,g(X),W)] %mingE[c(X,g(X),W)]
% gˆ∗(x) = arg min u \in U E[c(x,u,W)|X=x] % gˆ∗(1) = arg min u \in U E[c(1,u,W)|X=1] % gˆ∗(2) = arg min u \in U E[c(2,u,W)|X=2]
E 1uw = [c xu1(1,:);c xu2(1,:);c xu3(1,:)]∗P xw(1,:) ’/sum( P xw ( 1 , : ) ) ;
E 2uw = [c xu1(2,:);c xu2(2,:);c xu3(2,:)]∗P xw(2,:) ’/sum( P xw ( 2 , : ) ) ;
[val gstar] = min([E 1uw,E 2uw] ,[] ,1)
% gstar comes out to be 3,1 for the values given in the
question
