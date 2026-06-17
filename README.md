# 无线通信技术期末项目模板

本仓库是无线通信技术课程期末项目的 GitHub Classroom 模板仓库。

项目目标：根据 `PRD.docx` 的要求，使用 AI 辅助编程实现一个无线通信基带仿真系统，将 `Test.txt` 的 UTF-8 文本内容通过发送端、无线信道和接收端处理后恢复为 `results/received.txt`。

## 必须提交的文件

学生最终项目至少应包含：

```text
DESIGN.md
TEST_PLAN.md
MOCK_TEST_REPORT.md
AI_LOG.md
main.py
src/
tests/
results/
```

## 统一运行命令

项目必须支持以下命令：

```bash
python main.py --input Test.txt --output results/received.txt --snr 12 --seed 2026 --mod qpsk --channel awgn
```

运行后应生成：

```text
results/received.txt
results/metrics.json
```

并至少生成以下图表中的两项：

```text
results/constellation.png
results/ber_curve.png
results/sync_peak.png
```

## 本地公开测试

安装依赖：

```bash
pip install -r requirements.txt
```

运行公开测试：

```bash
pytest public_tests -q
```

这些公开测试只覆盖部分基础验收要求。教师最终评分还会使用隐藏验证集。

## AI 使用要求

允许并鼓励使用 AI 辅助编程。建议使用 Claude Code 或 Codex，并加装或启用 Superpowers skills。

必须保留 `AI_LOG.md`，记录关键 prompt、AI 生成内容、人工修改内容、测试失败修复过程和最终采纳理由。

即使程序运行成功，学生仍需能够解释每个模块的通信原理、关键参数、代码逻辑和实验结果。
