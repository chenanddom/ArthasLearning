# Arthas

## Linux中top命令的学习
top 命令通常用来监控linux的系统状况。
top - 18:40:26 up 1 day, 19 min,  2 users,  load average: 0.00, 0.01, 0.05
Tasks: 107 total,   1 running, 106 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
KiB Mem :   995896 total,   176724 free,   330460 used,   488712 buff/cache
KiB Swap:  2097148 total,  2097148 free,        0 used.   472200 avail Mem 

   PID USER      PR  NI    VIRT    RES    SHR S %CPU %MEM     TIME+ COMMAND                                                                                                                                                                     
     1 root      20   0  127968   6536   4132 S  0.0  0.7   0:03.06 systemd                                                                                                                                                                     
     2 root      20   0       0      0      0 S  0.0  0.0   0:00.01 kthreadd                                                                                                                                                                    
     3 root      20   0       0      0      0 S  0.0  0.0   0:00.43 ksoftirqd/0                                                                                                                                                                 
     5 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kworker/0:0H                                                                                                                                                                
     7 root      rt   0       0      0      0 S  0.0  0.0   0:00.00 migration/0                                                                                                                                                                 
     8 root      20   0       0      0      0 S  0.0  0.0   0:00.00 rcu_bh                                                                                                                                                                      
     9 root      20   0       0      0      0 S  0.0  0.0   0:00.72 rcu_sched                                                                                                                                                                   
    10 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 lru-add-drain                                                                                                                                                               
    11 root      rt   0       0      0      0 S  0.0  0.0   0:00.23 watchdog/0                                                                                                                                                                  
    13 root      20   0       0      0      0 S  0.0  0.0   0:00.00 kdevtmpfs                                                                                                                                                                   
    14 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 netns                                                                                                                                                                       
    15 root      20   0       0      0      0 S  0.0  0.0   0:00.01 khungtaskd                                                                                                                                                                  
    16 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 writeback                                                                                                                                                                   
    17 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kintegrityd                                                                                                                                                                 
    18 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 bioset                                                                                                                                                                      
    19 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 bioset                                                                                                                                                                      
    20 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 bioset                                                                                                                                                                      
    21 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kblockd                                                                                                                                                                     
    22 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 md                                                                                                                                                                          
    23 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 edac-poller                                                                                                                                                                 
    24 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 watchdogd                                                                                                                                                                   
    30 root      20   0       0      0      0 S  0.0  0.0   0:00.00 kswapd0                                                                                                                                                                     
    31 root      25   5       0      0      0 S  0.0  0.0   0:00.00 ksmd                                                                                                                                                                        
    32 root      39  19       0      0      0 S  0.0  0.0   0:01.74 khugepaged                                                                                                                                                                  
    33 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 crypto                                                                                                                                                                      
    41 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kthrotld                                                                                                                                                                    
    42 root      20   0       0      0      0 S  0.0  0.0   0:01.12 kworker/u256:1                                                                                                                                                              
    43 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kmpath_rdacd                                                                                                                                                                
    44 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kaluad                                                                                                                                                                      
    45 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kpsmoused                                                                                                                                                                   
    47 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 ipv6_addrconf                                                                                                                                                               
    60 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 deferwq                                                                                                                                                                     
    92 root      20   0       0      0      0 S  0.0  0.0   0:00.00 kauditd                                                                                                                                                                     
   688 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 ata_sff                                                                                                                                                                     
   697 root      20   0       0      0      0 S  0.0  0.0   0:00.01 scsi_eh_0                                                                                                                                                                   
   714 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 scsi_tmf_0                                                                                                                                                                  
   715 root      20   0       0      0      0 S  0.0  0.0   0:00.00 scsi_eh_1                                                                                                                                                                   
   722 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 scsi_tmf_1                                                                                                                                                                  
   731 root      20   0       0      0      0 S  0.0  0.0   0:00.93 kworker/u256:3                                                                                                                                                              
   869 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 ttm_swap                                                                                                                                                                    
   876 root     -51   0       0      0      0 S  0.0  0.0   0:00.00 irq/16-vmwgfx                                                                                                                                                               
  1731 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 nfit                                                                                                                                                                        
  1733 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 mpt_poll_0                                                                                                                                                                  
  1742 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 mpt/0                                                                                                                                                                       
  1811 root      20   0       0      0      0 S  0.0  0.0   0:00.00 scsi_eh_2                                                                                                                                                                   
  1818 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 scsi_tmf_2                                                                                                                                                                  
  2976 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kdmflush                                                                                                                                                                    
  2977 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 bioset                                                                                                                                                                      
  2991 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kdmflush                                                                                                                                                                    
  2992 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 bioset                                                                                                                                                                      
  3010 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 bioset                                                                                                                                                                      
  3015 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 xfsalloc                                                                                                                                                                    
  3020 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 xfs_mru_cache 
  
  top的使用方式 top[-d number] | top [-bnp]
  
  参数解释
  -d:number代表了秒数，表示top命令显示的页面更新一次的间隔。默认是5秒。-b:以批次的方式执行top。-n:与-b配合使用，表示需要进行几次top
  命令的输出结果。-p:指定特定的pid进程号进行观察。
  
  在top命令显示的页面还可以输入一下的相应的功能
  ？:显示在top当中可以输入的命令P:以CPU的使用资源排序显示
   M:以内存的使用资源排序显示
   N:以pid排序显示
   T:由进程使用的时间累计显示
   k:给某一个pid一个信号。可以用来杀死进程
   r:给某个pid重新定制一个nice值(即优先级)
   q:退出top(Ctrl+c也可以推出top)
   

 top前面几行参数的含义

 top - 18:40:26 up 1 day, 19 min,  2 users,  load average: 0.00, 0.01, 0.05
 Tasks: 107 total,   1 running, 106 sleeping,   0 stopped,   0 zombie
 %Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
 KiB Mem :   995896 total,   176724 free,   330460 used,   488712 buff/cache
 KiB Swap:  2097148 total,  2097148 free,        0 used.   472200 avail Mem 

