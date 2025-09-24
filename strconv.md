strconv   实现了基本数据类型与其字符串表示的转换
strconv.Atoi(s string) (i int, err error)
    将字符串类型的整数转换为int类型
strconv.Itoa(i int) string
    将int类型数据转换为对应的字符串表示
strconv.ParseBool(str string) (value bool, err error)
    返回字符串表示的bool值。它接受1、0、t、f、T、F、true、false、True、False、TRUE、FALSE；否则返回错误。
strconv.ParseInt(s string, base int, bitSize int) (i int64, err error)
    返回字符串表示的整数值，接受正负号。
    **s string**​：要解析的字符串
    ​**base int**​：进制基数（2-36）
    ​**bitSize int**​：目标整数类型的大小（0, 8, 16, 32, 64）
    ​**i int64**​：解析后的整数值
    ​**err error**​：解析过程中遇到的错误
strconv.ParseUint(s string, base int, bitSize int) (n uint64, err error)
    类似ParseInt但不接受正负号，用于无符号整型。
strconv.ParseFloat(s string, bitSize int) (f float64, err error)
    解析一个表示浮点数的字符串并返回其值。


strconv.FormatBool(b bool) string
    根据b的值返回”true”或”false”。
strconv.FormatInt(i int64, base int) string
    返回i的base进制的字符串表示。base 必须在2到36之间，结果中会使用小写字母’a’到’z’表示大于10的数字。
strconv.FormatInt(i int64, base int) string
    返回i的base进制的字符串表示。base 必须在2到36之间，结果中会使用小写字母’a’到’z’表示大于10的数字。
strconv.FormatUint(i uint64, base int) string
    FormatInt的无符号整数版本。
strconv.FormatFloat(f float64, fmt byte, prec, bitSize int) string
    将浮点数表示为字符串并返回。