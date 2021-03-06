# 1.引言

## 1.1目的

本文档描述了进销存系统的用户需求。

## 1.2阅读说明

文档内用例的描述使用了附表1的模版。

## 1.3参考文献

无
# 2.用例列表

| **参与者** | **用例** |
| --- | --- |
| 财务人员 |1. 账户管理<br>2. 制定单据<br>3.1制定收款单<br>3.2制定付款单<br>4.	查看销售明细表<br>5.查看经营历程表<br>6.期初建账|



# 3.详细用例描述
## 用例7 账户管理

| **ID** | 7 | **名称** | 账户管理 |
| --- | --- | --- | --- |
| **创建者** | 杨洋 | **最后一次更新者** | 杨洋 |
| **创建日期** | 2017/9/15 | **最后更新日期** | 2017/9/15 |
| **参与者** | 财务人员 |
| **触发条件** | 账户信息发生了更改 |
| **前置条件** | 财务人员已经登录并且获得了权限 |
| **后置条件** | 系统进行账户信息维护 |
| **优先级** | 高 |
| **正常流程** | 一．增加账户<br>1.1财务人员发出增加账户的请求<br>1.2系统提示财务人员导入账户信息（名称和金额）<br>1.3财务人员导入账户信息（名称和金额）并确认<br>1.4系统提示增加账户成功，并且显示新的账目列<br>重复 2-4 步骤直到财务人员完成所有应增账目的增加<br>1.5  更新系统操作日志<br>二．删除账户<br>2.1财务人员发出删除账户的请求 <br>2.2系统显示账目列表 <br>2.3财务人员选择账户列表项 <br>2.4系统显示账户具体信息 <br>2.5财务人员确定删除<br>2.6系统显示删除成功并显示更新后的删除列表<br>重复 2-6 步直到财务人员完成所有应删账目的删除<br>2.7  更新系统操作日志<br>三．修改账户属性<br>3.1财务人员发出修改账户的请求 <br>3.2系统显示账目列表 <br>3.3财务人员选择账户列表项 <br>3.4系统显示账户具体信息 <br>3.5财务人员编辑信息并确定 <br>3.6系统显示修改成功，显示更新后的账目列表 <br>重复 2-6 步直到财务人员完成所有应改账户的修改<br>3.5  更新系统操作日志<br>四．查询账户属性<br>4.1财务人员发出了查询账户信息的请求<br>4.2系统显示所有账目列表 <br>4.3财务人员选择通过编号查询，输入编号并确定 <br>4.4系统在账户列表中显示对应账户信息 <br>4.5更新系统操作日志
 |
| **扩展流程** | 1.3.a财务人员选择取消添加此次账户，返回步骤1.2<br>1.4.a系统提示信息编辑不全，返回步骤 1.2<br>2.5.a财务人员取消删除，返回步骤2.2<br>2.6a 系统显示该账户不存在,返回步骤2.2<br>3.5a、财务人员取消此次编辑，返回步骤 3.2<br>3.6a、系统显示信息编辑不完全，返回步骤 3.4 <br>3.6b、系统显示修改失败，返回步骤 3.2 <br>4.3a、财务人员选择通过关键字查询，输入关键字并确定 <br>4.3b、财务人员取消此次查询 返回步骤 4.2<br>4.4a系统提示查询账户不存在，返回步骤 4.2|
| **特殊需求** |无|

## 用例8 制定收款单

