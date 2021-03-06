了解小区趋势的包：CommunityTrend
=======================

web:

+ https://github.com/MaxBigdata/CommunityTrend


##

R Package


## INSTALL

```{r}
library(devtools)
install_github('Max/CommunityTrend')
```

## DEMO
## 了解社区市场近况，目前只有自如
```{r}
library(CommunityTrend)
```
# input
### trend内输入一个社区，
### 包内可输出自如上个月有出租房的8000多个社区和有上架房的4000多个社区信息

```{r}
trend('新龙城')
```

# output

自如上月趋势：

[1] "-------------------------------------"

[1] "|过去一个月内自如:"

[1] "|商圈总房数：912"

[1] "|商圈均价：2846.23516483517"

[1] "|小区总房数：182"

[1] "|小区均价：3033.87362637363"

[1] "|小区调价房数量:7"

[1] "|小区调价房平均降价:371.428571428571"

[1] "|"

[1] "|小区月内合租单间上架：75"

[1] "|小区月内新上架单间成交量:35"

[1] "|小区月内新上架单间平均展示期:9.85298365886627"

[1] "|小区月内新上架成交单间平均展示期:1.40164923316775"

[1] "|小区月内新上架单间平均调价数:4"

[1] "|小区月内新上架单间平均调价价格:510"

[1] "|"

[1] "|"

[1] "|--------：成交数据||上架数据"

[1] "|所在商圈:龙泽||龙泽"

[1] "|社区合租单间销量：82||75"

[1] "|社区合租单间均价：2679.46341463415||2765.54666666667"

[1] "|社区合租单间平均面积：12.7732926829268||13.0637333333333"

[1] "|社区合租单位面积价格：209.770767894139||211.696503296658"

[1] "|"

[1] "|当地商圈合租单间销量：485||428"

[1] "|当地商圈合租单间均价：2551.48453608247||2620.1308411215"

[1] "|当地商圈合租单间平均面积：13.2249072164948||13.3708878504673"

[1] "|当地商圈合租单间单位面积价格：192.930240969866||195.957880316072"

[1] "-------------------------------------"




# 更新方法（update）

### 更新方式一 :使用devtools包里的update函数
##### 但这种方式经常不灵

```{r}
update.packages("CommunityTrend")
```
### 更新方式二 :卸载包后重新安装
##### 卸载包的方式如下

```{r}
#删除环境中的此包
detach("package:CommunityTrend")
#删除包库lib中的此包
remove.packages("CommunityTrend")
```

# 下一版本预览

### ver2
趋势数据部分，计划根据需要加一些其他统计数据
例如：小区空调覆盖率
小区供暖覆盖率
小区设计风格分布
等...

### ver3
准备根据线性模型，XGboost，逻辑回归进行预测
然后输入一条标准自如租房信息，就可以得到预测房价
前两者模型的精度目前推进至7~8%的相对误差
并根据不同模型差值，数据库数据缺失比率等，评价预测精准性


### ver4
根据线性模型，给出不同属性与价格的关系
例如在外界条件不变的情况下，不同小区价格调低100元能减少多少展览时间

### ver1，2-plus
将模型扩展至其他公司，不仅关注自如，也覆盖其他


# 致谢

感谢李伟老师给出的统计火房，调价房，调价均值的建议

感谢刘娟姐对展示数据的评价和改进建议
