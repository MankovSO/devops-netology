add new line
add new line 1

задание №3.3 пункт 7 добавил строчку

действует на все каталоги в которых есть terraform
**/.terraform/*

ИСКЛЮЧАЕТ все файлы содержащие в расширении или имени между .. tfstate
 
*.tfstate
*.tfstate.*

исключаем файлы логов
crash.log
crash.*.log

# Exclude all .tfvars files, which are likely to contain sentitive data, such as
# password, private keys, and other secrets. These should not be part of version
# control as they are data points which are potentially sensitive and subject
# to change depending on the environment.
#
исключаем все файлы которые хранят конфиденциальную информацию
*.tfvars

# Ignore override files as they are usually used to override resources locally and so
# are not checked in
исключаем локальные файлы
override.tf
override.tf.json
*_override.tf
*_override.tf.json

# Include override files you do wish to add to version control using negated pattern
можем использовать файл с перечнем того что всетаки нужно добавить в киммиты
# !example_override.tf

# Include tfplan files to ignore the plan output of command: terraform plan -out=tfplan
# example: *tfplan*

# Ignore CLI configuration files
игнорируем записи командной строки
.terraformrc
terraform.rc
