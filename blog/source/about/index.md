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
      <div class="title">Java 后端开发实习生</div>
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
.resume-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  font-family: 'PingFang SC', 'Microsoft YaHei', sans-serif;
}

.resume-header {
  text-align: center;
  margin-bottom: 3rem;
  animation: fadeIn 1s ease-in;
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  padding: 2rem;
  border-radius: 12px;
}

.header-content {
  margin-bottom: 1.5rem;
}

.name {
  font-size: 2.8rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
  font-weight: bold;
}

.title {
  font-size: 1.8rem;
  color: #34495e;
  margin-bottom: 1.5rem;
}

.highlight-badges {
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
}

.highlight-badge {
  background: #3498db;
  color: white;
  padding: 0.6rem 1.2rem;
  border-radius: 25px;
  font-size: 1rem;
  font-weight: 500;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.contact-info {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-top: 1rem;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: #7f8c8d;
  font-size: 1.1rem;
}

.core-advantages {
  margin-bottom: 4rem;
}

.advantages-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.advantage-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  text-align: center;
  transition: transform 0.3s ease;
}

.advantage-card:hover {
  transform: translateY(-5px);
}

.advantage-icon {
  font-size: 2.5rem;
  color: #3498db;
  margin-bottom: 1rem;
}

.advantage-card h3 {
  color: #2c3e50;
  margin-bottom: 1rem;
  font-size: 1.3rem;
}

.advantage-card p {
  color: #7f8c8d;
  line-height: 1.6;
}

.resume-section {
  margin-bottom: 4rem;
  animation: slideUp 0.8s ease-out;
}

