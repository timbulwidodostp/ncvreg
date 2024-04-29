# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Regularization paths for MCP and SCAD penalized regression models Use ncvreg With (In) R Software
# Fit an MCP- or SCAD-penalized regression path Use ncvreg With (In) R Software
install.packages("readxl")
install.packages("httr")
install.packages("ncvreg")
library("httr")
library("readxl")
library("ncvreg")
# Import Data Excel Into R From Github Olah Data Semarang (timbulwidodostp)
github_link <- "https://github.com/timbulwidodostp/ncvreg/raw/main/ncvreg/ncvreg.xlsx"
temp_file <- tempfile(fileext = ".xlsx")
req <- GET(github_link, 
# authenticate using GITHUB_PAT
authenticate(Sys.getenv("GITHUB_PAT"), ""),
# write result to disk
write_disk(path = temp_file))
ncvreg <- readxl::read_excel(temp_file)
# Estimate Regularization paths for MCP and SCAD penalized regression models Use ncvreg With (In) R Software
X <- Prostate$X
y <- Prostate$y
fit <- ncvreg(X, y)
summary(fit, lambda=0.05)
# Regularization paths for MCP and SCAD penalized regression models Use ncvreg With (In) R Software
# Fit an MCP- or SCAD-penalized regression path Use ncvreg With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished