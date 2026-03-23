---
title: 关于我
date: 2023-03-23 18:53:50
---
# 个人简历
<div class="resume-container">
  <!-- 头部信息 -->
  <div class="resume-header">
    <div class="header-content">
      <h1 class="name">付伟亮</h1>
      <div class="title">Java 后端开发</div>
      <div class="highlight-badges">
        <span class="highlight-badge">2年经验</span>
        <span class="highlight-badge">高并发架构</span>
        <span class="highlight-badge">性能优化</span>
      </div>
    </div>
    <div class="contact-info">
      <div class="contact-item"><i class="fas fa-phone"></i> 185-7920-3611</div>
      <div class="contact-item"><i class="fas fa-envelope"></i> 2194094699@qq.com</div>
      <div class="contact-item"><i class="fas fa-globe"></i> fuwelliang.eu.org</div>
    </div>
  </div>

<style>
:root {
  --resume-bg: #f3f6fb;
  --resume-card: #ffffff;
  --resume-text: #1f2937;
  --resume-muted: #64748b;
  --resume-primary: #2563eb;
  --resume-primary-soft: #dbeafe;
  --resume-border: #e2e8f0;
  --resume-shadow: 0 10px 30px rgba(15, 23, 42, 0.08);
}

.resume-container {
  max-width: 1000px;
  margin: 0 auto 2rem;
  padding: 2.2rem;
  font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
  background: radial-gradient(circle at 0% 0%, #eff6ff 0, #f8fafc 38%, #f8fafc 100%);
  border: 1px solid var(--resume-border);
  border-radius: 20px;
  box-shadow: var(--resume-shadow);
}

.resume-header {
  text-align: center;
  background: linear-gradient(140deg, #ffffff 0%, #eff6ff 100%);
  padding: 2rem;
  border-radius: 16px;
  border: 1px solid #dbeafe;
  animation: fadeIn 0.8s ease-in;
}

.header-content {
  margin-bottom: 1.2rem;
}

.name {
  margin: 0 0 0.6rem;
  font-size: 2.6rem;
  line-height: 1.15;
  color: #0f172a;
  letter-spacing: 0.02em;
}

.title {
  margin-bottom: 1.2rem;
  font-size: 1.25rem;
  color: #334155;
  font-weight: 600;
}

.highlight-badges {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 0.75rem;
}

.highlight-badge {
  display: inline-flex;
  align-items: center;
  padding: 0.45rem 0.95rem;
  border-radius: 999px;
  font-size: 0.92rem;
  font-weight: 600;
  color: #1e3a8a;
  background: var(--resume-primary-soft);
  border: 1px solid #bfdbfe;
}

.contact-info {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 1.2rem;
  margin-top: 1rem;
}

.contact-item {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  color: var(--resume-muted);
  font-size: 0.98rem;
  background: #ffffff;
  border: 1px solid var(--resume-border);
  border-radius: 999px;
  padding: 0.35rem 0.85rem;
}

.resume-main {
  max-width: 1000px;
  margin: 2.2rem auto 0;
  padding: 2.2rem;
  font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
  color: var(--resume-text);
  background: var(--resume-card);
  border: 1px solid var(--resume-border);
  border-radius: 20px;
  box-shadow: var(--resume-shadow);
}

.resume-main h1,
.resume-main h2,
.resume-main h3 {
  position: relative;
  color: #0f172a;
  line-height: 1.3;
}

.resume-main h1 {
  margin-top: 0;
  margin-bottom: 1.4rem;
  font-size: 2rem;
}

.resume-main h2 {
  margin-top: 2.2rem;
  margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  font-size: 1.45rem;
  border-bottom: 2px solid #e2e8f0;
}

.resume-main h3 {
  margin-top: 1.6rem;
  margin-bottom: 0.75rem;
  font-size: 1.14rem;
  color: #1e3a8a;
}

.resume-main p,
.resume-main li {
  line-height: 1.8;
  color: #334155;
}

.resume-main ul,
.resume-main ol {
  margin-top: 0.4rem;
  margin-bottom: 1rem;
  padding-left: 1.3rem;
}

.resume-main li {
  margin-bottom: 0.4rem;
}

.resume-main hr {
  border: 0;
  height: 1px;
  margin: 1.8rem 0;
  background: linear-gradient(to right, rgba(37, 99, 235, 0), rgba(37, 99, 235, 0.4), rgba(37, 99, 235, 0));
}

.resume-main strong {
  color: #0f172a;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(8px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .resume-container,
  .resume-main {
    border-radius: 14px;
    padding: 1.35rem;
  }

  .name {
    font-size: 2rem;
  }

  .title {
    font-size: 1.05rem;
  }

  .contact-info {
    flex-direction: column;
    align-items: center;
    gap: 0.6rem;
  }

  .resume-main h1 {
    font-size: 1.7rem;
  }

  .resume-main h2 {
    font-size: 1.3rem;
    margin-top: 1.9rem;
  }
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  });

  document.querySelectorAll('.resume-section').forEach((section) => {
    section.style.opacity = '0';
    section.style.transform = 'translateY(20px)';
    section.style.transition = 'all 0.8s ease-out';
    observer.observe(section);
  });
});
</script>
</div>

