# Tushare Pro 接口离线文档库

> 📊 **精选整理的 Tushare Pro 数据接口 Markdown 文档库**，涵盖 15,000+ 高积分权限的高阶数据、打板专题、筹码因子及全市场基础数据接口。
> 便于量化投研离线查阅、IDE 内嵌检索、知识库构建（RAG）以及 AI Agent 量化工具链集成。

[![GitHub repo](https://img.shields.io/badge/GitHub-tushare--pro-blue?logo=github)](https://github.com/raystar27-code/tushare-pro)
[![Documentation](https://img.shields.io/badge/Docs-124%2B%20APIs-brightgreen)]()
[![Format](https://img.shields.io/badge/Format-Markdown-orange)]()
[![License](https://img.shields.io/badge/License-MIT-lightgrey)]()

---

## 📌 项目概述

本项目为量化研究员、策略开发者及数据分析师整理了本地化的 **Tushare Pro** 接口文档集。每个接口均包含：
- **接口名称与代码**（如 `stock_basic`、`daily` 等）
- **官方 doc_id 与原始文档溯源**
- **权限与限量规则**（积分要求、单次返回上限、频次限制）
- **完整输入/输出参数表**（字段类型、必选/可选、字段中文释义）
- **Python 代码调用范例**

---

## 🚀 核心价值

1. **高阶/特色数据覆盖全面**：收录了大量需高额积分（如 15000+ 积分）的专业接口文档，包括每日筹码及胜率、市场游资席位名录、涨停连板天梯、神奇九转指标、专业版技术面因子等。
2. **极速检索与离线查阅**：无需反复打开网页登录查询，支持在 VS Code、Cursor、Obsidian 等编辑器中全局快捷键极速搜索字段名与参数说明。
3. **AI Agent / RAG 知识库友好**：规范化的 Markdown 格式，天然适合导入 LangChain、LlamaIndex 等向量数据库，为量化 AI 编程助手提供高质量的上下文 Grounding。

---

## 📚 接口分类总览 (9 大板块 / 124+ 接口)

> 完整接口对照表请参阅：👉 **[INDEX.md (接口速查总索引)](docs/INDEX.md)**

### 1. 基础数据 (13 个)
涵盖 A 股上市公司基础元数据、代码列表及变动信息。
- [股票列表 (`stock_basic`)](docs/0025_股票列表.md)
- [交易日历 (`trade_cal`)](docs/0026_交易日历.md)
- [股票曾用名 (`namechange`)](docs/0100_股票曾用名.md)
- [上市公司基本信息 (`stock_company`)](docs/0112_上市公司基本信息.md)
- [IPO新股上市 (`new_share`)](docs/0123_IPO新股上市.md)
- [上市公司管理层 (`stk_managers`)](docs/0193_上市公司管理层.md)
- [管理层薪酬和持股 (`stk_rewards`)](docs/0194_管理层薪酬和持股.md)
- [股票历史列表 (`bak_basic`)](docs/0262_股票历史列表.md)
- [每日股本（盘前） (`stk_premarket_shares`)](docs/0329_每日股本（盘前）.md)
- [北交所新旧代码对照 (`bse_mapping`)](docs/0375_北交所新旧代码对照.md)
- [ST股票列表 (`st_list`)](docs/0397_ST股票列表.md)
- [沪深港通股票列表 (`hs_const`)](docs/0398_沪深港通股票列表.md)
- [ST风险警示板股票 (`st_alert`)](docs/0423_ST风险警示板股票.md)

---

### 2. 行情数据 (18 个)
全市场各周期价格、成交、除权因子及复权数据。
- [历史日线 (`daily`)](docs/0027_历史日线.md)
- [复权因子 (`adj_factor`)](docs/0028_复权因子.md)
- [每日指标 (`daily_basic`)](docs/0032_每日指标.md)
- [沪深股通十大成交股 (`hsgt_top10`)](docs/0048_沪深股通十大成交股.md)
- [港股通十大成交股 (`ggt_top10`)](docs/0049_港股通十大成交股.md)
- [通用行情接口 (`pro_bar`)](docs/0109_通用行情接口.md)
- [周线行情 (`weekly`)](docs/0144_周线行情.md)
- [月线行情 (`monthly`)](docs/0145_月线行情.md)
- [复权行情 (`adj_daily`)](docs/0146_复权行情.md)
- [每日涨跌停价格 (`stk_limit`)](docs/0183_每日涨跌停价格.md)
- [每日停复牌信息 (`suspend_d`)](docs/0214_每日停复牌信息.md)
- [备用行情 (`bak_daily`)](docs/0255_备用行情.md)
- [周/月线行情每日更新 (`weekly_monthly_daily`)](docs/0336_周_月线行情(每日更新).md)
- [周/月线复权行情 (`weekly_monthly_adj`)](docs/0365_周_月线复权行情(每日更新).md)
- [历史分钟 (`stk_mins`)](docs/0370_历史分钟.md)
- [实时日线 (`rt_daily`)](docs/0372_实时日线.md)
- [实时分钟 (`rt_mins`)](docs/0374_实时分钟.md)
- [A股实时分钟-日累计 (`rt_mins_acc`)](docs/0457_A股实时分钟-日累计.md)

---

### 3. 财务数据 (10 个)
上市公司三大会计报表、财务指标及业绩快报披露。
- [利润表 (`income`)](docs/0033_利润表.md)
- [资产负债表 (`balancesheet`)](docs/0036_资产负债表.md)
- [现金流量表 (`cashflow`)](docs/0044_现金流量表.md)
- [业绩预告 (`forecast`)](docs/0045_业绩预告.md)
- [业绩快报 (`express`)](docs/0046_业绩快报.md)
- [财务指标数据 (`fina_indicator`)](docs/0079_财务指标数据.md)
- [财务审计意见 (`fina_audit`)](docs/0080_财务审计意见.md)
- [主营业务构成 (`fina_mainbz`)](docs/0081_主营业务构成.md)
- [分红送股数据 (`dividend`)](docs/0103_分红送股数据.md)
- [财报披露日期表 (`disclosure_date`)](docs/0162_财报披露日期表.md)

---

### 4. 参考数据 (14 个)
股东结构、解禁、大宗交易与市场提示。
- [前十大股东 (`top10_holders`)](docs/0061_前十大股东.md)
- [前十大流通股东 (`top10_floatholders`)](docs/0062_前十大流通股东.md)
- [股权质押统计数据 (`pledge_stat`)](docs/0110_股权质押统计数据.md)
- [股权质押明细数据 (`pledge_detail`)](docs/0111_股权质押明细数据.md)
- [股票回购 (`repurchase`)](docs/0124_股票回购.md)
- [限售股解禁 (`share_float`)](docs/0160_限售股解禁.md)
- [大宗交易 (`block_trade`)](docs/0161_大宗交易.md)
- [股票开户数据（停） (`stk_account_old`)](docs/0164_股票开户数据（停）.md)
- [股票开户数据（旧） (`stk_account`)](docs/0165_股票开户数据（旧）.md)
- [股东人数 (`stk_holdernumber`)](docs/0166_股东人数.md)
- [股东增减持 (`stk_holdertrade`)](docs/0175_股东增减持.md)
- [个股异常波动 (`stk_surv`)](docs/0451_个股异常波动.md)
- [个股严重异常波动 (`stk_serious_surv`)](docs/0452_个股严重异常波动.md)
- [交易所重点提示证券 (`stk_tips`)](docs/0453_交易所重点提示证券.md)

---

### 5. 特色数据 (11 个)
量化核心特色指标、机构研判及技术面高阶因子。
- [券商月度金股 (`broker_recommend`)](docs/0267_券商月度金股.md)
- [机构调研数据 (`stk_surv`)](docs/0275_机构调研数据.md)
- [券商盈利预测数据 (`report_rc`)](docs/0292_券商盈利预测数据.md)
- [每日筹码及胜率 (`cyq_perf`)](docs/0293_每日筹码及胜率.md)
- [每日筹码分布 (`cyq_chips`)](docs/0294_每日筹码分布.md)
- [股票技术面因子 (`stk_factor`)](docs/0296_股票技术面因子.md)
- [股票技术面因子(专业版) (`stk_factor_pro`)](docs/0328_股票技术面因子(专业版）.md)
- [股票开盘集合竞价数据 (`stk_auction_open`)](docs/0353_股票开盘集合竞价数据.md)
- [股票收盘集合竞价数据 (`stk_auction_close`)](docs/0354_股票收盘集合竞价数据.md)
- [神奇九转指标 (`nine_turn`)](docs/0364_神奇九转指标.md)
- [AH股比价 (`ah_ratio`)](docs/0399_AH股比价.md)

---

### 6. 两融及转融通 (7 个)
杠杆资金变动及融券借券数据追踪。
- [融资融券交易汇总 (`margin`)](docs/0058_融资融券交易汇总.md)
- [融资融券交易明细 (`margin_detail`)](docs/0059_融资融券交易明细.md)
- [融资融券标的（盘前） (`margin_target`)](docs/0326_融资融券标的（盘前）.md)
- [转融资交易汇总 (`slb_stat`)](docs/0331_转融资交易汇总.md)
- [转融券交易汇总(停) (`slb_trade_old`)](docs/0332_转融券交易汇总(停）.md)
- [转融券交易明细(停) (`slb_detail_old`)](docs/0333_转融券交易明细(停）.md)
- [做市借券交易汇总(停) (`slb_mm`)](docs/0334_做市借券交易汇总(停）.md)

---

### 7. 资金流向数据 (7 个)
个股、行业及大盘资金多维度监测（包含同花顺 THS、东方财富 DC 统计口径）。
- [个股资金流向 (`moneyflow`)](docs/0170_个股资金流向.md)
- [行业资金流向（THS） (`moneyflow_ind_ths`)](docs/0343_行业资金流向（THS）.md)
- [板块资金流向（DC） (`moneyflow_ind_dc`)](docs/0344_板块资金流向（DC）.md)
- [大盘资金流向（DC） (`moneyflow_mkt_dc`)](docs/0345_大盘资金流向（DC）.md)
- [个股资金流向（THS） (`moneyflow_ths`)](docs/0348_个股资金流向（THS）.md)
- [个股资金流向（DC） (`moneyflow_dc`)](docs/0349_个股资金流向（DC）.md)
- [板块资金流向（THS） (`moneyflow_blk_ths`)](docs/0371_板块资金流向（THS).md)

---

### 8. 打板专题数据 (24 个)
短线超短、游资龙虎榜、情绪周期与涨停连板分析。
- [龙虎榜每日统计单 (`top_list`)](docs/0106_龙虎榜每日统计单.md)
- [龙虎榜机构交易单 (`top_inst`)](docs/0107_龙虎榜机构交易单.md)
- [THS概念板块分类 (`ths_index`)](docs/0259_THS概念板块分类.md)
- [THS概念板块行情 (`ths_daily`)](docs/0260_THS概念板块行情.md)
- [THS概念板块成分 (`ths_member`)](docs/0261_THS概念板块成分.md)
- [涨跌停和炸板数据 (`limit_list_d`)](docs/0298_涨跌停和炸板数据.md)
- [市场游资最全名录 (`hm_list`)](docs/0311_市场游资最全名录.md)
- [游资交易每日明细 (`hm_detail`)](docs/0312_游资交易每日明细.md)
- [THS热榜 (`ths_hot`)](docs/0320_THS热榜.md)
- [DC热榜 (`dc_hot`)](docs/0321_DC热榜.md)
- [榜单数据（KP） (`kp_rank`)](docs/0347_榜单数据（KP）.md)
- [题材成分（KP） (`kp_concept`)](docs/0351_题材成分（KP）.md)
- [THS涨跌停榜单 (`limit_cpt_list`)](docs/0355_THS涨跌停榜单.md)
- [涨停股票连板天梯 (`limit_step`)](docs/0356_涨停股票连板天梯.md)
- [涨停最强板块统计 (`limit_strong_plate`)](docs/0357_涨停最强板块统计.md)
- [DC概念板块分类 (`dc_index`)](docs/0362_DC概念板块分类.md)
- [DC概念板块成分 (`dc_member`)](docs/0363_DC概念板块成分.md)
- [开盘竞价成交（当日） (`auction_trade`)](docs/0369_开盘竞价成交（当日）.md)
- [TDX概念板块分类 (`tdx_index`)](docs/0376_TDX概念板块分类.md)
- [TDX概念板块成分 (`tdx_member`)](docs/0377_TDX概念板块成分.md)
- [TDX概念板块行情 (`tdx_daily`)](docs/0378_TDX概念板块行情.md)
- [DC概念板块行情 (`dc_daily`)](docs/0382_DC概念板块行情.md)
- [题材数据（DC） (`dc_theme`)](docs/0421_题材数据（DC）.md)
- [题材成分（DC） (`dc_theme_member`)](docs/0422_题材成分（DC）.md)

---

### 9. 指数专题 (20 个)
主要指数、行业指数、成分权重与申万/中信分类。
- [指数基本信息 (`index_basic`)](docs/0094_指数基本信息.md)
- [指数日线行情 (`index_daily`)](docs/0095_指数日线行情.md)
- [指数成分和权重 (`index_weight`)](docs/0096_指数成分和权重.md)
- [大盘指数每日指标 (`index_dailybasic`)](docs/0128_大盘指数每日指标.md)
- [指数周线行情 (`index_weekly`)](docs/0171_指数周线行情.md)
- [指数月线行情 (`index_monthly`)](docs/0172_指数月线行情.md)
- [申万行业分类 (`index_classify`)](docs/0181_申万行业分类.md)
- [国际主要指数 (`index_global`)](docs/0211_国际主要指数.md)
- [沪深市场每日交易统计 (`daily_info`)](docs/0215_沪深市场每日交易统计.md)
- [深圳市场每日交易情况 (`sz_daily_info`)](docs/0268_深圳市场每日交易情况.md)
- [中信行业指数日行情 (`ci_daily`)](docs/0308_中信行业指数日行情.md)
- [申万日线行情 (`sw_daily`)](docs/0327_申万日线行情.md)
- [申万行业成分（分级） (`sw_member`)](docs/0335_申万行业成分（分级）.md)
- [指数技术面因子(专业版) (`index_factor_pro`)](docs/0358_指数技术面因子(专业版).md)
- [中信行业成分 (`ci_member`)](docs/0373_中信行业成分.md)
- [指数实时日线 (`index_rt_daily`)](docs/0403_指数实时日线.md)
- [申万实时行情 (`sw_rt_daily`)](docs/0417_申万实时行情.md)
- [指数历史分钟 (`index_mins`)](docs/0419_指数历史分钟.md)
- [指数实时分钟 (`index_rt_mins`)](docs/0420_指数实时分钟.md)
- [SW历史分钟 (`sw_mins`)](docs/0469_SW历史分钟.md)

---

## 💻 快速上手代码示例

在 Python 中安装并调用 Tushare Pro：

```bash
pip install tushare
```

```python
import tushare as ts

# 1. 初始化 token (前往 https://tushare.pro 个人中心获取)
ts.set_token('YOUR_TUSHARE_TOKEN')
pro = ts.pro_api()

# 2. 查询股票基础列表 (0025_股票列表.md)
df_basic = pro.stock_basic(exchange='', list_status='L', fields='ts_code,symbol,name,area,industry,list_date')
print(df_basic.head())

# 3. 查询每日筹码及胜率 (0293_每日筹码及胜率.md - 高阶特色数据)
df_cyq = pro.cyq_perf(ts_code='000001.SZ', start_date='20240101', end_date='20240301')
print(df_cyq.head())

# 4. 查询连板天梯数据 (0356_涨停股票连板天梯.md - 打板专题数据)
df_limit_step = pro.limit_step(trade_date='20240301')
print(df_limit_step.head())
```

---

## 🛠️ 项目结构

```text
tushare-pro/
├── README.md               # 项目主说明文档 (包含模块索引与使用指南)
├── .gitignore              # Git 忽略配置
└── docs/                   # 核心文档目录
    ├── INDEX.md            # 124+ 接口完整清单表格索引
    ├── 0025_股票列表.md     # 独立接口详细文档 (输入/输出/权限/代码)
    ├── 0026_交易日历.md
    ├── ...
    └── 0469_SW历史分钟.md
```

---

## ⚠️ 免责声明

1. 本文档集基于公开的 Tushare Pro 接口说明整理，所有接口的数据解释权及版权均归 [Tushare Pro](https://tushare.pro) 官方所有。
2. 调用各接口所需的数据权限与积分要求以 Tushare 官方实际最新规则为准。
3. 本项目文档仅供量化投资学习、策略研究交流与本地辅助查阅使用，不构成任何投资建议。
