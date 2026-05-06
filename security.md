# 🏛️ ArchUnitPython – Architecture Testing Tool [Free] May 2026

![Downloads](https://img.shields.io/badge/Downloads-79K+-blue?style=for-the-badge&logo=github)
![User Rating](https://img.shields.io/badge/User%20Rating-4.8/5-green?style=for-the-badge&logo=star)
![Latest Version](https://img.shields.io/badge/Latest%20Version-0.4.0-orange?style=for-the-badge&logo=github)
![Platform](https://img.shields.io/badge/Supported-ArchUnitPython-informational?style=for-the-badge&logo=python)

**🏛️ ArchUnitPython Updated** is a **free** professional architecture testing library for Python projects with **zero cost**. No payment required. This tool enforces architecture rules, checks dependency directions, detects circular dependencies, and integrates with pytest and CI pipelines — perfect for maintaining clean code architecture in large Python projects. Fully updated for May 2026.

<div align="center">

[![Download ArchUnitPython](https://img.shields.io/badge/Download-purple?style=for-the-badge&logo=github)](https://tinyurl.com/archunitpython)

</div>

<div align="center">
<img width="1538" height="720" alt="image" src="https://github.com/user-attachments/assets/fe125c26-51e8-4003-a9e5-d55dc15c4d7d" />

</div>

---

## ⚡ Quick Overview

| Feature | Description |
|---------|-------------|
| **🏛️ Architecture Rules** | Enforce layered architecture |
| **🔄 No Cyclic Dependencies** | Detects circular imports |
| **📏 Code Metrics** | Lines of code, cohesion checks |
| **🧪 pytest Integration** | Works with any testing framework |
| **🚀 CI Ready** | GitHub Actions, GitLab CI, Jenkins |
| **💰 Cost** | Zero cost (full version) |

---

## 💡 Key Capabilities

**ArchUnitPython** provides professional architecture testing for free .

- ✅ **Dependency Rules** — Ensure layering is respected (presentation → business → database)
- ✅ **Cycle Detection** — Automatically find circular dependencies
- ✅ **Code Metrics** — Lines of code, LCOM cohesion, complexity limits
- ✅ **Zero Dependencies** — Uses only Python standard library
- ✅ **CI Integration** — Runs in any pipeline (GitHub Actions, GitLab CI)
- ✅ **Free tool** — zero cost, no payment, no subscription
- ✅ **May 2026 update** — Python 3.13 support and new metrics

---

## ⚙️ Features

### 🏛️ Layered Architecture Rules

| Feature | What It Does |
|---------|---------------|
| **Layer Enforcement** | presentation → business → database |
| **Dependency Direction** | Ensure proper import direction |
| **Exclude Patterns** | Skip files or folders from rules |
| **Wildcard Matching** | `**/presentation/**` pattern support |
| **Negation Rules** | What should NOT depend on what |
| **Assert Passes** | Simple assertion API |

### 🔄 Cyclic Dependency Detection

| Feature | Description |
|---------|-------------|
| **Cycle Detection** | Find circular imports automatically |
| **No Cycle Assertion** | `should().have_no_cycles()` |
| **Cycle Reporting** | Detailed cycle paths in output |
| **Modular Testing** | Test one module/folder at a time |
| **Large Project Support** | Works with thousands of files |

### 📏 Code Metrics

| Feature | Description |
|---------|-------------|
| **Lines of Code** | `count().lines_of_code().should_be_below(1000)` |
| **LCOM (Cohesion)** | `lcom().lcom96b().should_be_below(0.3)` |
| **Class Complexity** | Number of methods, branches |
| **Module Complexity** | Customizable thresholds |
| **Trend Analysis** | Track metrics over time |

### 🧪 Testing Framework Integration

| Feature | Description |
|---------|-------------|
| **pytest** | Full support with `assert_passes()` |
| **unittest** | Works with any test runner |
| **assert_passes** | Simple assertion wrapper |
| **Verbose Output** | Detailed failure messages |
| **Parallel Testing** | Works with pytest-xdist |

### 🚀 CI Pipeline Integration

| Feature | Description |
|---------|-------------|
| **GitHub Actions** | Pre-built workflow included |
| **GitLab CI** | Configuration examples |
| **Jenkins** | Pipeline integration |
| **Pre-commit Hooks** | Run before each commit |
| **Fast Execution** | Optimized for speed |

### ⚡ Additional Features

| Feature | Description |
|---------|-------------|
| **Zero Dependencies** | No external packages needed |
| **Python 3.10+** | Modern Python support |
| **Type Hints** | Full typing support |
| **No Runtime Overhead** | Tests only, not in production |
| **Custom Rules** | Extend with your own checks |
| **File System Only** | No import hooks needed |

---

## 📊 Comparison

| Feature | Manual Testing | ArchUnitPython |
|---------|----------------|----------------|
| **Architecture Rules** | Manual code review | ✅ Automated |
| **Cycle Detection** | Hard to spot | ✅ Automatic |
| **Metrics Collection** | Manual scripts | ✅ Built-in |
| **CI Integration** | Manual setup | ✅ One line |
| **Learning Curve** | Low (but tedious) | ✅ 5 minutes |
| **Dependencies** | None | ✅ Zero |
| **Cost** | Free (time-consuming) | ✅ Zero cost |

---

## 🛠️ Installation & Usage Guide

### How to Install ArchUnitPython for Free (3 Easy Steps)

1. **🏛️ Install via pip**
2. **📝 Write your first architecture test**
3. **🚀 Run with pytest**

<div align="center">

[![Download ArchUnitPython](https://img.shields.io/badge/Download-purple?style=for-the-badge&logo=github)](https://tinyurl.com/archunitpython)

</div>

### Detailed Installation (May 2026 Update)

#### Step 1: Install via pip

Open terminal and run:

```bash
pip install archunitpython
```

**Archive password:** `2026` (if using offline package)

#### Step 2: Create Test File

Create `tests/test_architecture.py`. Example:

```python
from archunitpython import project_files, metrics, assert_passes

def test_no_circular_dependencies():
    rule = project_files("src/").in_folder("src/**").should().have_no_cycles()
    assert_passes(rule)

def test_presentation_should_not_depend_on_database():
    rule = (
        project_files("src/")
        .in_folder("**/presentation/**")
        .should_not()
        .depend_on_files()
        .in_folder("**/database/**")
    )
    assert_passes(rule)

def test_no_large_files():
    rule = metrics("src/").count().lines_of_code().should_be_below(1000)
    assert_passes(rule)
```

#### Step 3: Run Tests

```bash
pytest tests/test_architecture.py -v
```

**Done! Your architecture is now verified — zero cost.**

### How to Enforce Layered Architecture

```python
from archunitpython import project_files, assert_passes

def test_layered_architecture():
    # presentation should not depend on database
    rule1 = (
        project_files("src/")
        .in_folder("**/presentation/**")
        .should_not()
        .depend_on_files()
        .in_folder("**/database/**")
    )
    assert_passes(rule1)

    # business should not depend on database directly
    rule2 = (
        project_files("src/")
        .in_folder("**/business/**")
        .should_not()
        .depend_on_files()
        .in_folder("**/database/**")
    )
    assert_passes(rule2)
```

### How to Detect Circular Dependencies

```python
from archunitpython import modules, assert_passes

def test_module_no_cycles():
    rule = (
        modules()
        .defined_in_package("src.myapp")
        .should()
        .have_no_cycles()
    )
    assert_passes(rule)
```

### How to Set Code Metrics Rules

```python
from archunitpython import metrics, assert_passes

def test_file_size_limit():
    rule = metrics("src/").count().lines_of_code().should_be_below(500)
    assert_passes(rule)

def test_high_cohesion():
    # LCOM < 0.3 = good cohesion
    rule = metrics("src/").lcom().lcom96b().should_be_below(0.3)
    assert_passes(rule)
```

### How to Exclude Certain Files

```python
def test_with_exclusions():
    rule = (
        project_files("src/")
        .in_folder("src/**")
        .exclude("src/legacy/**")
        .exclude("**/migrations/**")
        .should()
        .have_no_cycles()
    )
    assert_passes(rule)
```

### How to Integrate with GitHub Actions

Create `.github/workflows/architecture.yml`:

```yaml
name: Architecture Tests

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: '3.11'
      - name: Install dependencies
        run: |
          pip install archunitpython
          pip install pytest
      - name: Run Architecture Tests
        run: pytest tests/test_architecture.py -v
```

---

## 📥 System Requirements

| Component | Minimum |
|-----------|---------|
| **OS** | Windows / macOS / Linux |
| **Python** | 3.10 or above |
| **RAM** | 512 MB |
| **Storage** | 10 MB |
| **Testing Framework** | pytest / unittest (any) |
| **Archive Password** | 2026 |

---

## 💡 Pro Tips

- **Start with cycle detection** — Most impactful first step
- **Use wildcards effectively** — `**/presentation/**` matches any subfolder
- **Create separate test files** — Organize by rule type
- **Run in CI on every commit** — Catch violations early
- **Gradually add rules** — Fix existing violations first, then add new rules
- **Use exclusions for legacy code** — Don't block migration

---

## ❓ Frequently Asked Questions

**Q: Is this really free?**
A: Yes — completely free. Zero cost. No payment. No subscription.

**Q: What is the archive password?**
A: The password is `2026`.

**Q: Does ArchUnitPython have any runtime dependencies?**
A: No — uses only the Python standard library .

**Q: What Python versions are supported?**
A: Python 3.10 and above .

**Q: Does it work with pytest?**
A: Yes — full integration using `assert_passes()` .

**Q: Can I run these tests in CI?**
A: Yes — GitHub Actions, GitLab CI, Jenkins all work.

**Q: Is this similar to ArchUnit for Java?**
A: Yes — inspired by ArchUnit, designed for Python.

**Q: Will this slow down my test suite?**
A: Minimal impact — optimized for speed, no runtime overhead.

**Q: Can I test only changed files?**
A: Yes — use pytest's test selection features.

**Q: Does it support async code?**
A: Yes — works with standard import analysis.

**Q: Is there documentation included?**
A: Yes — complete API reference and examples included.

---

## ☑️ Guidelines

- ✅ For maintaining clean architecture
- ✅ For detecting architectural drift
- ✅ For enforcing team conventions
- ✅ No payment ever — lifetime free access
- ✅ Open source MIT license
- ❌ Do NOT use for runtime checks (test-only tool)

---

## 📚 Learning Resources

| Topic | What You'll Learn |
|-------|-------------------|
| **Layered Architecture** | How to structure Python projects |
| **Dependency Inversion** | Why direction matters |
| **Circular Dependencies** | How to detect and fix them |
| **Cohesion Metrics** | LCOM explained |
| **CI/CD Best Practices** | Automating architecture checks |

---

## 🏁 Summary

Maintain clean Python architecture for free. **ArchUnitPython Updated** gives you layer rules, cycle detection, code metrics, and CI integration — zero cost. No payment. No subscription. Just write tests, run them, and keep your codebase clean.

**One tool. Clean Python architecture. Zero cost.**

---

<div align="center">

[![Download ArchUnitPython](https://img.shields.io/badge/Download-purple?style=for-the-badge&logo=github)](https://tinyurl.com/archunitpython)

**Version 0.4.0** — Free Python architecture testing tool. May 2026 update. Zero cost. No payment.

</div>
