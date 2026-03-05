## OpenGWAS
OpenGWAS 的目标是将分散的 GWAS 汇总数据源与一系列能够从这些数据中挖掘价值的分析工具整合在一起。构建这种一致性极大地扩展了表型组因果推断的范围，同时也提高了其可靠性。

## 工具
- TwoSampleMR
- ieugwasr

## 使用
**从2024年5月1日起，访问OpenGWAS API需要提供JWT令牌（Token）进行身份验证**，

以下是具体的解决步骤：

- 1. 核心原因：API认证政策变更  
你收到的 `401` 错误（未授权）和提示信息明确指出，OpenGWAS API 在2024年5月之后更改了访问规则。现在调用 `extract_instruments()` 等函数时，必须提供一个有效的身份验证令牌，不能再匿名访问。

- 2. 如何获取你的JWT令牌  
你需要按照错误信息提示的步骤，前往 `https://api.opengwas.io/` 注册并获取令牌：  
(1).  **访问注册页面**：在浏览器中打开 `https://api.opengwas.io/`。  
(2).  **选择登录方式**：根据你的情况选择。通常使用 **GitHub账号** 登录最便捷（它会接受任何由GitHub验证的邮箱），或者选择学校/工作邮箱进行注册。  
(3).  **获取令牌**：登录成功后，你的账户页面会提供一个专属的 **JWT令牌（Token）**。它通常是一长串字符。请复制并安全保存它。  

 - 3. 在R代码中使用令牌  
获取令牌后，有两种方式在 `TwoSampleMR` 或 `ieugwasr` 函数中使用它：

**方法一：直接在函数中指定（推荐用于临时测试）**
```r
bmi_exp <- extract_instruments(
    outcomes = 'ieu-a-835', 
    clump = TRUE, 
    access_token = "你的JWT令牌"  # 将引号内的内容替换为你的实际令牌
)
```

**方法二：设置环境变量（推荐用于日常使用，避免每次粘贴）**
在R会话开始时，设置环境变量，这样后续所有相关函数都会自动使用：
```r
Sys.setenv(OPENGWAS_JWT = "你的JWT令牌")
# 之后调用函数时无需再指定 access_token
bmi_exp <- extract_instruments(outcomes = 'ieu-a-835', clump = TRUE)
```

- 4. 额外注意事项  
*   **令牌安全**：请妥善保管你的JWT令牌，不要将其公开分享（如在共享代码或公开帖子中）。  
*   **更新R包**：确保你的 `TwoSampleMR` 和 `ieugwasr` 包是最新版本，以便它们能正确支持新的认证方式。可以使用 `update.packages(c("TwoSampleMR", "ieugwasr"))` 进行更新。  
*   **配额与费用**：API的使用可能有请求频率或数据量的限制（配额），具体细节需查看 `https://api.opengwas.io/` 网站上的 "Allowance and cost" 部分。  

总结来说，你只需要完成一次注册并获取令牌，然后在R代码中加入 `access_token` 参数或设置环境变量，问题即可解决。

如果你在注册或获取令牌的过程中遇到任何问题，可以随时追问。
