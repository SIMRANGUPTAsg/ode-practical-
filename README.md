# ode-practical-
variation of parametre 
1 
homeqn = y''[x] - 7 y'[x] + 10 y[x] == 0
RHS = 6 E^(3 x)
2
sol = DSolve[homeqn, y, x]
3
y1 = y[x] /. sol[[1]] /. {C[1] -> 1, C[2] -> 2}
y2 = y[x] /. sol[[1]] /. {C[1] -> 2, C[2] -> 1}
4
w = Wronskian[{y1, y2}, x]
5
v1 = -Integrate[y2*RHS/w, x]
6
v2 = Integrate[y1*RHS/w, x]
7
PI = Simplify[y1 v1 + y2 v2]
8
Final = sol + PI

3rd degre homo equation 
sol = DSolve[y'''[x] - 5 y''[x] + 3 y'[x] + 9 y[x] == 0, y[x], x]
Plot[y[x] /. sol /. {C[1] -> Range[-4, 4], C[2] -> Range[-4, 4], 
   C[3] -> Range[-4, 4]}, {x, 0, 5}]
   
