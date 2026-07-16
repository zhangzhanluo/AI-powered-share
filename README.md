# AI 助力工作：工具与方法分享

组内技术分享资料。以「杰文斯悖论」为引子（成本越低、需求越大），围绕「多任务并行」展开，落到三个问题（提升复杂任务处理能力 / 第一时间触达 / 实时监控）与对应工具方法，并附思考。

- **分享人**：张战罗
- **面向**：组内同事
- **当前版本**：2.3（杰文斯悖论引子 + 多任务并行三问；按修改意见完善内容、修复 P04 页塌陷）

---

## 内容概览

以「杰文斯悖论」为引子（成本越低、需求越大），落到「多任务并行」三个问题与对应工具方法：

1. **问题一·提升复杂任务处理能力 · PRE 工程（臭皮匠工程）** —— 多角色分工与协调与监督（规划 / 执行 / 审核三角色分工 + 监督者调度），监督者单点 cron + headless `claude -p --resume` 续跑替换原 /loop 三终端；附 ros-ai-builder 真实案例。对应资源：`src/pre-engineering-main`
2. **问题二·第一时间触达 · 通知机制** —— 决策走网页表单弹窗（`decision-form.py`）、复杂任务完成自动生成报告并弹浏览器。
3. **问题三·实时监控 · Claude Code Agent Monitor** —— 跨项目多会话实时监控面板。对应资源：`src/Claude-Code-Agent-Monitor-master`
4. **思考** —— 变与不变、礁石与船、prompt→context→harness→loop 四代范式演进；结尾张杰「未来已来，唯变不变」。

---

## 目录结构

```
.
├── 分享文档.md          # 讲稿与讲义（配合演示使用）
├── ppt/
│   ├── index.html       # 单文件横滑演示文稿（IKB 克莱因蓝主题）
│   ├── assets/          # 本地动画（motion.min.js，离线兜底）
│   └── images/          # 演示用图
├── 一些想法.md          # 分享大纲（与 28 页 PPT 一一对应）
├── versions.md          # 版本记录
├── src.txt              # src/ 三个子项目的来源仓库链接
└── src/                 # 引用的源项目（已 gitignore，本地自备）
    ├── tech-report-template/             # LaTeX 技术文档模板（自有）
    ├── pre-engineering-main/            # PRE 多智能体协作框架（自有）
    └── Claude-Code-Agent-Monitor-master/ # Claude Code 监控面板（第三方）
```

> `src/` 已在 `.gitignore` 中忽略。其中 `tech-report-template` 与 `pre-engineering-main` 为作者自有仓库，`Claude-Code-Agent-Monitor-master` 为第三方项目。三个仓库的来源地址见 `src.txt`。

---

## 使用

**查看演示稿**：直接用浏览器打开 `ppt/index.html`。

- 键盘：`←` / `→` 翻页，`Esc` 退出概览（概览下可点击跳转）
- 内容是纯前端单文件，无需构建、无需依赖

**阅读讲稿**：打开 `分享文档.md`。

---

## 关联仓库

- PRE Engineering：<https://github.com/zhangzhanluo/pre-engineering>
- tech-report-template：<https://gitcode.com/zlzhang/tech-report-template>
- Claude-Code-Agent-Monitor：<https://github.com/hoangsonww/Claude-Code-Agent-Monitor>
