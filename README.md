# 机器学习1



# 1.电信客户流失预测（逻辑回归）
# AT&T Customer Churn Prediction

## 数据集介绍

AT&T 数据集包含客户个人信息、通话记录、上网情况等信息。本项目旨在充分利用数据预测客户的流失情况，以帮助挽留用户，保持用户基数和活跃程度。

具体数据字段说明如下：

| 字段名             | 描述               |
|-------------------|--------------------|
| CustomerID        | 客户ID             |
| Gender            | 性别               |
| partneratt        | 配偶是否也为 AT&T 用户 |
| dependents_att    | 家人是否也是 AT&T 用户 |
| landline          | 是否使用 AT&T 固话服务 |
| internet_att/internet_other | 是否使用 AT&T 的互联网服务 |
| Paymentbank/creditcard/electroinc | 付款方式 |
| MonthlyCharges    | 每月话费           |
| TotalCharges      | 累计话费           |
| Contract_month/1year | 用户使用月度/年度合约 |
| StreamingTv/streamingMovies | 是否使用在线视频或电影应用 |
| Churn             | 客户流失标识         |

## 处理流程

### 数据概况分析

- 数据行/列数量
- 缺失值分布

### 单变量分析

- 数字型变量的描述指标（平均值、最大最小值、标准差）
- 类别型变量（分类数量、占比）
- 正负样本占比

### 相关性分析与可视化

- 按类别交叉对比
- 变量之间的相关性分析（散点图、热力图）

### 逻辑回归分析

- 模型建立
- 模型评估与优化







# 2.Titanic号沉船事件生存预测

泰坦尼克号沉没是历史上最著名的沉船事件。1912年4月15日，在她的处女航中，泰坦尼克号在与冰山相撞后沉没，在2224名乘客和船员中造成1502人死亡。这场耸人听闻的悲剧震惊了国际社会，并为船舶制定了更好的安全规定。 造成海难失事的原因之一是乘客和船员没有足够的救生艇。尽管幸存下来有一些运气因素，但有些人比其他人更容易生存，例如妇女，儿童和社会地位较高的人群。 在这个案例中，我们要求您完成对哪些人可能存活的分析

## 数据来源
数据集来源于Kaggle的Titanic号沉船事件竞赛：[链接](https://www.kaggle.com/c/titanic/overview)

我们提取到的数据集中的特征包括票的类别，是否存活，乘坐班次，姓名，年龄，上船港口，房间，性别等。

## 数据集下载
数据集可以从以下链接下载：[数据集下载链接](http://biostat.mc.vanderbilt.edu/wiki/pub/Main/DataSets/titanic.txt)
![image](https://github.com/dfhvcfg/-shu/assets/57213191/2fd916dc-de0d-4b42-ac87-21e6632f849b)

  
