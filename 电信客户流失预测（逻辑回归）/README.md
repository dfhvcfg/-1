# 电信客户流失预测（逻辑回归）
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

