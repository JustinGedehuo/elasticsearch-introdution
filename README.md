#01 -课程简介
#02 -内容综述及学习建议
- 为什么要学 ElasticSearch
ElasticSearch 是一款开源的搜索引擎和大数据分析平台。
    - 主要功能
        - 分布式搜索引擎
        - 大数据近实时分析引擎
    - 产品特性
        - 高性能，和 T + 1 说不
        - 容易使用 / 容易扩展
    - 互联网公司大量使用 ElasticSearch
        - 小米
        - 饿了么
        - 滴滴出行
        - 携程
        - 阿里云
        - 腾讯云
- 学习目标：三个层面
    - 开发
        - 产品基本共功能，底层工作原理，数据建模最佳实践
    - 运维
        - 容量规划；性能优化；问题诊断；滚动升级
    - 方案
        - 搜索以及如何让解决搜索的相关性问题
        - 大数据分析实践，理论知识运用到实际场景
- 课程特色
    - 涵盖ElasticSearch认证全部知识点
    - 数据的真实性 & 多样性
- 课程实战
    - 电影搜索
    - Stack Overflow 调查问卷数据分析
- 课程内容与结构
    - ElasticSearch 入门与深入
        - 环境搭建 / 搜索与聚合 / 架构原理 / 数据建模
    - ElasticSearch 集群管理
        - 水平扩展及性能优化 / 最佳实践
    - ELK 进行大数据分析
        - 可视化分析 / 时序型数据 / 异常检测
    - 项目实战和知识点回顾
        - 电影搜索 / 问卷分析 / Elastic认证
- 学习建议
    - 勤动手
        - 本地搭建多节点的集群环境，理解分布式工作原理，执行教程中的每一个范例
    - 多思考
        - 结合实际的业务场景，深入思考，学会查阅相关文档
    - 定目标
        - 做一次分享，开发一个具体的项目，参加 Elastic 认证考试
#03 ElasticSearch 简介及其发展历史
- 起源 - Lucene
    - 基于 Java 语言开发的搜索引擎库类
    - 创建于 1999 年，2005 年成为 Apache 顶级开源项目
    - Lucene 具有高性能、易扩展的优点
    - Lucene 的局限性：
        - 只能基于 Java 语言开发
        - 类库的接口学习曲线陡峭
        - 原生并不支持水平扩展
- ElasticSearch 的诞生
    - 2004 年 Shay Banon 基于 Lucene 开发了 Compass
    - 2010 年 Shay Banon 重写了 Compass，取名 ElasticSearch
        - 支持分布式，可水平扩展
        - 降低全文检索的学习曲线，可以被任何编程语言调用
- ElasticSearch 的分布式架构
    - 集群规模可以从单个扩展至数百个节点
    - 高可用 & 水平扩展
        - 服务和数据两个维度
    - 支持不同的节点类型
        - 支持 Hot & Warm 架构
- 多种方式的集成接入
    - 多种编程语言的类库 （http://www.elastic.co/guide/en/elasticsearch/client/index.html）
        - Java / .NET / Python / PHP / Groovy / Perl
    - RESTful API v.s Transport API
        - 9200 v.s 9300 (建议使用RESTful API)
    - JDBC & ODBC
- ElasticSearch 的主要功能
    - 海量数据的分布式存储以及集群管理
        - 服务与数据的高可用、水平扩展
    - 近实时搜索，性能卓越
        - 结构化 / 全文 / 地理位置 / 自动完成
    - 海量数据的近实时分析
        - 聚合功能
- 市场反应
    - 2010 年第一次发布；2012 年成立公司
    - 成立 6 个月，160 万下载，首轮募到 1000 万美金风险投资
        - Rod Johnson
        - Benchmark Capital / Data Collective
    - “不要求你必须是一位数据科学家才能把它用好”
- ElasticSearch 版本与升级
    - 0.4：2010 年 2 月第一次发布
    - 1.0：2014 年 1 月
    - 2.0：2015 年 10 月
    - 5.0：2016 年 10 月
    - 6.0：2017 年 10 月
    - 7.0：2019 年 4 月
