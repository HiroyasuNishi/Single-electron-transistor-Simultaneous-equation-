# Single-electron-transistor-Simultaneous-equation-
# ナノ科学第３回レポート
import sympy

# q1, q2, qg, n, e, C1, C2, Cg, V, Vg = sympy.symbols(['q1', 'q2', 'qg', 'n', 'e', 'C1', 'C2', 'Cg', 'V', 'Vg'])　これでもできる
q1, q2, qg, n, e, C1, C2, Cg, V, Vg = sympy.symbols('q1 q2 qg n e C1 C2 Cg V Vg')
sympy.init_printing()

x = q1-q2-qg+n*e
y = q1/C1+qg/Cg-Vg-V/2
z = -q2/C2+qg/Cg-Vg+V/2

sympy.solve([x,y,z], [q1, q2, qg])
