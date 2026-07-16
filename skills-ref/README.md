# skills-ref

Agent Skills 参考库。

> [!IMPORTANT]
> 本库仅供演示之用。不适用于生产环境。

## 安装

### macOS / Linux

使用 pip：

```bash
python -m venv .venv
source .venv/bin/activate
pip install -e .
```

或使用 [uv](https://docs.astral.sh/uv/)：

```bash
uv sync
source .venv/bin/activate
```

### Windows

使用 pip (PowerShell)：

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -e .
```

使用 pip (命令提示符)：

```cmd
python -m venv .venv
.venv\Scripts\activate.bat
pip install -e .
```

或使用 [uv](https://docs.astral.sh/uv/)：

```powershell
uv sync
.venv\Scripts\Activate.ps1
```

安装完成后，`skills-ref` 可执行文件将在你的 `PATH` 上可用（在激活的虚拟环境中）。

## 使用

### CLI

```bash
# 验证技能
skills-ref validate path/to/skill

# 读取技能属性（输出 JSON）
skills-ref read-properties path/to/skill

# 为智能体提示词生成 <available_skills> XML
skills-ref to-prompt path/to/skill-a path/to/skill-b
```

### Python API

```python
from pathlib import Path
from skills_ref import validate, read_properties, to_prompt

# 验证技能目录
problems = validate(Path("my-skill"))
if problems:
    print("验证错误：", problems)

# 读取技能属性
props = read_properties(Path("my-skill"))
print(f"技能：{props.name} - {props.description}")

# 为可用技能生成提示词
prompt = to_prompt([Path("skill-a"), Path("skill-b")])
print(prompt)
```

## 智能体提示词集成

使用 `to-prompt` 为你的智能体系统提示词生成建议的 `<available_skills>` XML 块。此格式推荐用于 Anthropic 的模型，但 Skill 客户端可以根据所用模型选择不同的格式。

```xml
<available_skills>
<skill>
<name>
my-skill
</name>
<description>
此技能的功能以及何时使用它
</description>
<location>
/path/to/my-skill/SKILL.md
</location>
</skill>
</available_skills>
```

`<location>` 元素告诉智能体在哪里找到完整的技能指令。

## 许可证

Apache 2.0
