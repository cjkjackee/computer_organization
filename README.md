#computer_organization

## 影響程式執行的速度
-	演算法不一樣
-	programming language，compiler，架構不一樣
-	I/O不一樣
-	processor不一樣

## define performance
-	response time
	-	how long it take to do a task
-	throughput
	-	total work done pre unit time
replacing the processor with a faster version
	-	affect response time, throughput
adding processer
	-	affect throughput
define performance = 1/execution time

## measuring execution time
elapsed time 
-	程式執行所花的時間
-	total response time
-	因爲還有I/O那些時間，不能當作是真正的CPU performance time
CPU time
-	cpu在一個job上所花的時間
-	cpu真正有在工作的時間

## CPU clocking
clock period: duration of a clock cycle
clock frequency(rate): cycles per second

## CPU time
cpu time = clock cycle x cycle time = clock cycle/rate
所以要增加performance
-	減少clock cycles
-	增加rate
### eg
computer A: 2GHz clock, 10s cpu time
computer B: 6s cpu time, 1.2xcycle computer A

## instruction count ans CPI(cycles per instruction)
clock cycle = instrution count * CPI
### eg
computer A: cycle time = 250ps, CPI = 2.0
computer B: cycle time = 500ps, CPI = 1.2
same ISA
Q: same program running on A,B,which is faster, and by how much?

## CPI in More detail
每個指令所需要的cycle不一定一樣，所以用平均CPI

## reducing power
the power wall
	-	IC 的發展的瓶頸
	-	voltage不可能再降了
	-	所以rate不能再往上升，再上升，power就更高，更難散熱

## multiprocessor
因爲單一core因爲power wall 遇到瓶頸了，所以發展multicore

## manufacturing ICs
yield rate： proportion of working diec per wafer

## SPEC(standard performance evaluation crop) CPU benchmark
不能只測單一程式
-	因爲可能剛好是那個CPU指令集的強項
SPEC 指定了一些軟體讓CPU執行，看CPU的performance
-	這些程式，軟體合稱benchmark

## pitfall： amdahl‘s law
Amdahl’s law
-	改善一個系統，跟你改善的部分有關

