# ipc-connect-FUZZ-tool
ipc连接FUZZ工具
IPC（ Internet Process Connection）是共享“命名管道”的资管，它是为了让进城间通信而开放的命名管道，可以通过验证用户名和密码获得相关的权限，在远程管路计算机和查看计算机的共享资源时使用。![image](https://user-images.githubusercontent.com/79234113/145709315-715683cf-825d-4fc8-9f17-cb8104b24e82.png)

建立IPC常见的错误代码
	• (1) 5：拒绝访问，可能是使用的不是管理员权限，需要先提升权限
	• (2) 51：网络问题，windoows无法找到网络路径
	• (3) 53：找不到网站路径，可能是IP地址错误，目标未开机，目标Lanmanserver服务未启动、有防火墙等问题
	• (4) 67：找不到网络名，本地Lanmanworkstation服务未启动，目标删除ipc$
	• (5) 1219：提供的凭据和已存在的凭据集冲突，说明已建立IPC$，需要先删除
	• (6) 1326：账号密码错误
	• (7) 1792：目标NetLogon服务未启动，连接域控常常会出现此情况
	• (8) 2242：用户密码过期，目标有账号策略，强制定期更改密码
建立IPC失败的原因
	• (1) 目标系统不是NT或以上的操作系统
	• (2) 对方没有打开IPC$共享
	• (3) 对方未开启139,445端口，或者被防火墙屏蔽
(4) 输出命令，账号密码有错误


内网工具，使用python编写的工具，编译好了，直接上传到目标机进行测试
字典和用户名，以及Ip是通过信息收集得来的
![屏幕截图 2021-12-12 174127](https://user-images.githubusercontent.com/79234113/145709190-33ccb380-48d9-4041-9862-550da2c0fd62.png)
![屏幕截图 2021-12-12 174207](https://user-images.githubusercontent.com/79234113/145709237-8927e28b-1e05-44b1-9f4e-6d44d8d6c22e.png)
![屏幕截图 2021-12-12 174218](https://user-images.githubusercontent.com/79234113/145709240-fc33e128-5080-4a7c-80d6-d0f549ea2eb6.png)
![屏幕截图 2021-12-12 174230](https://user-images.githubusercontent.com/79234113/145709243-c4654f42-5971-4416-ae5c-7f1f173bcd2f.png)、
直接打开baopo.exe文件，把收集到的IP，密码,用户名，分别保存与baopo.exe一个目录下面，然后输入文件名（不需要输入txt后缀名字）
![屏幕截图 2021-12-12 173959](https://user-images.githubusercontent.com/79234113/145709246-3454b7a3-6707-4cfb-9644-597ce787ae91.png)

![屏幕截图 2021-12-12 174013](https://user-images.githubusercontent.com/79234113/145709285-983430b6-8bc9-45be-915f-46823ba33e70.png)
![屏幕截图 2021-12-12 170812](https://user-images.githubusercontent.com/79234113/145709290-8e23e6d0-4b94-4c56-b5e8-386ecf38385d.png)
成功
![屏幕截图 2021-12-12 174428](https://user-images.githubusercontent.com/79234113/145709292-8eb46c0d-b74a-497d-baa6-68edad7f9a5a.png)
