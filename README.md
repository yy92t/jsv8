# jsv8

#中文说明 | #english

---

# 中文说明

## 项目简介

**jsv8** 是一个围绕 V8 JavaScript 引擎构建的项目，用于提供 JavaScript 执行及相关集成功能。

本仓库包含 jsv8 项目的源代码、示例、文档及相关资源。

## 主要功能

- V8 JavaScript 引擎集成
- 轻量、易于集成
- 支持 JavaScript 代码执行
- 适用于嵌入式 JavaScript 使用场景
- 便于跨平台开发

## 项目结构

```text
jsv8/
├── src/            # 源代码
├── include/        # 头文件
├── examples/       # 示例程序
├── tests/          # 测试
├── docs/           # 文档
├── CMakeLists.txt  # CMake 配置
├── LICENSE
└── README.md
```

> 注意：实际目录结构可能根据 jsv8 的版本有所不同。

## 环境要求

在编译 jsv8 前，请确保开发环境已经安装所需的工具和依赖。

通常可能需要：

- Git
- C/C++ 编译器
- CMake
- V8
- 对应平台的构建工具

具体依赖请根据当前版本及目标平台进行配置。

## 获取项目

从 Gitee 克隆仓库：

```bash
git clone https://gitee.com/YOUR_USERNAME/jsv8.git
cd jsv8
```

请将 `YOUR_USERNAME` 替换为实际的 Gitee 用户名或组织名称。

## 编译

如果项目使用 CMake，可以通过以下方式进行标准构建：

```bash
mkdir build
cd build

cmake ..
cmake --build .
```

实际编译选项可能会根据操作系统、编译器及 V8 配置有所不同。

## 使用方法

项目编译完成后，可将 jsv8 集成至你的应用程序，并配置相应的 V8 库及头文件路径。

示例：

```cpp
#include <iostream>

// 在此处引入相应的 jsv8 头文件

int main()
{
    std::cout << "jsv8 example" << std::endl;
    return 0;
}
```

更多使用方式请参考 `examples/` 目录。

## 开发

建议开发新功能时创建独立分支：

```bash
git checkout -b feature/my-feature
```

完成修改后：

```bash
git add .
git commit -m "Add my feature"
git push origin feature/my-feature
```

随后可在 Gitee 中创建 Pull Request。

## 贡献

欢迎参与 jsv8 项目的开发。

1. Fork 本仓库
2. 创建新的功能分支
3. 完成代码修改
4. 提交修改
5. Push 至自己的 Fork 仓库
6. 创建 Pull Request

提交 Pull Request 时，请尽量说明修改目的及主要变化。

## 问题反馈

如发现 Bug 或有新的功能建议，请通过 Gitee Issue 进行反馈。

报告问题时，建议提供以下信息：

- 操作系统
- 编译器版本
- V8 版本
- 构建配置
- 错误信息
- 问题复现步骤

以上信息可以帮助开发者更快定位问题。

## 许可证

本项目的授权方式请参阅 `LICENSE` 文件。

## 致谢

感谢 V8 项目以及所有为 jsv8 提供代码、测试、文档和建议的贡献者。

---

# English

## Introduction

**jsv8** is a project built around the V8 JavaScript engine, providing JavaScript execution and related integration functionality.

This repository contains the source code, examples, documentation and supporting resources for the jsv8 project.

## Features

- V8 JavaScript engine integration
- Lightweight and easy to integrate
- JavaScript execution support
- Suitable for embedded JavaScript use cases
- Cross-platform development friendly

## Repository Structure

```text
jsv8/
├── src/            # Source code
├── include/        # Header files
├── examples/       # Example applications
├── tests/          # Tests
├── docs/           # Documentation
├── CMakeLists.txt  # CMake configuration
├── LICENSE
└── README.md
```

> Note: The actual directory structure may differ depending on the version of jsv8.

## Requirements

Before building jsv8, make sure the required development tools and dependencies are installed.

Typical requirements may include:

- Git
- C/C++ compiler
- CMake
- V8
- Platform-specific build tools

Exact requirements depend on the version and target platform.

## Getting Started

Clone the repository from Gitee:

```bash
git clone https://gitee.com/YOUR_USERNAME/jsv8.git
cd jsv8
```

Replace `YOUR_USERNAME` with the appropriate Gitee username or organisation name.

## Building

If the project uses CMake, a typical build can be performed with:

```bash
mkdir build
cd build

cmake ..
cmake --build .
```

Build options may vary depending on the operating system, compiler and V8 configuration.

## Usage

After building the project, jsv8 can be integrated into your application by configuring the appropriate V8 libraries and include paths.