### 第一行的参数
 top - 18:40:26 up 1 day, 19 min,  2 users,  load average: 0.00, 0.01, 0.05

|  参数   | 含义  |
|  ----  | ----  |
| 18:40:26  | 表示当前时间 |
|up 1 day, 19 min | 表示系统运行的时间 |
|  2 users  |当前登录的用户数 |
| load average: 0.00, 0.01, 0.05  | 系统负载，即任务队列的平均长度。三个数值分别为1分钟，5分钟，15分钟  |

   
   
 ### 第二行的参数
  Tasks: 107 total,   1 running, 106 sleeping,   0 stopped,   0 zombie

|  参数   | 含义  |
|  ----  | ----  |  
|  Tasks: 107 total | 进程总数 |
|  1 running  |  正在运行的进程数|
|  106 sleeping | 睡眠的进程数 |
| 0 stopped  | 停止的进程数 |
| 0 zombie  | 僵死进程数 |

 ### 第三行的参数
 %Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
 
|  参数   | 含义  |
|  ----  | ----  |  
|  %Cpu(s):  0.0 us  | 用户空间占用CPU百分比 |
|  0.0 sy  | 内核空间占用CPU的百分比 |   
| 0.0 ni  | 用户进程空间内改变过优先级的进程占用CPU百分比 |   
| 100.0 id  | 空闲CPU百分比 |   
| 0.0 wa  | 等待输入的输出的CPU时间百分比 |   
| 0.0 hi | 硬中断(Hardware IRQ)占用CPU百分比 |
| 0.0 si  |  软中断(Software Interrupts)占用CPU百分比 |  
| 0.0 st   |   |  
   
   
### 第四第五行参数
 KiB Mem :   995896 total,   176724 free,   330460 used,   488712 buff/cache
 KiB Swap:  2097148 total,  2097148 free,        0 used.   472200 avail Mem 
 
|  参数   | 含义  |
|  ----  | ----  |  
|KiB Mem :   995896 total| 物理内存总量|      
|176724 free| 空闲内存总量|      
|330460 used, |使用的的物理内存总量|      
|488712 buff/cache |用作内核缓存的内存量|      
|KiB Swap:  2097148 total|交换区总量|      
| 0 used.|使用的交换区总量|      
|2097148 free|空闲的交换区总量|      
|472200 avail Mem|代表可用于进程下一次分配的物理内存数量|      

### 进程信息
   PID USER      PR  NI    VIRT    RES    SHR S %CPU %MEM     TIME+ COMMAND   
   
|  参数   | 含义  |
|  ----  | ----  |  
|PID| 进程ID  |  
|USER| 进程所有者的用户ID  |  
|PR|优先级   |  
|NI|nice值，负值表示高优先级，正值表示低优先级|  
|VIRT|进程使用内存的虚拟内存总量，单位kb.VIRT=SWAP+RES|  
|RES|进程使用的，未被换出的物理内存大小，单位kb。RES=CODE+DATA|  
|SHR|共享内存得大小|  
|S|进程状态。D=不可中断得睡眠状态 R=运行 S=睡眠 T=跟踪/停止 Z=僵尸进程|  
|%CPU|上次个更新到现在的CPU占用百分比|  
|%MEM|进程使用的物理内存百分比|  
|TIME+|进程使用的CPU时间总计，单位1/100秒|  
|COMMAND|命令名/命令行|
   
   
   
### 相关简便操作

1.在top基本视图的情况下，按下"1"可以监控每个逻辑CPU的状况.

2. 敲击键盘的'b'(打开关闭加量效果)

3. 敲击键盘'x'(打开/关闭排序列的加亮效果%CPU这一列)

4. 按下'f'可以实现对相关列(添加或者移除某些列)的设置





   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
  
  
  
  
  
  
  
  
  
  
  
  

