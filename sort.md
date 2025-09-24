sort 提供了对片和用户定义集合进行排序的原语。

sort.Find(n int, cmp func(int) int) (i int, found bool)
在**有序序列**中查找满足特定条件的元素
**n int**: 序列长度（索引范围 [0, n-1]）
​**cmp func(int) int**: 自定义比较函数，接受索引参数
​**i int**: 找到的索引位置或应插入位置
​**found bool**: 是否找到精确匹配

sort.Search(n int, f func(int) bool) int
在**有序序列**中查找满足特定条件的最小索引位置
​**n int**: 序列长度（索引范围 [0, n-1]）
​**f func(int) bool**: 判断函数，接受索引参数，返回布尔值
**​返回值 int**: 满足条件的最小索引（或 n 如果不存在）
i := sort.Search(len(a), func(i int) bool { return a[i] >= x })  切片按照升序
i := sort.Search(len(a), func(i int) bool { return a[i] <= x })  切片按照降序


sort.SearchFloat64s(a []float64, x float64) int
在float64s的排序切片中搜索x，并返回由Search指定的索引。如果x不存在，返回值是插入x的索引（可以是len(a)）。切片必须按**升序**排序。

/////////////////////////////////////
slices定义了对任何类型的片都有用的各种函数。

slices.BinarySearch[S ~[]E, E cmp.Ordered](x S, target E) (int, bool)
BinarySearch在已排序的切片中搜索目标，并返回找到目标的最早位置，或者目标在排序顺序中出现的位置；它还返回一个bool值，表示是否真的在切片中找到目标。切片必须按**递增顺序**排序。
**S ~[]E**: 切片类型约束，表示任何元素类型为 E 的切片
​**E cmp.Ordered**: 元素类型约束，必须是可比较的有序类型（实现了 cmp.Ordered 接口）
​**x S**: 要搜索的有序切片（必须升序排序）
​**target E**: 要查找的目标值

slices.Clone[S ~[]E, E any](s S) S
    克隆返回片的副本。元素是使用赋值复制的，所以这是一个浅克隆。结果可能会产生额外的未使用容量。结果保留了s的病态性。
slices.Concat[S ~[]E, E any](slices ...S) S
    Concat返回一个新的切片，将传入的切片连接起来。如果串联为空，则结果为nil。
slices.Contains[S ~[]E, E comparable](s S, v E) bool
    报告v是否存在于s中。
slices.ContainsFunc[S ~[]E, E any](s S, f func(E) bool) bool
    按func中的函数查找报告s中是否至少有一个元素e满足f(e)
slices.Delete[S ~[]E, E any](s S, i, j int) S
    Delete从s中删除元素s[i:j]，返回修改后的片。
slices.DeleteFunc[S ~[]E, E any](s S, del func(E) bool) S
    DeleteFunc从s中删除del返回true的所有元素，返回修改后的切片。
slices.Equal[S ~[]E, E comparable](s1, s2 S) bool
    Equal报告两个片是否相等：长度相同且所有元素相等。
slices.Grow[S ~[]E, E any](s S, n int) S
    增加切片容量使其能容纳增加n个元素
slices.Index[S ~[]E, E comparable](s S, v E) int
    Index返回v在s中第一次出现的索引，如果不存在则返回-1。
slices.Insert[S ~[]E, E any](s S, i int, v ...E) S
    对于切片s，在索引i处插入v
slices.Max[S ~[]E, E cmp.Ordered](x S) E
    返回x中的最大值。
slices.Min[S ~[]E, E cmp.Ordered](x S) E
    Min返回x中的最小值。
slices.Repeat[S ~[]E, E any](x S, count int) S
    Repeat返回一个新切片，该切片重复给定次数的提供的切片。
slices.Reverse[S ~[]E, E any](s S)
    反转s切片中的元素
slices.Sort[S ~[]E, E cmp.Ordered](x S)
    Sort按升序对任意有序类型的切片进行排序。

