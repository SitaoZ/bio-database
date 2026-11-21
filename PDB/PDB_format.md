[格式参考](https://laiyz.cn/pdbformat/)
最后附上（不一定完整）格式解析：
```bash 
标题部分
HEADER: 分子类, 公布日期, ID号  
OBSLTE: 注明此ID号已改为新号
TITLE: 说明实验方法类型
CAVEAT: 可能的错误提示
COMPND: 化合物分子组成（比如 蛋白质以及配体）
SOURCE: 化合物来源（比如来源大肠杆菌的某种酶）
KEYWDS: 关键词
EXPDTA: 测定结构所用的实验方法
AUTHOR: 结构测定者
REVDAT: 修订日期及相关内容
SPRSDE: 已撤销或更改的相关记录
JRNL: 发表坐标集的文献
REMARK: 注释
REMARK 1: 有关文献
REMARK 2: 最大分辨率
REMARK 3: 用到的程序和统计方法. 该记录用来记述结构优化的方法和相关统计数据
REMARK 4-999: 其他信息

一级结构
DBREF: 其他数据库的有关记录
SEQADV: PDB与其他数据库内记录的出入
SEQRES: 残基序列
MODRES: 对标准残基的修饰
杂因子
HET: 非标准残基
HETNAM: 非标准残基的名称
HETSNY: 非标准残基的同义字
FORMOL: 非标准残基的化学式

二级结构
HELIX: 螺旋
SHEET: 折叠片
TURN: 转角
连接注释
SSBOND: 二硫键
LINK: 残基间化学键
HYDBND: 氢键
SLTBRG: 盐桥
CISPEP: 顺式残基

晶胞特征及坐标变换
CRYST1: 晶胞参数(NMR除外)
该记录用来记述晶胞结构参数(a, b, c, α, β, γ, 空间群)以及Z值(单位结构中的聚和链数)
ORIGXn: 直角-PDB坐标
SCALEn: 直角-分数结晶学坐标(n=1, 2, 3, NMR除外)该记录介绍数据中直角坐标向部分晶体学坐标的转换
MTRIXn: 非晶相对称
TVECT: 转换因子

坐标部分
MODEL: 多亚基时示亚基号
当一个PDB文件中包含多个结构时(例:NMR结构解析), 该记录出现在各个模型的第一行. MODEL记录行的第11-14列上记入模型序号. 序号从1开始顺序记入, 在11-14列中从右起写. 比如说有30个模型, 则第1至9号模型, 该行的7-13列空白, 在14列上记入1-9的数字; 第10-30号模型, 该行的7-12列空白, 13-14列上记入10-30的数字.
ATOM: 标准基团的原子坐标
该记录记述了标准氨基酸以及核酸的原子名, 残基名, 直角坐标, 占有率, 温度因子等信息.
SIGATM: 标准差
ANISOU: 温度因子
SIGUIJ: 各种温度因素导致的标准差
TER: 链末端
该记录表示链的末端, 在每个聚合链的末端都必须有TER记录, 但是由于无序序列而造成的链的中断处不需要该记录.
HETATM: 非标准基团原子坐标
该记录记述了标准氨基酸以及核酸以外的化合物的原子名, 残基名, 直角坐标, 占有率, 温度因子等信息.
ENDMDL: 亚基结束
与MODEL记录成对出现, 记述在各模型的链末端的TER记录之后.

自定义连接部分
CONECT: 原子间的连通性有关记录

MASTER: 版权拥有者
END: 文件结束 该记录标志PDB文件的结束, 是必需的记录.


KEYS = [‘ATOM’, ‘HETATM’, ‘HELIX’, ‘SHEET’, ‘TURN’, ‘SSBOND’, ‘LINK’, ‘TER’,’HEADER’, ‘OBSLTEID’, ‘TITLE’, ‘CAVEAT’, ‘COMPND’, ‘SOURCE’, ‘KEYWDS’, ‘EXPDTA’, ‘AUTHOR’, ‘REVDAT’, ‘SPRSDE’, ‘JRNL’, ‘REMARK’, ‘DBREF’, ‘SEQADV’, ‘SEQRES’, ‘MODRES’, ‘HET’, ‘HETNAM’, ‘HETSNY’, ‘FORMOL’, ‘HYDBND’, ‘SLTBRG’, ‘CISPEP’, ‘CRYSTNMR’, ‘ORIGXPDB’, ‘SCALENMR’, ‘MTRIX’, ‘TVECT’, ‘MODEL’, ‘SIGATM’, ‘ANISOU’, ‘SIGUIJ’, ‘ENDMDL’, ‘CONECT’, ‘MASTER’, ‘END’]

ATOM
列 说明
1 – 6 记录类型
7 – 11 原子序号
13 – 16 原子名称，往往从第14位开始写, 占四个字符的原子名称才会从第13位开始写
17 额外定位符
18 – 20 残基名称
22 原子所属的链
23 – 26 残基序列号
27 残基插入代码
28 – 30 留空
31 – 38 x坐标
39 – 46 y坐标
47 – 54 z坐标
55 – 60 占有率 Occupy
61 – 66 温度因子 B-factor
67 – 72 留空
73 – 76 区段标识 Seg id
77 – 78 元素符号, 右对齐
79 – 80 原子电荷
```
