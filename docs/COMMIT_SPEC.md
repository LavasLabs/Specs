Git 提交信息规范（Git Commit Message Convention）旨在使提交历史保持清晰和一致，从而使项目维护更为高效。以下是 Git 提交信息的一些规范和最佳实践：

### 格式规范

Git 提交信息通常分为三部分：标题、正文和页脚。基本格式如下：

```
<类型>(<范围>): <主题>

<正文>

<页脚>
```

#### 标题

- **类型（type）**: 描述提交的类别，例如功能、新功能、修复等。
- **范围（scope）**: 可选，描述提交影响的范围，例如文件、模块、功能等。
- **主题（subject）**: 简要描述提交的目的，建议不超过50个字符。

常见的类型有：
- `feat`：新功能
- `fix`：修复 Bug
- `docs`：文档变更
- `style`：代码格式（不影响功能，比如空格、格式化、缺少分号等）
- `refactor`：重构（即不是新增功能，也不是修复 Bug 的代码变动）
- `test`：添加或修改测试
- `chore`：构建过程或辅助工具的变动

**示例**：
```
feat(login): add user login functionality
```

#### 正文

- 详细描述提交的动机、实现方法和可能的影响。
- 每行不超过72个字符，以便于阅读。

**示例**：
```
Implement user login functionality.

The login module now supports user authentication via email and password.
Additional validation and error handling have been added.
```

#### 页脚

- 用于添加任何重要的元数据，如关闭的 issue 编号、审核者信息等。
- 如果是破坏性变更（breaking changes），应在页脚中进行说明。

**示例**：
```
BREAKING CHANGE: the login API endpoint has changed from /api/login to /api/v1/login.

Closes #123
```

### 实践建议

1. **保持简洁**：主题尽量简洁明了，不超过50个字符，正文不超过72个字符。
2. **使用动词时态**：主题使用祈使句，例如“add”、“fix”、“change”等。
3. **分段提交**：一个提交只做一件事，如果有多个改动，分成多个提交。
4. **关联 Issue**：如果提交解决了某个 Issue，使用 `Closes #issue_number` 或 `Fixes #issue_number` 来关联。

通过遵循这些规范，Git 提交信息可以更加清晰、规范，有助于团队协作和项目维护。