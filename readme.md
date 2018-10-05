为什么感知机的更新公式是$\vec{w} ← \vec{w}+\eta y_i\vec{x_i}$ 或

 $\vec{w} ← \vec{w}+\eta y_i\vec{x_i}$ 

$b ← b+\eta y_i$ 

答：在感知机迭代过程里面，只更新错误的点，只要 $\vec{w}^T\vec{x_i} + b​$ 和 $y_i​$ 符号不同就更新它，时常是用$y_i(\vec{w}^T\vec{x_i} + b)​$ 小于零来表示分类错误。更新的目标是让它有变大的趋向，因为希望最后它是大于0的
$$
y_i(w_{新}^Tx_i\ +\ b_新) = y_i((w_旧 + \eta y_ix_i)^Tx_i + b_旧 + \eta y_i)\\
=y_i(w_旧^Tx_i + b_旧 + (\eta y_i)x_i^Tx_i + \eta y_i)\\
=y_i(w_旧^Tx_i + b_旧) + (\eta y_i^2)(x_i^2 + 1)
$$
更新完的值是旧值加了一个大于零的值，所以趋向于更正确的分类



