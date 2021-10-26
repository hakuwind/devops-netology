# Files to be ignored in terraform due to .gitignore
* local .terraform directories
* .tfstate files
* crash log files (crash.log file specifically)
* all .tfvars files
* specific files: override.tf, override.tf.json, and any files containing any symbol(s) before _override.tf and _override.tf.json
* CLI config files: hidden .terraformrc and terraform.rc
