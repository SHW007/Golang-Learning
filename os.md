os提供了操作系统交互的功能，如文件操作、环境变量获取等。

os.Chdir(dir string) error
    Chdir将当前工作目录更改为指定目录。如果有一个错误，它的类型将是*PathError。
os.Chmod(name string, mode FileMode) error
    Chmod命令将指定文件的模式修改为mode。如果文件是一个符号链接，它会改变链接目标的模式。如果有一个错误，它的类型将是*PathError。
os.Chown(name string, uid, gid int) error
    Chown更改命名文件的数字uid和gid。如果文件是一个符号链接，它会更改链接目标的uid和gid。uid或gid为-1表示不更改该值。如果有一个错误，它的类型将是*PathError。
os.Chtimes(name string, atime time.Time, mtime time.Time) error
    Chtimes 会更改指定文件的访问时间atime和修改时间mtime，。如果传入的时间值为零，则会保持文件的时间不变。
os.Clearenv()
    Clearenv删除所有环境变量。
os.CopyFS(dir string, fsys fs.FS) error
    CopyFS将文件系统fsys复制到目录dir中，必要时创建dir。
os.DirFS(dir string) fs.FS
    DirFS返回一个文件系统（fs）。FS)用于目录dir下的文件树。
os.Environ() []string
    Environ以“key=value”的形式返回一个表示环境的字符串副本。
os.Executable() (string, error)
    Executable返回启动当前进程的可执行文件的路径名。


    