# java

一句话立场：Spring Boot 配置用一份 YAML 加环境变量；错误走 BizCode、BizException、全局 Handler 三件套；JDK 跟最新 LTS。

## 条目

### 配置用 YAML，收敛到一份 application.yaml 加环境变量占位，旁支 properties 合并后删除

为什么："帮我把 application.properties 迁移到 application.yaml"；"applications.yml 也迁移一下啊"。迁移后做键值等价比对，改完配置先 clean compile 再启动。

例外：暂无。

来源：2026-09-27、09-28 training-sys（Codex）。

### 错误处理用 BizCode(HttpStatus, code, msg) 枚举、BizException 和全局 Handler，统一返回 code、message、data

为什么：完整模式见 errors。Spring Security 过滤器链里的错误也要走同一格式，提示消息要对用户友好。

例外：暂无。

来源：2026-09-27 training-sys。

### JDK 跟最新 LTS，装正确版本而不是把路径指向另一个版本

为什么："改成 JDK 21 吧"，"在当前环境安装 JDK 21"；另一处"我装个新的 jdk17不行吗 为什么要指向21"。

例外：暂无。

来源：2026-09-26 training-sys；2026-10-21 isdu-app。

### 接口测试用外部语言的 HTTP 脚本跑在隔离的 schema 和端口上，出一份简短 HTML 报告，不写 Java 集成测试

为什么：Codex 记忆里的用户偏好："For API testing, prefer a retained external-language HTTP script against an isolated schema/port with a concise HTML report; do not use Java/Kotlin integration tests for that convention."对应 Claude Code 里的"写一个 Python 脚本, 用于验证大部分接口在调用的时候有按照这次修改的返回进行响应."

例外：暂无。

来源：2026-09-27 training-sys（Codex 转述加亲笔原话）。

## 演变

