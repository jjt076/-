# 高考志愿填报助手

## 项目简介

**高考志愿咨询助手** 是一个基于 Java、Spring Boot 和 [LangChain4j](https://github.com/langchain4j/langchain4j) 的智能咨询系统，专为高考考生和家长设计。系统集成了院校与专业信息查询、智能问答、预约咨询等功能，借助 LangChain4j 强大的大语言模型（LLM）能力，实现自然流畅的对话式志愿填报辅助。

## 主要功能

- **智能问答与对话**  
  基于 LangChain4j，支持自然语言提问，智能解答高考志愿相关政策、流程、专业选择等问题。

- **院校与专业信息查询**  
  提供全国高校及热门专业的详细资料，支持关键词检索，帮助考生全面了解目标院校和专业。

- **预约咨询服务**  
  支持用户预约一对一咨询，获取个性化志愿填报建议。

- **聊天记录存储**  
  基于 Redis 实现聊天记录的存储与管理，方便用户随时回顾历史咨询内容。

## 技术栈

- **后端**：Java 17、Spring Boot、LangChain4j
- **数据库**：MySQL（可扩展）、Redis
- **前端**：静态 HTML（可扩展为 Vue/React 等现代前端框架）
- **构建工具**：Maven
- **测试**：JUnit

## 目录结构

```
src/
  main/
    java/
      com.itheima.consultant/
        aiservice/         # 智能服务逻辑（集成 LangChain4j）
        controller/        # 控制器，接口入口
        service/           # 业务服务层
        mapper/            # 数据访问层
        repository/        # 存储实现
        pojo/              # 实体类
        config/            # 配置类
        tools/             # 工具类
    resources/
      content/             # 院校与专业资料PDF
      static/              # 前端静态页面
      application.yml      # 配置文件
  test/
    java/
      ...                  # 测试代码
```

## 快速开始

1. **克隆项目到本地**
   ```bash
   git clone https://github.com/yourname/consultant.git
   ```

2. **配置数据库、Redis 及 LangChain4j 相关参数**  
   修改 `src/main/resources/application.yml` 文件，填写数据库、Redis 及 LangChain4j 的相关配置。

3. **使用 Maven 构建并运行项目**
   ```bash
   mvn spring-boot:run
   ```

4. **访问系统首页**  
   在浏览器中打开 [http://localhost:8080/](http://localhost:8080/)
