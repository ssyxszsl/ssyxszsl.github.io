---
layout: single
permalink: /
title: "个人学术主页"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<span id="about"></span>

## 个人简介

我叫**史少阳**，现为北京理工大学机械与车辆学院车辆工程专业硕博连读研究生，导师为秦也辰教授，预计于 **2027 年 6 月**毕业。

我的研究主要聚焦于智能车辆决策、规划与控制，包括：

- 风险感知强化学习与安全决策
- 自动驾驶轨迹规划与模型预测控制
- 感知不确定性评估与风险建模
- 激光雷达点云处理与高程地图构建
- 非结构化环境可通行性分析与路径规划

目前主要使用 Python、C++、MATLAB、ROS 和 PyTorch 开展算法研究、仿真测试与实验验证。

[查看 GitHub](https://github.com/ssyxszsl){: .btn .btn--primary }
[下载 PDF 简历]({{ "/files/resume.pdf" | relative_url }}){: .btn .btn--inverse }


<span id="education"></span>

## 教育背景

### 北京理工大学

**车辆工程｜硕博连读（推荐免试）**  
2021.09—2027.06

- 导师：秦也辰 教授
- 研究方向：智能车辆规划与控制
- 预计毕业时间：2027 年 6 月

### 北京化工大学

**机械工程｜工学学士**  
2017.09—2021.06

- 导师：王维民 教授
- 本科专业排名：第 1 名，共 125 人


<span id="projects"></span>

## 项目经历

### 基于风险感知自进化强化学习的自动驾驶决策与规划系统研究

**负责人｜2025.10—2026.06**

面向高速、多车密集交互驾驶场景，构建“强化学习决策—模型预测控制规划—在线风险监督”一体化系统，使驾驶策略能够持续适应动态交通风险，并提升复杂驾驶场景中的安全性和鲁棒性。

主要工作：

- 融合自车与周围车辆状态，基于 SAC 模型输出目标速度和横向位置，实现跟驰、换道与超车决策。
- 构建风险价值网络预测短时碰撞风险，并利用最新交互数据进行周期性更新。
- 将风险估计引入强化学习奖励塑形，驱动驾驶策略持续向低风险行为演化。
- 将 SAC 高层决策嵌入 MPC 轨迹优化，加入车辆动力学、道路边界和碰撞规避约束。
- 当风险超过阈值时切换至保守策略，实现在线安全监督和规划兜底。
- 完成硬件在环实验验证。

相关成果：

- A Risk-Aware Decision Making and Motion Planning Framework for Interactive Autonomous Driving，ITSC 2026。
- Policy-conditioned Risk-aware Safe Reinforcement Learning with Model-Based Planning for Autonomous Driving，Expert Systems with Applications，审稿中。

---

### 感知不确定性驱动的自动驾驶风险自适应轨迹规划系统

**负责人｜2024.04—2026.03｜国家重点研发计划子课题**

面向遮挡、传感器噪声和长尾目标导致感知不确定性上升的复杂驾驶场景，构建感知不确定性驱动的风险自适应轨迹规划框架，实现感知可靠性量化、风险建模与规划决策的协同优化。

主要工作：

- 基于 Monte Carlo Dropout 改进 PointPillars 三维目标检测器。
- 联合建模分类不确定性和定位回归不确定性，输出目标级感知风险指标。
- 将感知不确定性引入 MPC 的轨迹跟踪权重、碰撞规避权重和障碍物势场。
- 感知风险升高时自动扩大安全距离，并降低激进跟踪行为。
- 融合多帧检测与跟踪信息，平滑时序不确定性估计。
- 结合车辆动力学、道路边界及执行器约束生成连续可行的安全轨迹。

相关成果：

- Perceptual Uncertainty-aware Trajectory Planning for Autonomous Vehicles，IEEE Transactions on Vehicular Technology，审稿中。
- 一种自动驾驶轨迹规划方法、系统、设备、介质及产品，发明专利，实质审查。
- 一种面向自动驾驶的感知不确定性评估方法，发明专利，实质审查。

---

### 分辨率自适应高程建图与路面预瞄感知系统

**负责人｜2023.04—2025.12**

面向智能悬架与底盘控制的路面预瞄需求，构建融合点云分割、属性感知更新与自适应分辨率优化的道路表面预瞄方法，为车辆悬架和底盘控制提供高精度前方路面信息。

主要工作：

- 基于局部 RANSAC 点云分割区分地面点和非地面点。
- 针对道路与障碍物区域设计差异化地图更新策略。
- 基于栅格高程方差构建四叉树细分机制。
- 在平坦区域保持较低分辨率，在起伏区域动态加密。
- 根据车辆运动学模型预测四轮轨迹并提取前方路面高程。
- 完成仿真与实车实验验证。

相关成果：

- Resolution-adaptive elevation mapping based road surface preview method for intelligent vehicles，Measurement，2026，272：121066。
- 一种基于点云输入的路面预瞄方法、系统、设备及介质，发明专利。

---

### 面向非结构化地形的无人平台可通行性建模与自适应路径规划

**主要参与｜2024.01—2026.06**

面向坡面、台阶、碎石及起伏地形等非结构化环境，构建考虑平台运动能力和稳定性约束的可通行性路径规划框架。

主要工作：

- 基于 LiDAR 和 IMU 构建高程地图。
- 提取坡度、台阶高度和地形粗糙度等地形特征。
- 将离地间隙、最大爬坡角、越障高度和横向稳定性约束映射至代价地图。
- 在路径搜索代价中融合地形风险、曲率变化与换向惩罚。
- 生成兼顾安全性、平滑性和可执行性的路径。

相关成果：

- Optimized 3D Path Planning for Unmanned Platforms in Complex Unstructured Environments，CVCI 2024。
- Navigation of Ground Unmanned Platforms with Adaptive Traversability in Unstructured Terrain，CVCI 2026，审稿中。


<span id="competition"></span>

## 相关竞赛

### Onsite 自动驾驶算法挑战赛——乘用车行车赛道 PNC 算法开发

**负责人｜2024.03—2024.06**

竞赛任务为开发自动驾驶规划与控制算法，并基于 2000 余个闭环仿真场景进行多维度评分。

竞赛成绩：

- 第二届：第 7 名，共 43 支队伍
- 第三届：第 4 名，共 56 支队伍

主要工作：

- 实现全局规划、局部规划 EM Planner 和纯追踪轨迹跟踪算法。
- 设计驾驶场景识别器。
- 针对大曲率场景设计采样式 IDM 规划算法。
- 设计基于周围车辆和交通灯状态的自适应参考车速模块。
- 在规划算法中加入横摆角速度限制。
- 设计基于曲率与车速的自适应预瞄距离选取模块。

[查看部分项目效果](https://github.com/ssyxszsl)


<span id="publications"></span>

## 科研成果

### 期刊论文

1. **Shaoyang Shi et al.** Resolution-adaptive elevation mapping based road surface preview method for intelligent vehicles. *Measurement*, 2026, 272: 121066.

2. **Shaoyang Shi et al.** Perceptual Uncertainty-aware Trajectory Planning for Autonomous Vehicles. *IEEE Transactions on Vehicular Technology*. Under review.

3. **Shaoyang Shi et al.** Policy-conditioned Risk-aware Safe Reinforcement Learning with Model-Based Planning for Autonomous Driving. *Expert Systems with Applications*. Under review.

### 会议论文

1. **Shaoyang Shi, et al.** A Risk-Aware Decision Making and Motion Planning Framework for Interactive Autonomous Driving. *2026 IEEE International Conference on Intelligent Transportation Systems (ITSC)*, 2026: 399–406.

2. **Yifei Han, Shaoyang Shi, et al.** Optimized 3D Path Planning for Unmanned Platforms in Complex Unstructured Environments. *CAA International Conference on Vehicular Control and Intelligence (CVCI)*, 2024.

3. **Xiaoxi Nie, Shaoyang Shi, et al.** Navigation of Ground Unmanned Platforms with Adaptive Traversability in Unstructured Terrain. *CVCI 2026*. Under review.

### 发明专利

- 秦也辰、史少阳等：一种自动驾驶轨迹规划方法、系统、设备、介质及产品，实质审查。
- 秦也辰、史少阳等：一种面向自动驾驶的感知不确定性评估方法，实质审查。
- 秦也辰、史少阳等：一种基于点云输入的路面预瞄方法、系统、设备及介质。


<span id="honors"></span>

## 荣誉与奖励

- 国家奖学金，两次
- 一等学业奖学金
- 优秀党员
- 优秀团干部
- 京彩大创市级一等奖
- 北京化工大学机械工程专业本科排名第 1
- 大学英语六级 CET-6


<span id="skills"></span>

## 专业能力

### 智能驾驶规划与控制

- 路径规划与轨迹规划
- 模型预测控制 MPC
- 深度强化学习 SAC、DDPG
- 车辆动力学约束规划
- 轨迹跟踪与横纵向控制
- CARLA、PRESCAN 闭环仿真
- 硬件在环实验验证

### 感知、定位与建图

- 激光雷达点云处理
- SLAM 与环境建图
- 三维目标检测
- 高程地图构建
- 感知不确定性评估
- 非结构化地形可通行性分析

### 编程与开发

- Python
- C++
- MATLAB
- Linux
- ROS
- Git
- PyTorch
- Origin

### 深度学习与数据处理

- PointNet
- PointPillars
- CenterPoint
- BEV 感知方法
- Monte Carlo Dropout
- 数据处理、可视化与统计分析


<span id="contact"></span>

## 联系方式

- 邮箱：[shishaoyang@bit.edu.cn](mailto:shishaoyang@bit.edu.cn)
- GitHub：[github.com/ssyxszsl](https://github.com/ssyxszsl)
- 所在单位：北京理工大学
- 所在城市：北京，中国

[下载 PDF 简历]({{ "/files/resume.pdf" | relative_url }}){: .btn .btn--primary }
