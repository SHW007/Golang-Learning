cmp  提供了与比较有序值相关的类型和函数。

cmp.Compare[T Ordered](x, y T) int
    比较x和y
    -1 if x is less than y,
     0 if x equals y,
    +1 if x is greater than y.

cmp.Less[T Ordered](x, y T) bool
    判断x是否小于y

cmp.Or[T comparable](vals ...T) T
    返回第一个不为0值的参数
