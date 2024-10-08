## 第2章 系统模型
- 物理模型
	- 物理模型是从计算机和所用网络技术的特定细节中抽象出来的分布式系统底层硬件元素的表示。
- 体系结构模型
	- 一个系统的体系结构是用独立指定的组件以及这些组件之间的关系来表示的结构。
	- 通信范型
		- 进程间通信
			- 指的是用于分布式系统进程之间通信的相对底层的支持，包括消息传递原语、直接访问由互联网协议提供的API（套接字编程）和对多播通信的支持。
		- 远程调用
			- 远程调用代表分布式系统中最常见的通信范型，覆盖一系列分布式系统中的通信实体之间基于双向交换的技术，包括调用远程操作、过程或方法。
			- 远程方法调用（Remote Method Invocation, RMI）非常类似于远程过程调用，但它应用于分布式对象的环境。
		- 间接通信
			- **组通信**：组通信设计消息传递给若干接收者，因此是支持一对多通信的多方通信范型。
			- **发布--订阅系统**：发布--订阅系统共享同一个关键的特征，即提供一个中间服务，有效确保由生产者生成的信息被路由到需要这个信息的消费者。
			- **消息队列**：消息队列提供了点对点服务，其中生产者进程能发送消息到一个指定的队列，消费者进程能从队列中接收消息，或被通知队列里有新消息到达。因此，队列是生产者和消费者进程的中介。
			- **元组空间**：元组空间提供了进一步的间接通信服务，并支持这样的模型——进程能把任意的结构化数据项（称为元组）放到一个持久元组空间，其他进程可以指定感兴趣的模式，从而可以在元组空间读或者删除元组。
			- **分布式共享内存**：分布式共享内存(Distributed Shared Memory, DSM)系统提供一种抽象，用于支持在不共享物理内存的进程之间共享数据。
- 基础模型
	- 交互模型
	- 故障模型
	- 安全模型