﻿享元模式：运用共享技术有效地支持大量细粒度的对象。

适用性：
	Flyweight 模式的有效性很大程度上取决于如何使用它以及在何处使用它。

当以下情况成立时可以使用 Flyweight 模式：
	一个应用程序使用了大量的对象。
	完全由于使用大量对象，造成很大的存储开销。
	对象的大多数状态都可变为外部状态。
	如果删除对象的外部状态，那么可以用相对较少的共享对象取代很多组对象。
	应用程序不依赖于对象标识。

效果：
	存储空间上的节省抵消了传输、查找和计算外部状态时的开销。节约量随着共享状态的增多而增大。

相关模式:
	Flyweight 模式通常和 Composite 模式结合起来，用共享叶节点的又向无环图实现一个逻辑上的层次结构。
	通常，最好用 Flyweight 实现 State 和 Strategy 对象。

体会：
	享元模式类似搞一个内存中的Key-Value对象存储，争取每个对象全局只有一个引用。
	那么，如果不局限 fine-grained，在 IoC Wireup 的策略中， 可用ContainerControlledLifetime来实现此模式。