| **ID** | 8 | **名称** | 制定收款单 |
| --- | --- | --- | --- |
| **创建者** | 杨洋 | **最后一次更新者** | 杨洋 |
| **创建日期** | 2017/9/15 | **最后更新日期** | 2017/9/15 |
| **参与者** | 财务人员，目的是制作收款单并提交给总经理 |
| **触发条件** | 客户向财务人员提出付款 |
| **前置条件** | 财务人员已经登录并且获得了权限 |
| **后置条件** | 制定收款单并完成收款。客户，账户记录发生变化。 |
| **优先级** | 高 |
| **正常流程** |1 财务人员发出制定收款单的请求<br>2 系统显示编辑单据页面 <br>3 财务人员编辑收款项（账户，金额，备注）并确认 <br>4 系统显示添加收款项成功，显示更新后的转账列表 <br>重复 3-4 步骤直到完成收款项的添加 <br>5 财务人员确认制定收款单 <br>6 系统显示制定收款单成功 <br>重复 2-6 步骤直到制定完收款单，存储收款单，并标记为提交状态<br>7更新系统操作日志 |
| **扩展流程** | 3a、财务人员选择转账列表一行选择删除 <br>1系统显示更新后的转账列表 <br>1a、系统提示选择正确行删除 <br>2返回步骤 2|
| **特殊需求** |1、收款单单据编号格式为SKD-yyyyMMdd-xxxxx<br>2、付款单单据编号格式为FKD-yyyyMMdd-xxxxx<br>3、现金费用单单据编号格式为XJFYD-yyyyMMdd-xxxxx |

## 用例8 制定付款单

| **ID** | 8 | **名称** | 制定付款单 |
| --- | --- | --- | --- |
| **创建者** | 杨洋 | **最后一次更新者** | 杨洋 |
| **创建日期** | 2017/9/15 | **最后更新日期** | 2017/9/15 |
| **参与者** | 财务人员，目的是制作付款单并提交给总经理 |
| **触发条件** | 客户向财务人员提出收款 |
| **前置条件** | 财务人员已经登录并且获得了权限 |
| **后置条件** | 制定付款单并完成付款。客户，账户记录发生变化。 |
| **优先级** | 高 |
| **正常流程** |1 财务人员发出制定付款单的请求<br>2 系统显示编辑单据页面 <br>3 财务人员编辑付款项（账户，金额，备注）并确认<br>4 系统显示添加付款项成功，显示更新后的转账列表 <br>重复 3-4 步骤直到完成付款项的添加 <br>5 财务人员确认制定付款单 <br>6 系统显示制定付款单成功 ，存储付款单，并标记为提交状态<br>重复 2-6 步骤直到制定完付款单<br>7更新系统操作日志 |
| **扩展流程** | 3a、财务人员选择转账列表一行选择删除 <br>1系统显示更新后的转账列表 <br>1a、系统提示选择正确行删除 <br>2返回步骤 2|
| **特殊需求** |无 |
## 用例8 查看销售明细表

| **ID** | 8 | **名称** | 查看销售明细表 |
| --- | --- | --- | --- |
| **创建者** | 杨洋 | **最后一次更新者** | 杨洋 |
| **创建日期** | 2017/9/15 | **最后更新日期** | 2017/9/15 |
| **参与者** | 财务人员，总经理，目标是了解某一销售的明细或者了解一段时间内的销售情况 |
| **触发条件** | 操作人员要求查看销售明细表 |
| **前置条件** | 操作人员已经登录并且获得了权限|
| **后置条件** | 无 |
| **优先级** | 高 |
| **正常流程** |1．操作人员发出查看销售明细表的请求 <br>2．系统显示全部销售明细表 <br>3．操作人员选择时间区间，商品名，客户，业务员，仓库 <br>4．系统显示对应销售单的列表<br>5.  更新系统操作日志 |
| **扩展流程** | 4a.对应销售单列表为空<br>4a.1.系统提示没有对应销售单并返回步骤2<br>4b.操作人员查看某一销售单的具体信息 <br>4b.1.系统显示该销售单的具体信息 <br>4c.操作人员请求导出数据 <br>4c.1.系统导出数据|
| **特殊需求** |无 |

## 用例8 查看经营历程表

