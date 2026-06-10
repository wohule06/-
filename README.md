# -
构建基于大模型的智能旅行规划 Agent，融合 MCP 工具调用与 RAG 检索增强技术，实现旅行需求理解、景点推荐、天气查询、酒店推荐及多日行程自动生成。系统采用 Agent Workflow 架构，通过高德地图 MCP Server 获取实时数据，并结合 Chroma 向量数据库与 Embedding 检索旅行知识库，实现工具调用与知识检索协同决策。项目引入异步并发、缓存优化及上下文压缩机制，有效降低响应时延并提升复杂任务规划能力。  技术栈： FastAPI、Qwen、MCP、LangGraph、Chroma、Embedding、AsyncIO、Redis
