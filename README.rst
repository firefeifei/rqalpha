=======
RQAlpha
=======

..  image:: https://raw.githubusercontent.com/ricequant/rq-resource/master/rqalpha/logo.jpg

..  image:: https://img.shields.io/travis/ricequant/rqalpha/master.svg
    :target: https://travis-ci.org/ricequant/rqalpha/branches
    :alt: Build

..  image:: https://coveralls.io/repos/github/ricequant/rqalpha/badge.svg?branch=master
    :target: https://coveralls.io/github/ricequant/rqalpha?branch=master

..  image:: https://readthedocs.org/projects/rqalpha/badge/?version=latest
    :target: http://rqalpha.readthedocs.io/zh_CN/latest/?badge=latest
    :alt: Documentation Status

..  image:: https://img.shields.io/pypi/v/rqalpha.svg
    :target: https://pypi.python.org/pypi/rqalpha
    :alt: PyPI Version

..  image:: https://img.shields.io/pypi/pyversions/rqalpha.svg
    :target: https://pypi.python.org/pypi/rqalpha
    :alt: Python Version Support


RQAlpha 从数据获取、算法交易、回测引擎，实盘模拟，实盘交易到数据分析，为程序化交易者提供了全套解决方案。

**仅限非商业使用。如需商业使用，请联系我们：public@ricequant.com**

RQAlpha 具有灵活的配置方式，强大的扩展性，用户可以非常容易地定制专属于自己的程序化交易系统。

RQAlpha 所有的策略都可以直接在 `Ricequant`_ 上进行回测和实盘模拟，并且可以通过微信和邮件实时推送您的交易信号。

`Ricequant`_ 是一个开放的量化算法交易社区，为程序化交易者提供免费的回测和实盘模拟环境，并且会不间断举行实盘资金投入的量化比赛。

特点
============================

======================    =================================================================================
易于使用                    让您集中于策略的开发，一行简单的命令就可以执行您的策略。
完善的文档                   您可以直接访问 `RQAlpha 文档`_ 或者 `Ricequant 文档`_ 来获取您需要的信息。
活跃的社区                   您可以通过访问 `Ricequant 社区`_ 获取和询问有关 RQAlpha 的一切问题，有很多优秀的童鞋会解答您的问题。
稳定的环境                   每天都有会大量的算法交易在 Ricequant 上运行，无论是 RQAlpha，还是数据，我们能会做到问题秒处理，秒解决。
灵活的配置                   您可以使用多种方式来配置和运行策略，只需简单的配置就可以构建适合自己的交易系统。
强大的扩展性                 开发者可以基于我们提供的 Mod Hook 接口来进行扩展。
======================    =================================================================================

快速指引
============================

*   `RQAlpha 介绍`_
*   `安装指南`_
*   `10分钟学会 RQAlpha`_
*   `策略示例`_

RQAlpha API
============================

*   `API`_ : RQAlpha API 文档

Mod
============================

RQAlpha 提供了极具拓展性的 Mod Hook 接口，这意味着开发者可以非常容易的对接第三方库。

您可以通过如下方式使用 安装和使用Mod:

..  code-block:: bash

    # 查看当前安装的 Mod 列表及状态
    $ rqalpha mod list
    # 安装 Mod
    $ rqalpha mod install xxx
    # 卸载 Mod
    $ rqalpha mod uninstall xxx
    # 启用 Mod
    $ rqalpha mod enable xxx
    # 禁用 Mod
    $ rqalpha mod disable xxx

以下是目前已经集成的 Mod 列表:

========================    ==================================================================================
Mod名                        说明
========================    ==================================================================================
`sys_accounts`_             【系统模块】为回测、模拟交易、实盘提供了股票和期货的账户模型及专用 API
`sys_analyser`_             【系统模块】记录每天的下单、成交、投资组合、持仓等信息，并计算风险度指标，并以csv、plot图标等形式输出分析结果
`sys_funcat`_               【系统模块】支持以通达信公式的方式写策略
`sys_progress`_             【系统模块】在控制台输出当前策略的回测进度
`sys_risk`_                 【系统模块】对订单进行事前风控校验
`sys_simulation`_           【系统模块】支持回测、撮合、滑点控制等
`sys_benchmark`_            【系统模块】提供了使用单一标的作为基准的具体实现
`sys_transaction_cost`_     【系统模块】实现了不同市场不同交易表的的税费计算逻辑
========================    ==================================================================================

