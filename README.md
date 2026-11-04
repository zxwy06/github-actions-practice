# GitHub Actions Python 单元测试实验

开源软件设计与分析实验二，使用 GitHub Actions 自动验证加法和乘法函数。

## 本地运行

```powershell
py -3.13 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m pytest -v
```

## 工作流与实验过程

`.github/workflows/ci.yml` 在推送、拉取请求或手动触发时运行两个测试函数，共四个断言。

实验依次保留三个提交：正确实现、将 `add` 故意改成乘法的错误实现、修复加法。
故障提交用于学习如何从 Actions 日志定位断言失败；最终 `main` 分支保留正确实现。

[查看工作流运行记录](https://github.com/zxwy06/github-actions-practice/actions)
