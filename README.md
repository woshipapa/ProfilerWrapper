# ProfilerWrapper
主要用于对pytorch profiler的包装，方便保存为trace.json文件去可视化，或者对profiler收集的数据进行自定义的画图打印等操作


### _init_
初始化时，可以指定profiler要记录的activities，是否要启用profiler的profile_memory功能，以及是否要启用Pytorch的snapshot内存分析

并且初始化了要绘图的数据，cuda_times和fa_times。

### _exit_
在每次离开with块时，会将当前profiler到的数据加入到cuda_times列表中，以便后续的数据统计和可视化


### leave
leave方法中可以定义最后需要进行的操作，比如绘图可视化，保存trace文件，dump & close snapshot


