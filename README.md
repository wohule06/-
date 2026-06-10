# -
构建基于大模型的智能旅行规划 Agent，融合 MCP 工具调用与 RAG 检索增强技术，实现旅行需求理解、景点推荐、天气查询、酒店推荐及多日行程自动生成。系统采用 Agent Workflow 架构，通过高德地图 MCP Server 获取实时数据，并结合 Chroma 向量数据库与 Embedding 检索旅行知识库，实现工具调用与知识检索协同决策。项目引入异步并发、缓存优化及上下文压缩机制，有效降低响应时延并提升复杂任务规划能力。  技术栈： FastAPI、Qwen、MCP、LangGraph、Chroma、Embedding、AsyncIO、Redis

#智能旅行助手 ✈️

> 基于 **Agents 框架** 与 **FastAPI** 构建的 AI 驱动旅行规划助手，为你生成个性化、可落地的完整旅行方案。

## 🌟 项目简介
HelloAgents智能旅行助手是一个**前后端分离**的智能旅行规划系统，它结合大语言模型（LLM）、高德地图服务、天气数据与POI兴趣点信息，根据用户的目的地、出行时间、交通偏好、兴趣标签等需求，自动生成包含每日行程、景点推荐、餐饮安排、酒店建议、预算统计与天气提示的完整旅行计划，让你的出行准备更高效、更省心。

## ✨ 核心功能
- **🧠 AI 智能行程规划**：根据你的城市、日期、预算与偏好，自动生成多日详细行程
- **🗺️ 地图服务集成**：
  - POI 搜索与详情查询（景点/餐饮/酒店）
  - 步行/驾车/公共交通路线规划
  - 目的地未来天气查询与温度解析
- **📸 景点视觉增强**：接入 Unsplash API，为景点自动匹配高清图片
- **📊 结构化数据模型**：基于 Pydantic 定义完整请求/响应模型，自动生成 OpenAPI 文档
- **💰 智能预算统计**：自动汇总景点门票、酒店、餐饮与交通的预估费用
- **✅ 健壮的接口设计**：统一的 `success/message/data` 响应格式，完善的参数校验与错误处理

## 🛠️ 技术栈
- **后端**：Python, FastAPI, Pydantic, HelloAgents 框架
- **第三方服务**：高德地图 API, 大语言模型 (LLM), Unsplash API, 天气 API
- **前端**：TypeScript, Vite, 现代 HTML/CSS
- **工程化**：环境变量配置, 模块化架构, 自动 API 文档 (Swagger/Redoc)

## 🚀 快速开始
1.  **克隆项目**
    ```bash
    git clone https://github.com/your-username/helloagents-trip-planner.git
    cd helloagents-trip-planner
    ```
2.  **配置环境变量**
    - 复制 `backend/.env.example` 为 `backend/.env`，并填入你的 API Key（高德地图、LLM、Unsplash 等）
3.  **启动后端服务**
    ```bash
    cd backend
    pip install -r requirements.txt
    python run.py
    ```
4.  **启动前端服务**
    ```bash
    cd frontend
    npm install
    npm run dev
    ```
5.  **访问服务**
    - 后端 API 文档：`http://localhost:8000/docs`
    - 前端界面：`http://localhost:5173`

## 📁 项目结构
```
helloagents-trip-planner/
├── backend/                 # FastAPI 后端服务
│   ├── app/
│   │   ├── agents/          # AI 智能体核心逻辑
│   │   ├── api/             # API 路由层
│   │   ├── models/          # Pydantic 数据模型 (schemas.py)
│   │   └── services/        # 第三方服务集成 (地图/LLM/图片等)
│   ├── requirements.txt
│   └── run.py               # 服务启动入口
├── frontend/                # TypeScript + Vite 前端
│   ├── src/
│   ├── package.json
│   └── vite.config.ts
└── README.md
```

以上只展示/上传了后端代码前端代码没有展示，效果如下图所示
<img width="1912" height="1842" alt="image" src="https://github.com/user-attachments/assets/c0aa818e-37d0-4108-ae9a-3e7e68bb60c6" />
FastApi实现效果：
<img width="1914" height="4374" alt="image" src="https://github.com/user-attachments/assets/840c98eb-b2e4-4ade-9441-c13dc97de750" />



## 🤝 贡献
欢迎提交 Issue 与 Pull Request 来改进项目！
