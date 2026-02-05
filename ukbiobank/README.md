## UKBiobank 使用

### dx

- login
```bash
dx login
```

### JupyterLab storage back to your project storage using dx upload

- upload to project root directory
```bash
dx upload "olink_i0_npx_wide.csv"
```

- uplode fasta to ref directory in RPA 
```bash
dx upload  GRCh38_full_analysis_set_plus_decoy_hla.fa --path "/ref/"
dx upload  GRCh38_full_analysis_set_plus_decoy_hla.fa.fai --path "/ref/"
dx upload  GRCh38_full_analysis_set_plus_decoy_hla.dict --path "/ref/"
```
