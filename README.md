# Go  
Go是谷歌开发的一款简介高效的编程语言，编译的速度相当快，而且学习难度相对而言比较简单，适用于微服务，AI等领域  
##如何配置  
1.到[官网](https://golang.google.cn/dl/)下载go（这个是中国国内的网站），我以linuxubuntu 25.04配置为例，下载好之后在下载文件夹下打开终端，运行  
```  
tar -xzf 文件名 -C /usr/local/
```
然后将环境变量添加到```~/.bashrc```中  
```
export GOROOT=/usr/local/go  
export PATH=$GOROOT/bin:$PATH  
export GOPATH=$HOME/go  
export PATH=$PATH:$GOPATH/bin
```
运行  
```
mkdir -p ~/go/{bin,src,pkg}  
source ~/.bashrc  
```
使其生效  
然后打开一个**新的**终端，运行  
```
go version
```
如果有输出类似go1.24.3的，就代表安装配置成功了，然后安装code  
```
sudo snap install code --classic
```
可以尝试编写第一个go程序来验证是否安装成功  
安装vim  
```
sudo apt install vim
cd
cd  桌面
vi hello.go  
```
在打开的终端中按下键盘上的"I"按键，复制下方代码  
```
package main  
import "fmt"  
func main() {  
    fmt.Println("Hello, World!\nGo!")  
}
```
然后按下键盘上的```Ctrl```+```Shift```+```V```粘贴，接着按下```Esc```键推出到普通模式(左下方没有**插入**两个字)，然后按住```Shift```+```;```，输入```x```退出，然后运行  
```
go run hello.go  //直接运行程序
```
或者  
```
go build hello.go //将程序编译为为二进制文件
./hello //运行程序
```
终端应该输出  
```
HelloWorld!
Go!
```
如果输出成功就证明你已经成功配置了go的开发环境，可以开始编程了(可以使用Code里面的Copilot自动编成，选择Agent模式)  
[注册github账号如果无法注册，地区选择美国](https://github.com)
