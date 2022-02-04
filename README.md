1. $git log --oneline | grep aefea
	aefead220 Update CHANGELOG.md
   $git log | grep aefea
	commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545
	
2.  git show 85024d3
commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)
3.   git log --pretty=%P -n 1 b8d720
		56cd7859e05c36c06b56d013b55a252d0bb7e158 
		9ea88f22fc6269854151c571162c5bcf958bee2b

4. 	 git log --pretty=oneline v0.12.23...v0.12.24
33ff1c03bb960b332be3af2e333462dde88b279e (tag: v0.12.24) v0.12.24
b14b74c4939dcab573326f4e3ee2a62e23e12f89 [Website] vmc provider links
3f235065b9347a758efadc92295b540ee0a5e26e Update CHANGELOG.md
6ae64e247b332925b872447e9ce869657281c2bf registry: Fix panic when server is unreachable
5c619ca1baf2e21a155fcdb4c264cc9e24a2a353 website: Remove links to the getting started guide's old location
06275647e2b53d97d4f0a19a0fec11f6d69820b5 Update CHANGELOG.md
d5f9411f5108260320064349b757f55c09bc4b80 command: Fix bug when using terraform login on Windows
4b6d06cc5dcb78af637bbb19c198faff37a066ed Update CHANGELOG.md
dd01a35078f040ca984cdd349f18d0b67e486c35 Update CHANGELOG.md
225466bc3e5f35baa5d07197bbc079345b77525e Cleanup after v0.12.23 release

5.  git log -S 'func providerSource' --oneline
5af1e6234 main: Honor explicit provider_installation CLI config when present
8c928e835 main: Consult local directories as potential mirrors of providers

commit 8c928e83589d90a031f811fae52a81be7153e82f


6. $ git grep --heading "globalPluginDirs"
		plugins.go
	$git log -L :globalPluginDirs:plugins.go

		commit 52dbf94834cb970b510f2fba853a5b49ad9b1a46
		commit 41ab0aef7a0fe030e84018973a64135b11abcd70
		commit 66ebff90cdfaa6938f26f908c7ebad8d547fea17

7. git log -S 'synchronizedWriters' --pretty=format:"%h - %an, %ar : %s"
	Author: Martin Atkins <mart@degeneration.co.uk>







#############################################################################################

add new line
add new line 1



действует на все каталоги в которых есть terraform
**/.terraform/*

ИСКЛЮЧАЕТ все файлы содержащие в расширении или имени между .. tfstate
 
*.tfstate
*.tfstate.*

исключаем файлы логов
crash.log
crash.*.log

 Exclude all .tfvars files, which are likely to contain sentitive data, such as
 password, private keys, and other secrets. These should not be part of version
 control as they are data points which are potentially sensitive and subject
 to change depending on the environment.

исключаем все файлы которые хранят конфиденциальную информацию
*.tfvars

 Ignore override files as they are usually used to override resources locally and so
 are not checked in
исключаем локальные файлы
override.tf
override.tf.json
*_override.tf
*_override.tf.json

 Include override files you do wish to add to version control using negated pattern
можем использовать файл с перечнем того что всетаки нужно добавить в киммиты
 !example_override.tf

 Include tfplan files to ignore the plan output of command: terraform plan -out=tfplan
 example: *tfplan*

 Ignore CLI configuration files
игнорируем записи командной строки
.terraformrc
terraform.rc