如果您基于 RQAlpha 进行了 Mod 扩展，欢迎告知我们，在审核通过后，会在 Mod 列表中添加您的 Mod 信息和链接。

基于 RQAlpha 的米筐期货程序化实盘终端
==================================

米筐将 RQAlpha 打通期货实盘，实现了策略的全自动化交易。策略托管运行在云端，用户无需为策略的稳定运行和硬件支持担忧。 `立即获取免费Windows版实盘终端。 <https://ricequant.pro/download/RQProAir/RQProAir-1.3.0.exe>`_

.. image:: https://raw.githubusercontent.com/ricequant/rqalpha/master/docs/source/_static/rqpro.png

策略可进行自动化实盘交易是最不可或缺的一环，RQPro 终端期货实盘目前合作的期货商有东亚期货、安粮期货和中信期货，支持的期货商仍在扩充中，以期尽可能满足您的期货商选择。RQPro 实盘交易的核心优势如下：

* 基于 RQAlpha 引擎，拥有强劲的性能，从回测至实盘无需更改代码，支持回测、模拟仿真和实盘交易一体化。
* 支持十年全品种（商品、国债、股指）、多频率（日、分钟、Tick）期货历史数据。
* 实时数据直连 CTP，提供实时 tick 行情，历史数据自动清洗入库。
* 支持期货夜盘，符合看穿式监管合规要求。
* 实盘策略加密后运行在云端，兼顾策略私密性和硬件管理问题。
* 服务端采用 K8S 技术，保证低延迟和高可用。
* 包含专为实盘打造的仓位管理系统，支持手工增删成交来调整策略的仓位。可以在对账出现差异或因在其他系统中经由同一资金账号交易后的成交回报不同步，调整仓位使得策略仓位与实际仓位一致。

目前的云端实盘交易功能仅支持期货交易，如需股票程序化交易，请等待后续中泰证券量化交易终端下载。
期货实盘交易在 `米筐主站 <https://www.ricequant.com>`_ 注册账号即可在终端内使用。
更多详细可见 `《期货实盘说明》 <https://assets.ricequant.com/welcome/期货实盘说明.09b0d7b5.pdf>`_ ，欢迎致电 0755-22676337 联系我们咨询云端期货实盘信息。

RQData数据本地化服务
====================

为专业投资者提供便利易用的金融数据方案，免除数据整理、清洗及运维的困扰，使投研人员及策略开发者可以更专注于投研及模型开发等关键环节。米筐RQData金融数据API可无缝对接RQAlpha，您只需在策略中import rqdatac，即可通过API本地调用以下数据：

=============================       ==================================================================================
**合约信息**                              中国A股、指数、场内场外基金、期货、场内债券的基本合约信息
**A股基础信息**                           交易日、股票拆分和分红、停牌、ST股判断等数据
**行情数据**                              A股2005年至今及实时行情数据（含连续竞价时间段）；指数快照行情、历史权重、指数估值指标等
**基金数据**                              基础数据、净值数据、报告披露、持仓数据等
**期货、期权和现货数据**                   全市场期权数据；期货历史及快照行情数据等；期货主力连续合约；期货会员持仓排名及仓单
**可转债数据**                            可转债基础合约；可转债股价、转债导致规模变化、现金等数据
**A股上市以来的所有财务数据**               基础财务数据、营运、盈利能力、估值等；财务快报及业绩预告、TTM滚动财务数据等；支持财务数据Point in Time API
**行业、板块、概念分类**                   股票资金现金流入流出、换手率
**风格因子数据**                          风格因子暴露度、收益率、协方差和特异风险。（每个交易日8:30开始更新增量数据）
**宏观经济数据**                          存款准备金率、货币供应量、大量宏观因子等数据
**电商数据**                              天猫、淘宝、京东三大平台（日更新）。注：与超对称科技合作提供
**舆情数据**                              雪球与东方财富股吧。注：与数据合作方合作提供
=============================       ==================================================================================

