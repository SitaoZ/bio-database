

1. 设置NCBI API Key（提高速率限制）
默认情况下，ncbi_snp_query()的请求限制是每秒最多1次查询，且不允许并发请求。对于大批量SNP，这会导致极慢的查询速度。

解决方法：申请NCBI API Key，将速率提升到每秒10次请求
```bash
# 步骤1：在NCBI网站申请API Key
# 登录 https://www.ncbi.nlm.nih.gov/account/settings/
# 在"API Key Management"部分创建API Key

# 步骤2：在R中设置环境变量
# 方法A：临时设置（仅当前会话有效）
Sys.setenv(ENTREZ_KEY = "你的实际API密钥")

# 方法B：永久设置（推荐）
usethis::edit_r_environ()  # 打开.Renviron文件
# 添加一行：ENTREZ_KEY='你的实际API密钥'
# 保存后重启R
```

[refer1](https://mrcieu.r-universe.dev/rsnps/doc/manual.html#download_users)  
[refer2](https://docs.ropensci.org/rsnps/reference/rsnps-package.html)