Example:

```cpp
#include <iostream>

// Include the appropriate jsv8 headers here.

int main()
{
    std::cout << "jsv8 example" << std::endl;
    return 0;
}
```

See the `examples/` directory for additional usage examples.

## Development

Create a dedicated branch when developing a new feature:

```bash
git checkout -b feature/my-feature
```

After making your changes:

```bash
git add .
git commit -m "Add my feature"
git push origin feature/my-feature
```

You can then create a Pull Request on Gitee.

## Contributing

Contributions to jsv8 are welcome.

1. Fork this repository
2. Create a feature branch
3. Make your changes
4. Commit your changes
5. Push the branch to your fork
6. Submit a Pull Request

When submitting a Pull Request, please provide a clear description of the purpose and main changes.

## Reporting Issues

If you encounter a bug or have a feature request, please create an Issue on Gitee.

When reporting a problem, it is helpful to include:

- Operating system
- Compiler version
- V8 version
- Build configuration
- Error messages
- Steps to reproduce the problem

This information can help developers diagnose the problem more efficiently.

## Licence

Please refer to the `LICENSE` file for the licensing terms of this project.

## Acknowledgements

Thanks to the V8 project and everyone who has contributed code, testing, documentation and suggestions to jsv8.


# Google Apps Script: Flexible Pivot Table Builder

This script creates pivot tables in Google Sheets using the Advanced Sheets API. It accepts flexible column references (header names, letters, or numeric indices) and can be pointed at any tabular data range.

## Prerequisites

1. Open Extensions > Apps Script on your Google Sheet.
2. Add this project as a bound script.
3. Enable Advanced Google Services:
   - In Apps Script: Services (left sidebar) > + > Google Sheets API > Add.
   - Ensure the Google Sheets API is also enabled in your Cloud project if prompted.
4. Paste the `PivotTableBuilder.gs` content into the editor and save.

## Quick Start

1. Prepare a sheet named `Data` with a header row (e.g., columns like `ID, Region, Status, Amount`).
2. Create a blank sheet (or let the script create it) named `Pivot`.
3. Run `createExamplePivot()` from the script editor or use the custom menu "Pivot Tools > Create Example Pivot".

The example:
- Rows: Region
- Columns: Status
- Values: Sum of Amount, Count of ID
- Output to sheet "Pivot" at A1.

## Build Your Own Pivot

Use `createPivotTable(config)` with a configuration like:

```javascript
createPivotTable({
  sourceSheet: 'RawData',
  sourceRangeA1: 'A1:Z', // must include header row
  destinationSheet: 'MyPivot',
  anchorCellA1: 'B2', // optional, default A1

  rows: [
    { column: 'Product', showTotals: true, sortOrder: 'ASC' }
  ],
  columns: [
    { column: 'Quarter', showTotals: true, sortOrder: 'DESC' }
  ],
  values: [
    { column: 'Revenue', summarizeFunction: 'SUM', name: 'Revenue (Sum)' },
    { column: 'OrderID', summarizeFunction: 'COUNT', name: 'Orders' }
  ]
});
```

### Column References

For `rows`, `columns`, and `values`, the `column` field accepts:
- Header name: `'Revenue'`
- Column letter: `'C'` or `'AA'`
- 1-based column index: `3`

The reference must point within `sourceRangeA1`.

### Supported summarizeFunction values

- SUM, COUNTA, COUNT, MAX, MIN, AVERAGE, MEDIAN, PRODUCT, STDEV, STDEVP, VAR, VARP, CUSTOM

If you use `CUSTOM`, provide a `formula` in the value spec.

### Grouping and Sorting

- `sortOrder`: `'ASC'` or `'DESC'`
- `showTotals`: defaults to `true`
- You can pass a `groupRule` on a row/column group if you need date or histogram bucketing (advanced Sheets API object).

## Notes

- This script uses the Sheets Advanced Service via `Sheets.Spreadsheets.batchUpdate` with `updateCells` and a `pivotTable` cell at the anchor position.
- Filters and more advanced pivot configurations can be added by extending the request object.
- The pivot table is created at the specified anchor cell on the destination sheet. You can create multiple pivots by selecting different anchors.

## Troubleshooting

- ReferenceError: "Sheets is not defined"
  - Ensure you enabled the Advanced Google Sheets API service in the Apps Script editor (Services > + > Google Sheets API).

- Column reference outside range
  - The column reference must be within the `sourceRangeA1`. Expand the range or adjust the column reference.

- Headers not found
  - Make sure your `sourceRangeA1` includes the header row and that header names match exactly (case-sensitive).
