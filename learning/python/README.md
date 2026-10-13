# Python 学习入口

适合已有 C / C++ 基础的学习者。整理日期：2026-10-13。

## 今天从这里开始

1. 打开 [官方教程：数据结构](https://docs.python.org/zh-cn/3/tutorial/datastructures.html)，读列表、集合、字典和推导式。
2. 做下面的「词频统计」练习，先独立写，再查资料。
3. 在 [学习记录](PROGRESS.md) 写下今天的发现和下次从哪里继续。

每次 30～45 分钟：阅读 10 分钟 → 动手 20 分钟 → 记录 5 分钟。只选一套主线，不必把所有视频刷完。

## 文本与规范

| 资源 | 作用 | 获取方式 |
|---|---|---|
| [Python 官方中文教程](https://docs.python.org/zh-cn/3/tutorial/) | 主线；面向有编程基础的人，核对准确语义 | 在线；[离线下载](https://docs.python.org/zh-cn/3/download.html)，选择对应 Python 版本 |
| [廖雪峰 Python 教程](https://liaoxuefeng.com/books/python/introduction/index.html) | 中文辅助：生成器、装饰器、对象、文件、测试等 | 免费在线阅读 |
| [Python-100-Days 本仓库完整快照](Python-100-Days/README.md) | 按主题练习、查阅示例与应用内容 | 已导入 713 个文件；[原始仓库](https://github.com/jackfrued/Python-100-Days) |
| [PEP 8](https://peps.python.org/pep-0008/) | 命名、缩进、导入与代码风格 | 官方英文原文，按需查阅 |
| [Python 标准库](https://docs.python.org/zh-cn/3/library/) | 查 pathlib、collections、json、csv、argparse 等 | 官方中文参考 |

## 视频与配套练习

| 资源 | 推荐看什么 | 使用说明 |
|---|---|---|
| [CS50P](https://cs50.harvard.edu/python/) | 异常、库、单元测试、文件、正则、面向对象 | 英文主视频；各单元配讲义、代码与作业；免费学习，提交反馈需按官网注册 |
| [CS50P 单元与讲义入口](https://cs50.harvard.edu/python/weeks/0/) | 从单元目录找 Lecture / Notes / Problem Set | 语法部分快速浏览，作业独立完成 |
| [莫烦 Python 视频](https://www.bilibili.com/video/BV1wW411Y7ai/) / [配套图文](https://mofanpy.com/tutorials/python-basic/basic/) | 对不熟悉的知识点补课 | 中文短视频；年代较早，环境和库用法对照当前文档 |
| [黑马 Python 基础课](https://www.bilibili.com/video/BV1qW4y1a7fU/) | 环境安装、编辑器与调试不熟悉时查看 | 2022 年、Python 3.10 课程；已有 C/C++ 基础可跳过大部分基础语法 |

## 学习路线与检查点

- [ ] **容器与语法差异**：官方第 3～5 章；切片、推导式、解包、enumerate、zip。完成词频统计。
- [ ] **对象与函数**：可变性、别名、浅/深拷贝、== 与 is、默认参数、关键字参数、作用域。能解释可变默认参数的问题。
- [ ] **模块、文件与异常**：官方第 6～8 章；with、pathlib、json、csv、异常处理。完成文件清单练习。
- [ ] **对象模型与迭代**：官方第 9 章；类属性/实例属性、特殊方法、迭代器、yield；用廖雪峰补装饰器。
- [ ] **工程习惯**：官方第 12 章；venv、pip、类型注解、PEP 8；跟 CS50P 写测试。
- [ ] **综合练习**：完成命令行通讯录，选做 Python-100-Days 的应用章节。

## 三个可以直接开始的练习

### 1. 词频统计（容器与函数）

输入一段英文文本，忽略大小写和标点，输出出现次数最多的 10 个单词。同频按字母排序。先用 dict，再用 collections.Counter 重写。

验收：`Hello, hello world!` 得到 hello=2、world=1；空输入返回空结果；相同频次排序稳定。把统计逻辑写成函数，并为这些情况写测试。

### 2. 文件清单（pathlib、异常、CSV）

输入一个目录，递归生成文件名、扩展名、大小的 CSV 清单；按扩展名汇总大小。只读取文件，不移动或删除原文件；输出放在扫描目录之外。

验收：空目录、中文文件名、无扩展名文件、无权限目录都有明确处理；默认跳过符号链接；汇总字节数等于明细之和。

### 3. 命令行通讯录（综合）

使用 argparse 支持 add/list/search，以 JSON 保存姓名与联系信息。练习时只使用虚构数据。可先用 dict 实现，再尝试 dataclass。

验收：重启后仍能读取；重名处理明确；损坏 JSON 给出错误且不覆盖原文件；添加和检索有测试。

## 目录与保存方式

- `Python-100-Days/`：上游完整文件快照，建议保持原样；自己的代码另放目录。
- `PROGRESS.md`：学习记录和下次起点，可在 GitHub 点击编辑后保存。
- `UPSTREAM.md`：来源、版本及同步说明。

本页保存在 `python-learning` 分支；桌面「Python 学习入口」指向本页。视频和外部文本保存为原站链接，未下载视频；原站访问仍需网络。公开仓库中的学习记录也会公开，请勿写入密码、私人联系信息等内容。