| **ID** | 8 | **名称** | 查看经营历程表|
| --- | --- | --- | --- |
| **创建者** | 杨洋 | **最后一次更新者** | 杨洋 |
| **创建日期** | 2017/9/15 | **最后更新日期** | 2017/9/15 |
| **参与者** | 财务人员，总经理，目标是查看一段时间里的符合条件的所有单据，了解经营情况 |
| **触发条件** | 操作人员要求查看查看经营历程表 |
| **前置条件** | 操作人员已经登录并且获得了权限|
| **后置条件** | 无 |
| **优先级** | 高 |
| **正常流程** |1．操作人员发出查看经营历程表的请求 <br>2．系统显示全部经营历程表 <br>3．操作人员选择时间区间，商品名，客户，业务员，仓库 <br>4．系统显示对应单据的列表<br>5. 更新系统操作日志 |
| **扩展流程** |4a.对应销售单列表为空<br>1.系统提示没有对应对应单据并并返回步骤2<br>4b.操作人员查看某一单据的具体信息 <br>系统显示该单据的具体信息 <br>1a.财务人员使用红冲功能（总经理没有此功能） <br>1.系统自动生成一个一模一样但是仅仅把数量取负数的单子并入账 <br>1b、财务人员使用红冲并复制功能（总经理没有此功能） <br>1.系统自动生成一个一模一样但是仅仅把数量取负数的单子并入账，并且显示可编辑的草稿单 <br>2.财务人员编辑草稿单 <br>3.系统显示编辑过后的单据已入账<br>4c.操作人员请求导出数据 <br>系统导出数据<br>|
| **特殊需求** |无 |

## 用例8 查看经营情况表

| **ID** | 8 | **名称** | 查看经营情况表|
| --- | --- | --- | --- |
| **创建者** | 杨洋 | **最后一次更新者** | 杨洋 |
| **创建日期** | 2017/9/15 | **最后更新日期** | 2017/9/15 |
| **参与者** | 财务人员和总经理，目标是查看一段时间内的经营收支状况和利润，了解收支情况，以制定合适的销售方案 |
| **触发条件** | 财务人员和总经理想要查看一段时间内的经营收支状况和利润|
| **前置条件** | 操作人员已经登录并且获得了权限|
| **后置条件** | 无 |
| **优先级** | 高 |
| **正常流程** |1、	用户请求查看经营情况表<br>系统显示经营情况表，包括以下信息：收入类、支出类和利润<br>2a.系统导出数据<br>更新系统操作日志|
| **扩展流程** |2a.系统导出数据|
| **特殊需求** |无 |
## 用例9 期初建账


| **ID** | 9 | **名称** | 期初建账 |
| --- | --- | --- | --- |
| **创建者** | 杨洋| **最后一次更新者** | 杨洋|
| **创建日期** | 2017/9/15 | **最后更新日期** | 2017/9/15 |
| **参与者** |财务人员,目的是建立新账来保存交易信息|
| **触发条件** | 公司需要建立一个新账目 |
| **前置条件** | 财务人员已经登录并且获得了权限 |
| **后置条件** | 建立一个拥有初始条件的新账目，永久储存期初信息 |
| **优先级** | 高 |
| **正常流程** |1．财务人员发出期初建账的请求 <br>2. 系统显示空商品列表 <br>3.财务人员填入商品信息（商品分类，某一商品的名称，类别，型号，进价/售价(默认为上年平均)，最近进价和最近售价留空）并确认<br>4.系统显示空客户信息列表（客户分类，某一个客户的名称，联系方式等， 应收应付(之前遗留)），银行账户信息（名称，余额） <br>5.财务人员填入客户信息（客户分类，某一个客户的名称，联系方式等，应收应付(之前遗留)）并确认<br>6.系统显示空账户列表 <br>7.财务人员填入账户信息（名称，金额）并确认<br>8.系统再次确认是否创建新账 <br>9.财务人员确认<br>10.系统建立新账，保存期初信息<br> 11.更新系统操作日志|
| **扩展流程** | 3a。增加商品是已有商品 <br>1．系统提示错误返回步骤2<br>5a.增加客户是已有客户 <br>1.系统提示错误返回步骤4<br>7a.增加账户是已有账户 <br>1.系统提示错误并返回步骤6<br>9a.财务人员取消确认 <br>1.系统取消操作 |
| **特殊需求** | 无 |


