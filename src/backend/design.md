# 设计

perfumer 的后端由 Rust 编写，并且使用了如下技术栈

- [Rocket](https://rocket.rs)
- [SeaORM](https://www.sea-ql.org/SeaORM/)
- PostgreSQL
  - with `VectorChord`
  - with `uuidv7`
- Redis
- [RustFS](https://rustfs.com/)
  - 用于替代 Minio，提供 S3 服务

## 后端的职责

后端提供如下能力：

- 数据储存
  - 聊天记录
  - 聊天记录的嵌入信息
  - 对于消息的评论
  - 对于消息的同意与否定
- 数据查找
  - 相似数据
  - 模糊查找

后端不提供如下能力：

- 记录去重
- 处理结构