<div class="resume-main">

# 个人简历

## 基本信息

- **姓名**：付伟亮
- **求职意向**：Java 后端开发｜供应链 / WMS / TMS｜AI 工具融合实践（Cursor / Claude CLI / Dify / n8n）
- **工作经验**：2 年半
- **联系电话**：185-7920-3611
- **邮箱**：isfuweiliang@qq.com
- **个人博客**：fuwelliang.eu.org

---

## 个人优势

### 后端开发

- 熟练掌握 Java 基础，熟悉集合、多线程、并发编程、线程池、锁机制、NIO 等常用技术。
- 熟悉 Spring Boot、Spring Cloud 基础、Nacos、MyBatis、MyBatis-Plus，能够独立完成业务模块设计与接口开发。

### 数据库 / 缓存 / 消息

- 熟悉 MySQL，具备表设计、索引优化、慢 SQL 分析、事务隔离、执行计划分析等经验。
- 熟悉 Redis，能够应用于缓存、分布式锁、热点数据处理、重复提交拦截等场景。
- 熟悉 RabbitMQ，具备异步消息处理、延迟队列、状态回传、系统解耦等实践经验。
- 了解 MongoDB，有司机定位数据存储与实时同步相关使用经验。

### 运维与工具

- 熟悉 Linux、Git、Docker，具备基础部署、日志排查和线上问题定位能力。
- 熟练掌握 IDEA、Navicat、Shell、VS Code 等工具，熟悉 Git。

### 前后端协作

- 了解 Vue、Element UI 基础，能够与前端进行接口联调、字段约定和联动问题排查。

### AI 应用能力

- 在项目中实际使用过 Cursor、Claude CLI、Skills、Agents、Dify、n8n、Coze 等 AI 工具和平台，能够结合研发、运维、业务支持等场景进行融合应用。
- 熟悉基于 Prompt 的任务拆解、结构化输出、规则约束、上下文补充等方式，可用于异常分析、数据校验提示、文档生成等场景。
- 具备一定的 Agent 工作流设计意识，能够结合业务流程设计多步骤任务执行链路，用于提升研发效率和业务处理效率。
- 了解 Vibe Coding 协作模式，能够借助 AI 工具完成需求梳理、代码生成、重构优化、SQL 编写、接口联调辅助和文档沉淀。
- 可将 AI 能力应用于异常日志分析、批量导入错误说明、接口文档辅助生成、测试数据构造、研发提效等实际场景。

---

## 工作经历

### 上海标杆供应链科技有限公司 ｜ Java 后端开发工程师
**2023.07 - 至今**

负责公司供应链相关系统的后端研发与优化工作，参与 Web 仓储管理系统（WMS）、运输调度系统（TMS）、PDA 作业端、门店订货小程序等项目的功能开发、接口设计、性能优化、客户化需求支持及线上问题排查。

---

## 项目经历

## 富鹊云智慧 WMS

### 项目介绍

此项目是公司基于 10 年以上供应链实操经验研发的一套行业级产品。  
WMS 融合了以下软件系统：

- OMS（订单管理）
- SRM（采购管理）
- WMS（仓储作业）
- TMS（运输管理）

同时兼容 PDA、AGV 调度、智能电子秤以及小程序等，与物联网深度融合，实现各设备间的互联互通。  
WMS 系统开放 API 平台和异步回传能力，以实现系统间数据的无缝流转，为有仓储需求的企业提供整套智能、安全、稳定的产品方案。

### 系统架构（文字描述）

WMS 系统采用微服务架构，通过 Nacos 进行微服务治理，RabbitMQ 处理异步消息，MinIO 存储文件。

### Web 技术选型

- Spring Boot
- MySQL
- MyBatis
- MyBatis-Plus
- Redis
- RabbitMQ
- Alibaba Druid
- Quartz
- RestTemplate
- Vue2
- MinIO

---

## AI 工具融合与智能研发实践

### 使用工具

- Cursor
- Claude CLI
- Skills
- Agents
- Coze

### 智能研发实践