目前RQData已正式上线，支持Python API、Matlab API及Excel插件等多种调取方式，欢迎 `免费试用 <https://www.ricequant.com/welcome/rqdata>`_ 和 `咨询私有化部署 <https://www.ricequant.com/welcome/pricing>`_ 。

加入开发
============================

*   `如何贡献代码`_
*   `基本概念`_
*   `RQAlpha 基于 Mod 进行扩展`_

获取帮助
============================

关于RQAlpha的任何问题可以通过以下途径来获取帮助

*  可以通过 `索引`_ 或者使用搜索功能来查找特定问题
*  在 `Github Issues`_ 中提交issue
*  RQAlpha 交流群「487188429」


.. _Github Issues: https://github.com/ricequant/rqalpha/issues
.. _Ricequant: https://www.ricequant.com/algorithms
.. _RQAlpha 文档: http://rqalpha.readthedocs.io/zh_CN/latest/
.. _Ricequant 文档: https://www.ricequant.com/api/python/chn
.. _Ricequant 社区: https://www.ricequant.com/community/category/all/
.. _FAQ: http://rqalpha.readthedocs.io/zh_CN/latest/faq.html
.. _索引: http://rqalpha.readthedocs.io/zh_CN/latest/genindex.html
.. _RQPro: https://www.ricequant.com/rqpro_propaganda/?utm_source=github
.. _专业级本地终端RQPro: https://www.ricequant.com/rqpro_propaganda/?utm_source=github

.. _RQAlpha 介绍: http://rqalpha.readthedocs.io/zh_CN/latest/intro/overview.html
.. _安装指南: http://rqalpha.readthedocs.io/zh_CN/latest/intro/install.html
.. _10分钟学会 RQAlpha: http://rqalpha.readthedocs.io/zh_CN/latest/intro/tutorial.html
.. _策略示例: http://rqalpha.readthedocs.io/zh_CN/latest/intro/examples.html

.. _API: http://rqalpha.readthedocs.io/zh_CN/latest/api/base_api.html

.. _如何贡献代码: http://rqalpha.readthedocs.io/zh_CN/latest/development/make_contribute.html
.. _基本概念: http://rqalpha.readthedocs.io/zh_CN/latest/development/basic_concept.html
.. _RQAlpha 基于 Mod 进行扩展: http://rqalpha.readthedocs.io/zh_CN/latest/development/mod.html
.. _History: http://rqalpha.readthedocs.io/zh_CN/latest/history.html
.. _TODO: https://github.com/ricequant/rqalpha/blob/master/TODO.md
.. _develop 分支: https://github.com/ricequant/rqalpha/tree/develop
.. _master 分支: https://github.com/ricequant/rqalpha
.. _rqalpha_mod_tushare: https://github.com/ricequant/rqalpha-mod-tushare
.. _通过 Mod 扩展 RQAlpha: http://rqalpha.io/zh_CN/latest/development/mod.html
.. _sys_analyser: https://github.com/ricequant/rqalpha/blob/master/rqalpha/mod/rqalpha_mod_sys_analyser/README.rst
.. _sys_funcat: https://github.com/ricequant/rqalpha/blob/master/rqalpha/mod/rqalpha_mod_sys_funcat/README.rst
.. _sys_progress: https://github.com/ricequant/rqalpha/blob/master/rqalpha/mod/rqalpha_mod_sys_progress/README.rst
.. _sys_risk: https://github.com/ricequant/rqalpha/blob/master/rqalpha/mod/rqalpha_mod_sys_risk/README.rst
.. _sys_simulation: https://github.com/ricequant/rqalpha/blob/master/rqalpha/mod/rqalpha_mod_sys_simulation/README.rst
.. _sys_accounts: https://github.com/ricequant/rqalpha/blob/master/rqalpha/mod/rqalpha_mod_sys_accounts/README.rst
.. _sys_benchmark: https://github.com/ricequant/rqalpha/blob/master/rqalpha/mod/rqalpha_mod_sys_benchmark/README.rst
.. _sys_transaction_cost: https://github.com/ricequant/rqalpha/blob/master/rqalpha/mod/rqalpha_mod_sys_transaction_cost/README.rst
.. _RQData数据本地化服务: https://www.ricequant.com/doc/rqdata-institutional
.. _点击链接免费开通: https://ricequant.mikecrm.com/h7ZFJnT

