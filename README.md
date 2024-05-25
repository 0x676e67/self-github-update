# self-github-update 使用文档

`self-github-update` 是一个用于 Rust 可执行文件自我更新的库，特别适用于 Github 上的项目。以下是一些可用的特性和它们的描述：

## 特性

### 默认特性

- `default`: 默认启用 `client` 特性。

### 客户端特性

- `client`: 启用 `reqwest` 库，用于发送网络请求。

- `client-impersonate`: 启用 `reqwest-impersonate` 库，用于模拟网络请求。

### 压缩和解压特性

- `archive-zip`: 启用 `zip` 和 `zipsign-api` 库，用于处理 ZIP 压缩文件。

- `compression-zip-bzip2`: 启用 `archive-zip` 和 `zip/bzip2` 库，用于处理使用 BZIP2 算法压缩的 ZIP 文件。

- `compression-zip-deflate`: 启用 `archive-zip` 和 `zip/deflate` 库，用于处理使用 DEFLATE 算法压缩的 ZIP 文件。

- `archive-tar`: 启用 `tar` 和 `zipsign-api` 库，用于处理 TAR 压缩文件。

- `compression-flate2`: 启用 `archive-tar`、`flate2` 和 `either` 库，用于处理使用 FLATE2 算法压缩的 TAR 文件。

### 签名特性

- `signatures`: 启用 `zipsign-api` 库，用于处理压缩文件的签名验证。

## 如何使用

在你的 `Cargo.toml` 文件中，添加 `self-github-update` 作为依赖，并选择你需要的特性：

```toml
[dependencies]
self-github-update = { version = "0.39.0", features = ["archive-zip"] }
```

### 例子

`https://github.com/jaemk/self_update`
