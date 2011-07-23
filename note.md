##coding style

    插入模式下ctrl_t为缩进

              ctrl_d往前缩进
    
    在.vimrc中设置 

            set expandtab  "将tab展开成空格


            set tabstop=4 "让tab占4个空格"
            
            
            set shiftwidth=4 "shift加大写v加’>‘占4个空格
            
            
            set autoindent "vim下设置自动缩进"

            set dictionary=/usr/share/dict/words "使用法发 ：在vim中用ctrl—x—k三
            
            
            个键即可查询字典里的内容"


    4个空格为普遍缩进格式

##删除网页上的文件

    git rm 111
   
    git commit -a 

    git push

##配置文件

     .vimrc
  
     .bashrc

     .gitconfig

##snipmate 插件的安装


     下载snipMate.zip压缩包
      
     unzip snipMate.zip -d ~/.vim解压

     步骤：cd .vim

           cd snippets

           ls
  
           vim c.snippets 进入界面
   
          eg：##dog

             dog

            敲tab键再输入dog dog dog 

           下次vim中敲dog则显示dog  dog dog








## git 
   
	   git commit -a -m ""
  
           引号里如何输入多行？

           git commit -a 回车即可显示输入多行信息


##再次新建工程
 
      进入dashboard 创建工程名


      git init(初始化)


      git add hello.c（跟踪hello.c） 
   
 
      git commit -a -m "o"（创建版本）

   
      git  remote add origin git@github.com:wangpan/wangpan-project.git


   
      git push （-u） origin master  



##编译器gcc

    1  gcc -Wall b.c （wall警告所有)
  
    2  vim中先
     
        :w 保存
        
        ：sh 进入另一个bash
      
        ctrl+d退出此bash
      
         u  返回上一个状态 往前走
 
         ctrl +r 往后走


###1未作成版本版本情况下重置上一个版本 
    
      git reset --hard HEAD

###2已作成版本情况下重置上一个版本
  
      git reset --hard HEAD^



__peter__的笔记

    pwd

    man pwd # q to quit

    mkdir dir

### path

    绝对路径: start with /
    相对路径: start with .

## shell prompt

    peter@cow:~/tg-note$
    user@machinename:currentWorkingDirectory(folder)$

# software installation

    sudo apt-get install tree


# tar 

http://www.happypeter.org/posts/10

# ref

http://happypeter.github.com/LGCB/

http://billie66.github.com/TLCL/book

__课上笔记__


一  权限问题
owner  group others
rwx    rwx   rwx
r 可读   w  可㝍   x可执行



二  HTML语言中
     <br>代表换行



三  如何查找

1 eg：进入 rm

      / +查找内容

      n 查找下一处

      N 查找上一处

2 在vim环境中同1

3 网页上查找

      / +内容

      ctrl+g 查找下一处

      ctrl+G 查找上一处

四  如何查看linux下隐藏的文件

     ls -a

    带“.”则表示此文件为隐藏文件

document     

    * n. 文件，公文；[计] 文档；证件

    * vt. 用文件证明

五 

  854  cd aaa/

  855  git init(初始化)

  856  ls -a（显示隐藏文件）

  857  vim hell

  858  ls

  859  git add hell（通知add跟踪hell）

  860  git commit -a（all） -m（message） "first"（创建第一个版本）

  861  tig（显示）

  862  history


六 查看两个文件的不同

   第一种方法

      differ -u h.c h1.c 

         保存到

         differ -u h.c h1.c > h.diff

      打补丁

        patch h.c < h.diff(将h.diff中内容加到h.c中)

        patch -R h.c < h.diff (将h.c 中内容减去h.diff内容 即恢复h.c内容)

   第二种方法

      git 方法

       1 mkdir ggg（新建ggg）

       2 cd ggg（进入ggg）

       3 git init（初始化）

       4 vim hello

       5 git add hello.c（通知add跟踪hello） 

       6 git commit -a -m "my first version"（创建第一个版本）


vim笔记

     vim 插入模式下Ctrl—n 自动补齐

     ctrl+shift+t 打开另一个标签
    
     在vim中如遇到打不开的问题
    
     原因

     1 有.note.md.swp 可能是已经打开了一个bash 
      

      解决方法：关闭一个bash
  

    2 可能上次未正常关闭vim


      解决方法： rm -rf .note.md.swp

##V  进入可视行模式

##只打开一个a.c时 打开b.c
   

    方法：“  ：e   b.c ”
 

   只关闭b.c
  
    方法  “：bd”


## vim 处理多个文件

   ：ls (查看buffer  buffer意思：缓冲区)
 

   ：bn （进入下一个bash）

  
   ：bp （进入上一个bash）



##缩进

  进入可是模式下" >" 即可缩进


##注册github 

  1  akaedu@akaedu-desktop:~$ pwd
  
  /home/akaedu

  akaedu@akaedu-desktop:~$ ssh-keygen

  Generating public/private rsa key pair.

  Enter file in which to save the key (/home/akaedu/.ssh/id_rsa): 

  Created directory '/home/akaedu/.ssh'.

  Enter passphrase (empty for no passphrase): 

  Enter same passphrase again: 

  Your identification has been saved in /home/akaedu/.ssh/id_rsa.

  Your public key has been saved in /home/akaedu/.ssh/id_rsa.pub.

  The key fingerprint is:

  0a:9b:08:7e:17:cf:79:01:16:d5:75:ec:6d:51:c8:56 akaedu@akaedu-desktop

  The key&apos;s randomart image is:

  +--[ RSA 2048]----+

  |       .... .o.+E|

  |        .  .  =o |

  |       o     .. o|

  |      . .      .o|

  |.   ..  S.     . |

  |.. . ++.. .      |

  | ...o..+ .       |

  |  . .   .        |

  |                 |

  +-----------------+

  akaedu@akaedu-desktop:~$ cd .ssh

  akaedu@akaedu-desktop:~/.ssh$ ls

  id_rsa  id_rsa.pub

  akaedu@akaedu-desktop:~/.ssh$ vim id_rsa.pub 



  2  Global setup:

     名称以及邮箱

     Set up git

     git config --global user.name "wangpan"



  Next steps:


  mkdir wangpan-note

  cd wangpan-note

  git init

  touch README

  git add README

  git commit -m 'first commit'

  git remote add origin git@github.com:wangpan/wangpan-note.git

  git push -u origin master

      


  Existing Git Repo?

  cd existing_git_repo

  git remote add origin git@github.com:wangpan/wangpan-note.git

  git push -u origin master

  __注__
  
   在往网页上传东西之前
   
   git commit -a -m "内容" 
   
   然后 
  
   git push 



ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAxUN8io2fEOy9XKqksV/hpGkaAaRfhIYlWVkFtMmzkyJFGrfGOBmJ75LFJ9NlDCZ0iTF3IIukF057FxxN1P0Pg6x2JMdqy9j5QzDmmdBcYoIa3k1tjHJsq8NcJ0UrCUBOqXjxKg/PYflSIfb5C5wV+NGS4LOw+TEdh5IWdhtdwLfHZYS2AS6uH8x83o+tHfkqca3HpJuu/xzI9shn3e4Hs3nzp1lKxGPC0Qk8hEUDhuj+2VBut0oTwS6JdLAx/gvH0Dp5MsulrON3DG+jzBQmCanVnclEka/zJPlM9jfl9fIVkZX4VunW5QmkTRBsMnDn+Lshs2vZBTvVOI2M8WMF9Q== akaedu@akaedu-desktop
