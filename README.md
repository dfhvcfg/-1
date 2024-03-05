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
