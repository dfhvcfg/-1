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







# 3.使用随机森林和adaboost进行车辆贷款违约预测

## 1. 案例介绍
国内某贷款机构的车贷业务面临借款人拖欠还款或拒不还款，导致该机构的不良贷款率居高不下的问题。该机构将部分贷款数据开放，诚邀大家帮助他们建立风险识别模型来预测可能违约的借款人（敏感信息已脱敏）

给定某机构实际业务中的相关借款人信息，包含53个与客户相关的字段
其中loan_default字段表明借款人是否会拖欠付款
任务目标是通过训练集训练模型，来预测测试集中loan_default字段的具体值，即借款人是否会拖欠付款，以此为依据，降低贷款风险。

## 2. 数据集介绍
customer_id 客户标识符

main_account_loan_no 主账户申请贷款数量

main_account_active_loan_no 主账户申请的有效贷款数量

main_account_overdue_no 主账号逾期数量

main_account_outstanding_loan 主账户未偿还的贷款余额

main_account_sanction_loan 主账户所有贷款被批准的贷款金额

main_account_disbursed_loan 主账户所有贷款已发放的贷款金额

sub_account_loan_no 二级账户申请贷款数量

sub_account_active_loan_no 二级账户申请的有效贷款数量

sub_account_overdue_no 二级账户逾期数量

sub_account_outstanding_loan 二级账户未偿还的贷款金额

sub_account_sanction_loan 二级账户所有贷款被批准的贷款金额

sub_account_disbursed_loan 二级账户所有贷款已发放的贷款金额

disbursed_amount 已发放贷款金额

asset_cost 资产成本

branch_id 发放贷款的分行

supplier_id 发放贷款的车辆经销商

manufacturer_id 汽车制造商

year_of_birth 客户出生日期

disbursed_date 贷款日期

area_id 付款区域

employee_code_id 记录付款的对接员工

mobileno_flag 是否填写手机号

idcard_flag 是否填写身份证

Driving_flag 是否出具驾驶证

passport_flag 是否填写护照

credit_score 信用评分

main_account_monthly_payment 主账户月供金额

sub_account_monthly_payment 二级账户的月供金额

last_six_month_new_loan_no 过去六个月客户的新贷款申请数量

last_six_month_defaulted_no 过去六个月客户的违约数量

average_age 平均贷款期限

credit_history 信用记录

enquirie_no 客户查询贷款次数

loan_to_asset_ratio 贷款与资产比例

total_account_loan_no 所有账户申请的活跃贷款数量

main_account_inactive_loan_no 主账户申请的无效贷款数量

sub_account_inactive_loan_no 二级账户申请的无效贷款数量

total_inactive_loan_no 所有账户申请的无效贷款数量

total_overdue_no 所有账户的逾期次数

total_outstanding_loan 所有账户的未结余额的总额

total_sanction_loan 来自所有账户的所有贷款被批准的贷款金额

total_disbursed_loan 为所有账户的所有贷款支付的贷款金额

total_monthly_payment 所有账户的月供金额

outstanding_disburse_ratio 已发放贷款总额/未偿还贷款总额（两者比例）

main_account_tenure 主账户还款期数

sub_account_tenure 二级账户还款期数

disburse_to_sactioned_ratio 已发放贷款/批准贷款（两者比例）

active_to_inactive_act_ratio 有效贷款次数/无效贷款次数（两者比例）

Credit_level 信用评分

employment_type 工作类型

age 年龄

loan_default 1表示客户逾期，0表示客户未逾期

  
# 使用XGBoost进行红酒品质分类

本示例演示了如何使用XGBoost来预测红酒的品质。数据集包含11个特征和3269条数据，品质共有6个类别，分别用数字0、1、2、3、4、5表示。

## 数据集介绍

