# -Assignment-1
兰州大学数据挖掘与大数据分析 Assignment 1
1. 数据集（20 分）
• 使用正弦函数生成一个包含两个正弦周期的数据集（振幅可自行设定），从中均匀采样20 个
数据样本，对每个样本的目标变量yi 添加一个随机的扰动值（扰动值不要太大），形成数据
集D1;（10 分）
• 从UCI dataset repository 中下载一个适合用于回归分析的数据集，满足以下要求：
– 至少包含三列以上连续的数值型数据；（5 分）
– 至少包含100 个以上的样本；（5 分）
下载以后，仔细阅读数据集的使用说明，理解其用途及每一列数据的含义。
2. 数据预处理（10 分）
• 选定一种标准化处理方法，将所下载数据的每一列进行标准化处理，使所有列的数据处于同
一规模；（5 分）
• 对下载的数据集，根据数据集的用途及每一列的物理含义，选取其中一列作为目标变量y，
选取其它至少两列作为自变量x1,x2,···，形成数据集D2；（5 分)
3. 回归分析（50 分）
• 一元多项式回归（25 分）
变换多项式的阶数m(m= 1,2,···,5)，对每一个m将数据集D1 按照|Dtrain|: |Dtest|= 80% :
20% 的比例进行划分，用训练集Dtrain 进行训练确定回归系数，用测试集Dtest 进行测试，获
取MAE 和RMSE 值。
• Ridge 回归或Lasso 回归（25 分）
– 选取Ridge 回归模型或Lasso 回归模型，将D2 全部用作训练集，变换正则化系数λ的
取值，确定回归系数，获取正则化路径数据，从中确定稳定的超参数λ；（15 分）
1
– 将D2 按|Dtrain|: |Dtest|= 80% : 20% 的比例随机进行划分，用训练集Dtrain 对选定的
模型进行训练（使用刚才确定的λ值），重新确定回归系数，用测试集Dtest 进行测试，
获得MAE 和RMSE 值；重复这一过程5 次以上，获取多组MAE 和RMSE 值。（10 分）
4. 撰写技术报告（20 分）
以科技论文的形式撰写assignment 的技术报告，报告格式参见下图。其中，“引言”部分阐述
本文工作的意义；“算法”部分介绍所选的算法及其相关算法；“实验”部分阐述出于什么目的、
设计了哪些实验、使用了怎样的数据集，得出了什么样的结论；“结论”部分对本文工作进行总
结；“参考文献”部分列出本文所引用的文献情况。文  章  标  题
作者姓名
作者单位
摘要：
1. 引言
2. 算法
3. 实验及结果分析
4. 结论
参考文献
[1]
[2]
...
• 对于一元多项式回归的结果：画出生成数
据集的正弦曲线及采样并添加扰动的数据
点，并画出 m的不同取值得到的拟合曲
线；画出不同的m值对应的MAE、RMSE
的条形图，m的每一个取值对应的MAE、
RMSE 构成一组；针对这两张图，对其展
示的结果进行分析、解释；
• 对于Ridge 回归或Lasso 回归的结果：用折
线图画出正则化路径，对其进行分析，讨
论如何确定超参数λ的取值；对选定的λ，
画出多组MAE、RMSE 的条形图，每一次
对D2 进行划分得到的MAE、RMSE 构成
一组，并在最后添加一组MAE、RMSE 的
平均值，并针对该图进行分析、解释；
• 实验部分应对数据集进行介绍，说明使用
了什么样的方式人工合成了数据集D1，从
哪里下载了一个数据集并进行了怎样的处
理得到D2；
• 对实验结果的呈现，必须以文字形式进行
阐述、解释或者说明，不能只是简单地展
示结果的图，否则会减分；调整图的大小，
使之清晰美观，否则会减分；
• 报告应以正规的书面语言进行客观的阐述，
切勿使用口语化的表达方式或使用随意的
网络用语；
• 插图应使用矢量图，如果是用 Wps/Word
书写，则插图应该转成.emf 或者.wmf 格式，
使其在缩放时不失真；图、表要添加编号
与标题，并在正文中引用其编号；
• 报告中对使用的算法应引用其出处的参考
2
文献，引用格式为用方括号括起来的上标
数字形式，按引用的次序依次顺序编号，并
在报告末尾添加“参考文献”一节；每一
条文献条目中至少应包括作者名，文章标
题，期刊名，期号，卷号，出版年月，pp：
页码范围，DOI 号或官网的URL。
5. 必须提交的材料
• 生成的数据集、下载的数据集及预处理以后的数据集：各个数据集各自存入一个文件中，文
件名为程序中使用该数据集是的名称；
• python 的源程序：按照正弦曲线生成数据集采样并添加扰动的源程序、数据预处理的源程序、
实现回归的源程序，各自存入一个文件，文件名能体现其作用；
• pdf 版本的技术报告；
• 以上三部分压缩成一个压缩包，以学号+ 姓名对压缩包进行命名。