- 新特性 5.x
    - Lucene 6.x，性能提升，默认打分机制从 TF-IDF 改为 BM 25
    - 支持 Ingest 节点 / Painless Scripting / Completion suggested 支持 / 原生的 Java REST 客户端
    - Type 标记成 deprecated，支持 Keyword 的类型
    - 性能优化：
        - 内部引擎移除了避免同一文档并发更新的竞争所，带来 15% - 20% 的性能提升
        - Instant aggregation，支持分片上聚合的缓存
        - 新增了 Profile API
- 新特性 6.x
    - Lucene 7.x
    - 新功能
        - 跨集群复制（CCR）
        - 索引生命周期管理
        - SQL 的支持
    - 更友好的升级及数据迁移
        - 在主要版本之间的迁移更为简单，体验升级
        - 全新的基于操作的数据复制框架，可加快恢复数据
    - 性能优化
        - 有效存储稀疏字段的新方法，降低了存储成本
        - 在索引时进行排序，可加快排序的查询性能
- 新特性 7.x
    - Lucene 8.x
    - 重大改进 - 正式废除单个索引下多 Type 的支持
    - 7.1 开始，Security 功能免费使用
    - ECK - ElasticSearch Operator Kubernetes
    - 新功能
        - New Cluster Coordination
        - Feature-Complete High Level REST Client
        - Script Score Query
    - 性能优化
        - 默认的 Primary Shard 数从 5 改为 1，避免 Over Sharding
        - 性能优化，更快的 Top K
        
#04 ElasticSearch 家族成员及其应用场景
- Elastic Stack 生态圈
    - ![Image text](https://raw.githubusercontent.com/hongmaju/light7Local/master/img/productShow/20170518152848.png)
#05 ElasticSearch 的安装与简单配置
#06 Kibana 的安装与界面快速浏览
#07 在 Docker 容器中运行 ElasticSearch 和 Cerebro
#08 Logstash 安装与导入数据
#09 基本概念：索引、文档和 RESTAPI
#10 基本概念：节点、集群、分片及副本
#11 文档的基本 CRUD 与批量操作
#12 倒排索引介绍
#13 通过 Analyzer 进行分词
#14 SearchAPI 概览
#15 URISearch 详解
#16 RequestBody 与 QueryDSL 简介
#17 QueryString & SimpleQueryString 查询
#18 DynamicMapping 和常见字段类型
#19 显式 Mapping 设置与常见参数介绍
#20 多字段特性及 Mapping 中配置自定义 Analyzer
#21 Index Template 和 Dynamic Template
#22 ElasticSearch 聚合分析简介
#23 第一部分总结
#24 基于词项和基于全文的搜索
#25 结构化搜索
#26 搜索的相关性算分
#27 Query & Filtering 与字符串多字段查询
#28 单字符串多字段查询：DisMaxQuery
#29 单字符串多字段查询：MultiMatch
#30 多语言及中文分词与检索
#31 Space-Jam，一次全文搜索的实例
#32 使用 Search-Template 和 Index-Alias 查询
#33 综合排序：Function-Score-Query 优化算法
#34 Term & Phrase-Suggester
#35 自动补全与基于上下文的提示
#36 配置跨集群搜索
#37 集群分布式模型及选主与脑裂问题
#38 分片与集群的故障迁移
#39 文档分布式存存储
#40 分片及其生命周期
#41 剖析分布式查询及相关性算分
#42 排序及 DocValues & Fielddata
#43 分页与遍历：From，Size，SearchAfter & ScrollAPI
#44 处理并发读写操作
#45 Bucket & Metric 聚合分析及嵌套聚合
#46 Pipeline 聚合分析
#47 作用范围与排序
#48 聚合分析的原理及精准度问题
#49 对象及 Nested 对象
#50 文档的父子关系
#51 UpdateByQuery & ReindexAPI
#52 IngestPipeline & PainlessScript
#53 ElasticSearch 数据建模实例
#54 ElasticSearch 数据建模最佳实践