数据集包含以下特征：
![image](https://github.com/dfhvcfg/-1/assets/57213191/a20c85e4-df2d-4441-96d8-a289b36f3653)








# 用朴素贝叶斯进行垃圾邮件分类
## 1. 朴素贝叶斯文本分类原理说明

### 1.1 数据集介绍

有如下训练数据, 记录了用户对餐厅的评价, 我们为每一条评论添加了相关标签, Positive 代表好评，Negative代表差评

![image](https://github.com/dfhvcfg/-1/assets/57213191/76854a97-b672-4c21-812b-5b35dc1ebe99)


### 1.2 模型训练

#### 数据预处理

首先我们将训练数据集中的所有单词都 转换为小写 ，并去掉标点符号

![image](https://github.com/dfhvcfg/-1/assets/57213191/61b05662-bd5e-4d8e-9b53-28187585f1d3)


#### 准备词袋

统计好评(Positive) 和 差评(Negative) 中出现的单词的词频(单词出现的次数)，放到两个词袋中(bag of word)

![image](https://github.com/dfhvcfg/-1/assets/57213191/b7c08ec1-043e-4bc6-ace3-9cdf9e07a4f4)


到这儿我们的模型数据已经准备好, 可以进行预测了

### 1.3 朴素贝叶斯分类

#### 数据预处理

按照训练阶段相同的方式处理数据

![image](https://github.com/dfhvcfg/-1/assets/57213191/07b99b2a-897b-4437-8f51-b321f5650dcf)

#### 接下来我们要将数据拆成一个一个单词

![image](https://github.com/dfhvcfg/-1/assets/57213191/16fac2da-df18-430e-a16c-0b0be4d34f6d)


#### 朴素贝叶斯分类

此时我们要分别计算 P(好评|very,good,food,and, service) , P(差评|very,good,food,and,service)，并比较他们的大小

根据贝叶斯公式
![image](https://github.com/dfhvcfg/-1/assets/57213191/7f1f17fa-e15b-4804-b83d-2e89ca8a4323)

我们需要计算 :
![image](https://github.com/dfhvcfg/-1/assets/57213191/1745ead8-33de-4aa1-93b0-28c8f5a648ab)

由于只需要比较大小 所以我们只需要计算:
![image](https://github.com/dfhvcfg/-1/assets/57213191/ba009cce-c6cd-46e3-81ab-71cd72ea0fa1)


先计算 P(好评) P(差评)

![image](https://github.com/dfhvcfg/-1/assets/57213191/b8d99f24-5e00-4a7e-b53b-64066115de98)


#### 朴素贝叶斯的独立假设

P(very,good,food,and, service|好评) = P(very|好评) * P(good|好评) * P(food|好评) * P(and|好评) * P(service|好评)

P(very,good,food,and, service|差评) = P(very|差评) * P(good|差评) * P(food|差评) * P(and|差评) * P(service|差评)

统计待预测样本的单词在不同类别中的词频

![image](https://github.com/dfhvcfg/-1/assets/57213191/9070f19c-4227-4825-a794-c7088cf16796)


统计带预测样本的单词在不同类别中的概率
![image](https://github.com/dfhvcfg/-1/assets/57213191/b53a5ba9-fd77-4455-9b41-a049ac58b138)

计算P(very,good,food,and, service|好评) 和P(very,good,food,and, service|差评)

![image](https://github.com/dfhvcfg/-1/assets/57213191/c4a43082-2da3-4779-8e23-f03c666cc182)


由于在训练集中, 好评的词袋中没有and 和 service 差评的词袋中没有 good , and ,service 导致概率计算为0, 无法预测

我们需要为其加上 拉普拉斯平滑系数
![image](https://github.com/dfhvcfg/-1/assets/57213191/0bd8602c-9a25-4919-b6f0-1d58f243ed9b)

一般α = 1 , m为特征数量, 本例为训练集中单词出现的总次数

本例中训练集一共有32个不同的单词

注: 后续计算与上面的公式略用区别 相当于N+m+1 但不影响最终的计算结果

![image](https://github.com/dfhvcfg/-1/assets/57213191/ffdc55e8-f412-4e99-9b5c-a32f4ad9b0a8)


统计词频
![image](https://github.com/dfhvcfg/-1/assets/57213191/5bbfaf2d-cdfb-44a5-973c-15ffed2d4b3b)
![image](https://github.com/dfhvcfg/-1/assets/57213191/ec36c31e-5e12-4fbd-8333-f77500d44d8d)

计算概率
![image](https://github.com/dfhvcfg/-1/assets/57213191/dc8479af-03b9-474d-a277-ec007848a656)

计算P(very) * P(good) * P(food) * P(and) * P(service):
![image](https://github.com/dfhvcfg/-1/assets/57213191/b6db8e29-9276-4e3a-87bd-cbaa369a16a4)

计算最终结果
![image](https://github.com/dfhvcfg/-1/assets/57213191/ebd20e9c-05d2-4a5a-8afe-2e8402efbd7f)

从上面结果中看出 好评的概率>差评的概率, 所以该条评论为好评

### 1.4 流程小结

- 训练数据处理(去掉无关符号, 字母转小写)→ 统计训练数据词频→ 得到词袋(BoW)
- 带预测样本数据处理(去掉无关符号, 字母转小写) → 统计带预测样本中单词在训练集中的词频→ 计算概率→得出分类结果

