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

[1] "|社区合租单间上架：7"

[1] "|平均展览时间:9.85298365886627"

[1] "|成为火房比例:无"

[1] "|调价房数量:7"

[1] "|调价房平均降价:371.428571428571"

[1] "|"

[1] "|"

[1] "|--------：成交数据||上架数据"

[1] "|所在商圈:龙泽||龙泽"

[1] "|社区合租单间销量：52||7"

[1] "|社区合租单间均价：2812.69230769231||3044.28571428571"

[1] "|社区合租单间平均面积：12.5601923076923||12.9428571428571"

[1] "|社区合租单间平均楼层：14.6538461538462||16.1428571428571"

[1] "|社区合租单位面积价格：223.937041630303||235.209713024283"

[1] "|"

[1] "|当地商圈合租单间销量：315||72"

[1] "|当地商圈合租单间均价：2670.22222222222||2754.66666666667"

[1] "|当地商圈合租单间平均面积：13.4137142857143||13.2670833333333"

[1] "|当地商圈合租单间平均楼层：15.7111111111111||14.8333333333333"

[1] "|当地商圈合租单间单位面积价格：199.066579572671||207.631669859615"

[1] "-------------------------------------"



# -----------------------------------------------------------------------------
# update 更新方法

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
