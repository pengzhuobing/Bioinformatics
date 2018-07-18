# Bioinformatics

***
20180626  diversity.py  
用 python3 的 pandas 计算了基于丰度表的丰富度和 shannon 物种多样性指数,相比较之前写脚本遍历计算，基于数据框的运算爽很多. 命名为之 diversity.py,目前只能计算两个,以后看情况再加咯.

***
20180627  2017年影响因子 20180626.xlsx  
增加了刚出的截止至 2017 年杂志的影响因子(Journal Citation Reports).

***
20180710  NCBIscrapy.py  
利用 python3 的爬虫帮别人爬取 NCBI 网站上的一些东西，比较简单，留作记录.

***
20180714  geneInsample.py  
得到基因丰度表以后，计算基因在样本中的存在情况，如至少在 10% 的样本存在的基因有多少，20%，30%... 以此类推.
并且按照需要输出低于某一阈值的基因 ID, 用来后续分析的过滤，如在少于 10% 样品中存在的基因 ID.  

***
20180714  numToid.py  
接上一步，过滤出来至少在 10% 样品中存在的基因编号后，需要得到相应的基因 ID (因为之前基因长度文件配置的缘故，现在要替换回来).  
没有用字典，试着用 pandas 的 concat 功能, 将两个数据集按照行索引取交集合并，提取编号和与之对应的 ID, 单独输出到文件.  

***
20180718 补充 geneInsample.py  
修改 geneInsample.py, 使得脚本能输出高于某一阈值的基因丰度表，如大于 10% 样本中存在的所有基因的丰度表，用于物种丰度表的表征.
