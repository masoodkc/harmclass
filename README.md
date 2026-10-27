# harmclass

**把有害内容按类别归并并统计分布。**

`harmclass` —— 按预先定义的类别归档文本，统计各类占比与典型样本

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`harmclass.py` 拷走就能用
- 不联网、不写文件

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install masoodkc-harmclass
```

装完直接用命令名调用：

```bash
harmclass --help
```

也可以不用安装，直接把 `harmclass.py` 拷走用——它只依赖标准库。

## 为什么需要它

分类是穷举定义好的类别，不做开放式判断

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到 有害内容分类 领域的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python harmclass.py --file input.txt
python harmclass.py --text "示例内容"
python harmclass.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 分组靠标签与关键词相似度，分错组时不保证可解释。
- 不评估分组质量。

## 跑测试

```bash
python test_harmclass.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/masoodkc/harmclass>

---

## 关于作者

masoodkc 做有害内容分类相关的问题。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://masoodkc.github.io>
- 仓库：<https://github.com/masoodkc/harmclass>

## 许可

MIT，见 [LICENSE](LICENSE)。
