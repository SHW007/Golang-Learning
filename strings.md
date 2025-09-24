strings 实现简单的函数来操作UTF-8编码的字符串。

strings.Clone(s string) string
    返回字符串 s 的全新副本。它确保将字符串 s 复制到一个新的内存分配中

strings.Compare(a, b string) int
    按字典顺序比较两个字符串。

strings.Contains(s, substr string) bool
    报告substr是否在s内。

strings.ContainsAny(s, chars string) bool
    s中是否有chars的字母，有就true

strings.Count(s, substr string) int
    Count计算s中substr的非重叠实例的个数。如果substr为空字符串，Count返回1 + s中Unicode码点的个数。

strings.EqualFold(s, t string) bool
    比较s和t，不区分大小写

strings.Fields(s string) []string
    按空格拆分字符串，返回切片

strings.HasPrefix(s, prefix string) bool
    检查s是否以prefix开头

strings.HasSuffix(s, suffix string) bool
    检查s是否以suffix结尾

strings.Join(elems []string, sep string) string
    Join将其第一个参数的元素连接起来以创建单个字符串。分隔字符串sep放置在结果字符串的元素之间。

strings.Map(mapping func(rune) rune, s string) string
    Map返回字符串s的副本，其中所有字符都根据映射函数进行了修改。如果映射返回负值，则从字符串中删除该字符，不进行替换。

strings.Replace(s, old, new string, n int) string
    Replace返回字符串s的副本，其中旧的前n个不重叠的实例替换为new。

strings.Split(s, sep string) []string
    将切片拆分为所有以sep分隔的子字符串，并返回分隔符之间的子字符串切片。

strings.SplitSeq(s, sep string) iter.Seq[string]
    SplitSeq返回一个遍历以sep分隔的s的所有子字符串的迭代器。迭代器产生与Split（s, sep）返回的字符串相同的字符串，但不构造切片。它返回一个单用途迭代器。
    
