## **使用 LlamaIndex 和 DeepSeek 的合同审查工作流**
该仓库包含一个 Jupyter Notebook，展示了如何创建一个代理工作流以审查合同是否符合 GDPR 规定。该工作流使用 LlamaIndex 进行文档解析和检索，以及 DeepSeek 进行自然语言处理任务。
## 概述
该工作流包括以下步骤：
1. **设置**：安装必要的依赖项并设置环境。
2. **文档解析**：使用 LlamaParse 解析合同文档。
3. **条款提取**：从合同中提取相关条款。
4. **指南匹配**：使用向量存储索引将提取的条款与 GDPR 指南进行匹配。
5. **合规性检查**：评估每个条款与匹配指南的合规性。
6. **报告生成**：生成最终的合规性报告，总结发现的问题。
## 先决条件
在运行笔记本之前，请确保您拥有以下条件：
- Python 3.10 或更高版本
- Jupyter Notebook
- LlamaCloud 和 DeepSeek 的 API 密钥
## 工作流详细信息
### 1. 设置
设置包括安装必要的包和为文档解析和检索设置环境。
### 2. 文档解析
使用 LlamaParse 解析合同文档，从中提取结构化数据。
### 3. 条款提取
使用预定义的架构从合同中提取相关条款。该架构包括诸如 `clause_text`、`mentions_data_processing`、`mentions_data_transfer` 等字段。
### 4. 指南匹配
使用向量存储索引将每个提取的条款与相关的 GDPR 指南进行匹配。根据条款文本与指南文本的相似性检索指南。
### 5. 合规性检查
评估每个条款与匹配指南的合规性。评估包括检查条款是否满足指南中指定的要求。
### 6. 报告生成
生成最终的合规性报告，总结每个条款的合规状态，并提供实现完全合规的建议。
## 示例输出
工作流生成一个合规性报告，包括：
- **供应商名称**：供应商的名称（如果可识别）。
- **整体合规状态**：指示合同是否整体合规。
- **总结备注**：实现完全合规的一般总结或建议。
示例输出：
```plaintext
vendor_name='EFG, Inc.' overall_compliant=False summary_notes='The contract contains noncompliant clauses related to subprocessor engagement and data transfer mechanisms...'
```
## 贡献
欢迎贡献！请为任何改进或错误修复打开问题或提交拉取请求。
## 许可证
该项目在 MIT 许可证下授权。有关详细信息，请参阅 [LICENSE](LICENSE) 文件。
## 致谢
- [LlamaIndex](https://github.com/run-llama/llama_index) 用于文档解析和检索。
- [DeepSeek](https://www.deepseek.com/) 用于自然语言处理任务。
---
有关更多详细信息，请参考该仓库中的 [Jupyter Notebook](agentic_contract_review_deepseek.ipynb)。
