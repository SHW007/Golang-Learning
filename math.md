math 提供基本的常量和数学函数。

math.Abs(x float64) float64
    绝对值 Abs(NaN) = NaN
math.Acos(x float64) float64
    arccos 单位是弧度
math.Asin(x float64) float64
    arcsin
math.Atan(x float64) float64
    arctan
math.Cbrt(x float64) float64
    立方根
math.Ceil(x float64) float64
    回>=x的最小整数值。
math.Cos(x float64) float64
    cos
math.Erf(x float64) float64
    返回x的误差函数。
math.Erfc(x float64) 
    返回x的互补误差函数。
math.Exp(x float64) float64
    e^x
math.Exp2(x float64) float64
    2^x
math.Expm1(x float64) float64
    返回e^x - 1
math.FMA(x, y, z float64) float64
    返回x * y + z，只计算一次四舍五入。
math.IsNaN(f float64) (is bool)
    是否为非数字
math.Log(x float64) float64
    log以e为底
math.Log10(x float64) float64
    以10为底
math.Log1p(x float64) float64
    log(1+x)
math.Max(x, y float64) float64
    返回大的值
math.Min(x, y float64) float64
    返回小的值
math.Mod(x, y float64) float64
    返回x%y的浮点余数，其符号与x的符号一致
math.Modf(f float64) (int float64, frac float64)
    拆分整数和小数，符号与f相同
math.Sin(x float64) float64
    sin
math.Sqrt(x float64) float64
    平方根
math.Tan(x float64) float64
    tan






math.Asinh(x float64) float64
    反双曲sinx
math.Atan2(y, x float64) float64
    Atan2返回y/x的反正切
math.Atanh(x float64) float64
    返回x的逆双曲正切
math.Copysign(f, sign float64) float64
    返回一个大小为f且符号为sign的值。
math.Cosh(x float64) float64
    双曲正弦
math.Dim(x, y float64) float64
    Dim返回x-y的最大值或0。
math.Erfcinv(x float64) float64
    返回Erfc(x)的倒数。
math.Erfinv(x float64) float64
    返回x的误差逆函数。
math.Acosh(x float64) float64
    反双曲cos (x)
math.Float32bits(f float32) uint32
    返回f的IEEE 754二进制表示形式，其中f的符号位和结果在相同的位位置。
math.Float32frombits(b uint32) float32
    返回与IEEE 754二进制表示b对应的浮点数，b的符号位和结果位位置相同。
math.Float64bits(f float64) uint64
math.Float64frombits(b uint64) float64
math.Floor(x float64) float64
math.Frexp(f float64) (frac float64, exp int)
    将f分解为标准化分数和2的积分幂。
math.Gamma(x float64) float64
    返回 x 的伽马函数值
math.Hypot(p, q float64) float64
    returns Sqrt(p*p + q*q)
math.Ilogb(x float64) int
    以整数形式返回x的二进制指数。
math.Inf(sign int) float64
    如果符号>= 0，则Inf返回正无穷，如果符号< 0则返回负无穷。