.resume-section h2 {
  color: #2c3e50;
  border-bottom: 3px solid #3498db;
  padding-bottom: 0.8rem;
  margin-bottom: 2rem;
  font-size: 1.8rem;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.skill-card {
  background: white;
  padding: 1.8rem;
  border-radius: 12px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.skill-card:hover {
  transform: translateY(-5px);
}

.skill-card h3 {
  color: #2c3e50;
  margin-bottom: 1.2rem;
  font-size: 1.3rem;
  display: flex;
  align-items: center;
  gap: 0.8rem;
}

.skill-card ul {
  list-style: none;
  padding: 0;
}

.skill-card li {
  margin-bottom: 0.8rem;
  color: #7f8c8d;
  padding-left: 1.5rem;
  position: relative;
}

.skill-card li:before {
  content: "•";
  color: #3498db;
  position: absolute;
  left: 0;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.project-card {
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  overflow: hidden;
  transition: transform 0.3s ease;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-header {
  background: #f8f9fa;
  padding: 1.5rem;
  border-bottom: 1px solid #e9ecef;
}

.project-header h3 {
  color: #2c3e50;
  margin-bottom: 0.8rem;
  font-size: 1.4rem;
}

.project-tech {
  color: #7f8c8d;
  font-size: 0.9rem;
}

.project-content {
  padding: 1.5rem;
}

.project-intro {
  margin-bottom: 1.5rem;
}

.project-intro h4 {
  color: #2c3e50;
  margin-bottom: 0.8rem;
  font-size: 1.2rem;
}

.project-intro p {
  color: #7f8c8d;
  line-height: 1.6;
}

.project-achievements h4 {
  color: #2c3e50;
  margin-bottom: 1rem;
  font-size: 1.2rem;
}

.project-achievements ul {
  list-style: none;
  padding: 0;
}

.project-achievements li {
  margin-bottom: 1rem;
  color: #7f8c8d;
  line-height: 1.6;
}

.project-achievements strong {
  color: #2c3e50;
}

.timeline {
  position: relative;
  padding-left: 2rem;
}

.timeline-item {
  position: relative;
  margin-bottom: 2rem;
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.timeline-date {
  color: #3498db;
  font-weight: bold;
  margin-bottom: 0.8rem;
  font-size: 1.1rem;
}

.timeline-content h3 {
  color: #2c3e50;
  margin-bottom: 0.5rem;
  font-size: 1.3rem;
}

.position {
  color: #7f8c8d;
  margin-bottom: 1rem;
  font-size: 1.1rem;
}

.timeline-content ul {
  list-style: none;
  padding: 0;
}

.timeline-content li {
  margin-bottom: 0.8rem;
  color: #7f8c8d;
  padding-left: 1.5rem;
  position: relative;
}

.timeline-content li:before {
  content: "•";
  color: #3498db;
  position: absolute;
  left: 0;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .resume-header {
    padding: 1.5rem;
  }

  .name {
    font-size: 2.2rem;
  }

  .title {
    font-size: 1.4rem;
  }

  .contact-info {
    flex-direction: column;
    gap: 0.8rem;
  }

  .highlight-badges {
    gap: 0.8rem;
  }

  .highlight-badge {
    font-size: 0.9rem;
    padding: 0.5rem 1rem;
  }

  .skills-grid,
  .projects-grid {
    grid-template-columns: 1fr;
  }

  .advantage-card {
    padding: 1.5rem;
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

## 专业技能
### 编程语言
- 熟练掌握Java语言基础，熟练使用多线程、异步并发、分布式、事务IO、集合、HashMap等基础和进阶内容。

### 框架与技术
- 掌握使用Spring Boot、Spring MVC、MyBatis、MyBatis-Plus，熟悉IOC、AOP思想并有具体实现和想法。
- 基于Spring Security+JWT实现分布式权限管理，支持200+用户并发访问，通过角色-权限-资源三级映射，将接口访问控制粒度细化至按钮级别。

### 数据库
- 掌握MySQL数据库设计、复杂Sql脚本编写、服务器主从复制、事务隔离级别、事务回滚、索引优化、慢SQL和SQL执行计划、B+树数据结构、锁机制、表锁和行锁以及InnoDB存储引擎。
- 熟悉数组、链表、栈、队列、二叉树、红黑二叉树、常用排序等基本的数据结构和算法。
- 理解微服务cloud及其常用组件Nacos、druid、Tidb的使用。

### 运维与工具
- 熟悉Linux环境部署及日志分析、Docker及K8S集群。
- 熟悉Redis非关系型NoSql数据库，及其业务场景中的缓存穿透、击穿、雪崩、双写一致性以及对应的处理方法，了解Redis持久化，以及配合Lua脚本实现原子化高并发高可用架构。
- 熟练掌握IDE工具：IDEA、Navicat、Shell、VS Code，熟悉GIT及其回溯、追踪和冲突合并。
- 熟悉RabbitMq延迟队列、消息异步的具体应用。

## 工作经历
### 2023.07 - 至今 | 上海标杆供应链科技有限公司 | Java后端开发实习生
- 主要参与公司WEB系统（WMS\TMS）系统开发，移动端APP和小程序开发。
- 独立负责架构设计和逻辑实现，后台API接口开发、部署和上线。
- 参与实际需求分析，配合产品确定需求实现和人工天到项目和功能落地。
- 技术支持：解决线上系统故障，提供售后技术方案，客户满意度达95%。

## 项目经历
### 2023.7-至今 | 富鹊云智慧WMS | JAVA后端开发
#### 项目介绍
此项目是公司基于10年+供应链实操经验研发的一套行业级的产品。“WMS”融合了软件系统：OMS(订单管理)、SRM(采购管理)、WMS(仓储作业)、TMS(运输管理)四套系统并兼容PDA、AGV调度、智能电子秤还有小程序等与物联网深度融合，实现各设备间的互联互通，同时WMS系统开放API平台和异步回传以实现系统间数据无缝流转能力。为有仓储的企业提供整套、智能、安全、稳定的产品方案。

#### 系统架构（文字描述）
WMS系统采用微服务架构，通过Nacos实现服务注册发现，RabbitMQ处理异步消息，MinIO存储文件。

#### WEB技术选型
Spring Boot、MySql、MyBatis、MyBatis-plus、Redis、Rabbitmq、Alibaba Druid、Quartz、RestTemplate、VUE2、MiniIO

#### 岗位职责
1. 设计RESTful API实现跨系统数据同步(OMS/SRM/TMS)，日均处理单据5W+，系统可用性达99.9%。
2. 担任核心开发，独立负责餐饮行业益禾堂及工业级泰坦客户的协同开发和对接。
3. 在益禾堂对接项目中，通过Druid监控定位慢SQL，针对订单查询场景设计复合索引，使慢查询从日均2000条降至800条，数据库响应时间缩短40%。PDA移动端协同：实现实时数据同步功能，提升仓储作业效率40%。
4. 主要完成了：出库单管理、实时库存管理、报表导出及电子标签业务流程和责任描述。
5. 通过WMS开放API完成基础配置的SKU、货主、承运人、分仓、库位、供应商、客户门店基础数据的同步与修改，以及三方系统下单推入完成入库(收货上架SKU)和出库(装箱发运)来实现业务的无缝衔接。
6. 配置Druid来监控sql的执行、统计、监控、实时链接等，以方便后期针对性优化。
7. 通过自研动态分配算法实时派发订单并根据库存分配规则即时匹配实时下发PDA或小程序提高仓库作业效率。
8. 使用EasyExcel框架配合多线程事务，实现每一万条业务数据导入(10线程)仅需1.7秒且中间出错可即时回滚保障性能同时确保数据安全性。
9. 动态定时任务Quartz框架可以在规定的时间将漏掉的单据自动补发，从而节省繁琐的人工操作。
10. Rabbitmq做异步延迟队列和同步队列向上游或下游系统同步单据处理状态并保存响应结果实现系统操作交互。
11. 配合移动端PDA或微信小程序可以快速收货上架商品和出库拣货并且与WEB端数据实时同步方便查询实时状态。
12. 配合MINIIO实现APP软件包自动更新，最大程度降低BUG对现场操作的风险。
13. 配合微信小程序消息订阅推送可实时提醒指定的仓储人员完成作业，极大程度降低现场空闲时间，提高作业效率。

### 2024.1-至今 | 智能TMS运输系统 | JAVA后端开发
#### 项目介绍
此项目是供应链的运输环节，此系统通过物联网技术实现仓库订单出库之后，订单的实时监控和调度，运输过程的优化结合高德API实时分析让运输过程可控高效。该系统与WMS系统无缝对接，为企业提供整套的解决方案。

#### 技术栈
Spring Boot、Redis、JWT、MyBatis、MyBatis-plus、MySql、Redis、MongoDB、Rabbitmq、Alibaba Druid、Quartz、RestTemplate、VUE2、MiniIO

#### 岗位职责
主要完成了运单管理、运费管理、提货、签收。

#### 技术描述
1. 基于RBAC模型实现权限控制，支持200+用户并发访问，系统响应时间<500ms。
2. 借助mango db实现司机定位实时同步并计算收费信息和奖励，用户体验较好。
3. 借助Spring Boot框架中的MultipartFile特性，实现了签收文件上传到指定目录功能。
4. 集成Apache POI和EasyExcel实现数据导出功能，支持万级数据生成Excel文件。

## 自我评价
- 技术能力：熟悉Java生态技术栈，曾独立解决线上缓存雪崩问题，将系统恢复时间从4小时缩短至30分钟。
- 协作能力：在跨部门协作中积极沟通，成功推动WMS-TMS系统集成项目按期交付。
- 学习能力：主动学习微服务架构，一个月内掌握并在项目中应用，获得团队认可。
- 在项目经历中，展现了出色的技术能力和业务理解，通过技术创新和优化提高了系统性能和用户体验。
- 期待加入一个充满挑战和机遇的工作环境，为客户提供高质量的产品，同时也为自己的职业发展积累宝贵的经验。
