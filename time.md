time 时间的显示和测量用的函数

time.Now()
    获取当前的时间对象
    / 格式化的模板为 2006 年 1 月 2 号 15 点 04 分
    fmt.Println(now.Format("2006-01-02 15:04:05")) 打印出24小时制
now.Unix()
    获取时间戳
    Unix:秒
    UnixNano:纳秒
time.Unix()
    将时间戳转为时间格式
time.NewTicker()
    设定定时器
    time.NewTicker(time.Second) //定义一个 1 秒间隔的定时器
time.Sleep(time.Second)
