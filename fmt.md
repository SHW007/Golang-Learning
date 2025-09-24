#### fmt.

`fmt.Append(b []byte, a ...any) []byte`
- 使用其操作数的默认格式追加格式，将结果追加到字节片，并返回更新后的片。
fmt. Appendf(b []byte, format string, a ...any) []byte
    Appendf根据格式说明符进行格式化，将结果追加到字节片，并返回更新后的片。
fmt. Appendln(b []byte, a ...any) []byte
    与append类似，但会追加换行符

fmt.Errorf(format string, a ...any) error
    Errorf根据格式说明符进行格式化，并返回字符串作为满足error的值。

fmt.FormatString(state State, verb rune) string
    FormatString返回一个字符串，表示State捕获的完全限定格式指令，后跟参数动词。

    Fprint系列函数会将内容输出到一个io.Writer接口类型的变量w中，我们通常用这个函数往文件中写入内容。
fmt.Fprint(w io.Writer, a ...any) (n int, err error)
    Fprint使用其操作数的默认格式进行格式化，并写入w。当两个操作数都不是字符串时，在操作数之间添加空格。它返回写入的字节数和遇到的任何写入错误。
fmt.Fprintf(w io.Writer, format string, a ...any) (n int, err error)
fmt.Fprintln(w io.Writer, a ...any) (n int, err error)

    从io.Reader中读取数据
fmt.Fscan(r io.Reader, a ...any) (n int, err error)
    Fscan扫描从r读取的文本，将连续的空格分隔值存储到连续的参数中。换行符算作空格。它返回成功扫描的项目数。如果少于参数的数量，err将报告原因。
fmt.Fscanf(r io.Reader, format string, a ...any) (n int, err error)
fmt.Fscanln(r io.Reader, a ...any) (n int, err error)

    Print系列函数会将内容输出到系统的标准输出
fmt.Print(a ...any) (n int, err error)
    使用其操作数的默认格式打印格式，并写入标准输出。当两个操作数都不是字符串时，在操作数之间添加空格。它返回写入的字节数和遇到的任何写入错误。
fmt.Printf(format string, a ...any) (n int, err error)
fmt.Println(a ...any) (n int, err error)

    可以在程序运行过程中从标准输入获取用户的输入
fmt.Scan(a ...any) (n int, err error)
    Scan扫描从标准输入读取的文本，将连续的空格分隔值存储到连续的参数中。换行符算作空格。它返回成功扫描的项目数。
fmt.Scanf(format string, a ...any) (n int, err error)
fmt.Scanln(a ...any) (n int, err error)

    Sprint系列函数会把传入的数据生成并返回一个字符串。
fmt.Sprint(a ...any) string
    Sprint用于将任意类型的数据转换为字符串。将所有参数格式化后拼接成的字符串。不打印
fmt.Sprintf(format string, a ...any) string
fmt.Sprintln(a ...any) string

    从指定字符串中读取数据
fmt.Sscanln(str string, a ...any) (n int, err error)
    扫描参数字符串，将连续的空格分隔值存储到连续的参数中。换行符算作空格。它返回成功扫描的项目数。如果少于参数的数量，err将报告原因。
fmt.Sscanf(str string, format string, a ...any) (n int, err error)
    fmt.Sscanf("Kim is 22 years old", "%s is %d years old", &name, &age)将str中的字符串按照format中指定的存到a中
fmt.Sscanln(str string, a ...any) (n int, err error)
    Sscanln类似于scan，但是在一个换行符处停止扫描，并且在最后一个项目之后必须有一个换行符或EOF。

%b	base 2
%c	the character represented by the corresponding Unicode code point
%d	base 10
%o	base 8
%O	base 8 with 0o prefix
%q	a single-quoted character literal safely escaped with Go syntax.
%x	base 16, with lower-case letters for a-f
%X	base 16, with upper-case letters for A-F
%U	Unicode format: U+1234; same as "U+%04X"
%s	the uninterpreted bytes of the string or slice
%q	a double-quoted string safely escaped with Go syntax
%x	base 16, lower-case, two characters per byte
%X	base 16, upper-case, two characters per byte
bool:                    %t
int, int8 etc.:          %d
uint, uint8 etc.:        %d, %#x if printed with %#v
float32, complex64, etc: %g
string:                  %s
chan:                    %p
pointer:                 %p

