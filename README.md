# Cocoapods-
Cocoapods安装指南

1.RVM安装

1.1终端输入： curl -L https://get.rvm.io | bash -s stable

1.2载入RVM环境：source ~/.rvm/scripts/rvm

1.3检查RVM是否安装完成：rvm -v
例如：rvm 1.27.0 (latest) by Wayne E. Seguin <wayneeseguin@gmail.com>, Michal Papis <mpapis@gmail.com> [https://rvm.io/]


2.安装Ruby和RubyGems

2.1列出Ruby版本：rvm list known
例如：
# MRI Rubies
[ruby-]1.8.6[-p420]
[ruby-]1.8.7[-head] # security released on head
[ruby-]1.9.1[-p431]
[ruby-]1.9.2[-p330]
[ruby-]1.9.3[-p551]
[ruby-]2.0.0[-p648]
[ruby-]2.1[.8]
[ruby-]2.2[.4]
[ruby-]2.3[.0]
[ruby-]2.2-head
ruby-head

2.2选择版本进行安装：rvm install 2.3.0
备注：安装过程需要等待一会

2.3检查本机已安装的Ruby：rvm list
例如：rvm rubies
=* ruby-2.3.0 [ x86_64 ]
# => - current
# =* - current && default
#  * - default

2.4卸载RVM:rvm remove x.x.x(x.x.x表示版本号)


3安装Cocoapods

3.1（重要）需要确认 https://cocoapods.org 是否可以访问，如果可以访问忽略步骤3.2

3.2替换sources
3.2.1 查看当前sources：gem sources -l
3.2.2 删除默认sources：gem sources --remove https://rubygems.org/
3.2.3 （上一步操作成功后再执行此步骤）添加新sources：gem sources -a https://ruby.taobao.org/
3.2.4 确认设置是否成功：gem sources -l

3.3 (重要) Mac OS 10.11 以下使用命令： sudo gem install cocoapods

3.4（重要）Mac OS 10.11 以上使用命令：
sudo gem install -n /usr/local/bin cocoapods
和
sudo xcode-select --switch /Applications/Xcode.app

3.5安装：pod setup
(备注：此步骤是漫长的安装等待，本人安装的2.3.0版本，文件大小782M，
检查文件大小命令：cd ~/.cocoapods和du -sh *)

3.6 安装完毕开启愉快的旅程！！！


