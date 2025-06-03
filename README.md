
主要是学习一些Agent的执行范式

#### ✏️动手学Agent (一)：COT

讲了`Chain of Throught`，应该理解为“链式思维”？主要是得掌握两种方式【其实就是两种提示词的构造方式】
1. Few-shot
	- 在标准提示词中间增加 “解题思考过程” 的例子 
2. Zero-shot
	- 在标准提示词最后加入"Let's think step by step"。

#### ✏️动手学Agent (二)：Plan and Execute

使用Agent的时候会发现，前面几步还挺聪明，第三步突然就跑偏了，越往后越离谱。所以引入Plan and Execute框架（或者称为范式），先规划再执行。先写一个计划，再整个执行，分清思维和行为；相比于ReACT的一边想一边干，可控性更强。缺点是不适合实时性强的任务。

#### ✏️动手学Agent (三)：ReAct

🌳和Function Calling有什么区别？
->FunctionCalling 是调用系统内部的工具（比如函数），如果调用系统外部的工具，则使用MCP；
优点：
- 可以将各种外部API或工具封装成函数供模型调用。
- 对于明确的任务，可以直接调用相应的工具
缺点：
- 如果任务定义不明确或用户意图模糊，LLM可能难以准确选择工具。
总之：意图精确的场景下，可以使用FunctionCalling这种智能体策略

🌳ReAct：当我有一个模糊的输入的时候，我先思考（Reasoning），然后再行动（Act）
缺点：
- 通常需要多测调用LLM，ReAct通常比FunctionCalling更慢，并且消耗更多的token

参考：

- (https://github.com/Tallisgo/llm_based_agent/tree/master)

- (https://zhuanlan.zhihu.com/p/709162731)



#### ✏️OpenManus学习

....待更新