1. **AI 辅助研发提效**  
   在日常开发中结合 Cursor、Claude CLI 进行需求理解、代码生成、方法重构、SQL 编写、异常定位和接口联调辅助，提高日常开发效率。

2. **知识与技能沉淀**  
   通过 Skills 沉淀常用开发模式、代码模板、排查思路和业务处理经验，减少重复性工作，提高团队知识复用效率。

3. **业务工作流编排**  
   结合 Coze 搭建智能工作流，应用于导入错误说明优化、接口文档初稿生成等场景。

---

## 工作成果

1. 担任核心开发，独立负责餐饮行业益禾堂及工业级泰坦客户的协同开发和对接。
2. 实现 PDA 移动端协同，支持现场人员实时查询当前作业任务，并快速完成上架、拣货等操作流程，提升仓储作业效率 40%，同时实现全链路节点可跟踪，并可及时处理异常情况。
3. 配合动态库存分配算法，使 AGV 自行完成货物搬离、上架、补货，缺货时可配合微信小程序通知，极大减少缺货风险。
4. 通过 LOG 实时运行日志监控 WMS 系统执行、统计、监控、实时连接等，针对高频订单查询场景设计复合索引，快速定位问题并优化具体代码，提高用户体验，同时降低处理耗时对系统的风险。
5. 通过 WMS 开放 API 完成基础配置数据的同步与修正，包括：
    - SKU
    - 货主
    - 承运人
    - 分仓
    - 库位
    - 供应商
    - 客户门店基础数据
6. 对接三方系统下单推送，完成入库（收货上架 SKU）与出库（装箱发运）流程，实现业务无缝衔接。
7. 使用 EasyExcel 框架配合多线程事务，实现每万级业务数据并发导入，支持同步或异步导入；配合 RabbitMQ 使用异步延迟队列和同步队列，向上游或下游系统同步单据处理状态，并保存响应结果，实现系统操作交互。
8. 基于 Quartz 实现异步编排动态定时任务，可在指定时间自动补发漏掉的单据，节省繁琐人工操作，达到降本增效目的。
9. 配合 MinIO 实现 APP 软件包自动发布与自动更新，可实现最短 5 分钟修复严重 Bug，最大程度降低 Bug 对现场操作的风险。
10. 通过 Redis 分布式锁 + MyBatis-Plus 乐观锁，实现每天 5000+ 订单的重复拦截，做到零失误，为客户减少损失。

---

## 智能 TMS 运输系统

### 项目介绍

此项目聚焦供应链运输环节。系统通过物联网技术，在仓库订单出库后实现订单的实时监控和调度，并结合高德 API 进行运输过程优化分析，让运输过程更加可控、高效。  
该系统与 WMS 系统无缝对接，为企业提供整套仓配运协同解决方案。

### 技术栈

- Spring Boot
- MyBatis-Plus
- MySQL
- Redis
- RabbitMQ
- Quartz
- MongoDB
- JWT
- RestTemplate
- Vue2

### 主要职责

1. 负责 TMS 系统后端接口开发，参与物流订单、承运调度、运输状态流转等业务模块实现。
2. 参与运输规则相关逻辑开发，支持区域匹配、时间窗口、载重限制等业务场景。
3. 使用 MongoDB 处理司机端定位数据存储与同步，支撑运输轨迹监控和费用计算相关业务。
4. 集成快递 / 物流信息聚合查询能力，支持系统内统一查看物流状态。
5. 实现导出报表等业务功能，支持运营数据查看与批量导出。
6. 配合开放 API 对接第三方仓库及物流系统，实现订单流转和运输链路协同。

### 项目成果

1. 支撑物流订单从 WMS 到 TMS 的业务承接，提高仓配运一体化协同效率。
2. 基于 MongoDB 实现司机定位信息实时同步，增强运输过程可追踪性。
3. 通过接口整合和规则处理，降低运输过程中的信息割裂与人工切换成本。
4. 基于 EasyExcel 完成万级数据导出能力，满足运营分析和业务报表需求。
5. 在运输状态监控、轨迹同步、异常处理方面积累了实际项目经验。

---

## 自我评价

具备较扎实的 Java 后端开发基础和 2 年半供应链业务系统开发经验，能够独立完成后端功能开发、接口联调、线上问题排查。熟悉 WMS、TMS、PDA 等供应链业务场景，理解订单、库存、运输协同等核心流程，抗压能力强，可接受出差、驻场开发。

同时持续关注 AI 技术在研发和业务系统中的应用，已在项目实践中使用 Cursor、Claude CLI、Skills、Agents、Dify、n8n、Coze 等工具，结合 Vibe Coding 协作模式提升开发效率。

同时也是 LINUX DO 的成员。

</div>
