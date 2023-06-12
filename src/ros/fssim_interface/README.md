# Interface for FSSIM

In order to create a universal simulator, FSSIM comunicated with your own framework through this interface.
This package does not contain any logic, it only translated messages from FSSIM into your messages. 

* `config`: contains definitions of topics which are translated

# How to run FSSIM

Detailed description can be found in [fssim](https://github.com/bitfsd/fssim)

### Run FSSIM parallely to your code
If you want to run simulator in one terminal window and be able to test your code in parallel execute
1. `roslaunch fssim_interface only_fssim.launch`
2. Your pipeline, e.g. `roslaunch control trackdrive.launch


这是一个 ROS 节点的接口说明文档，介绍了如何与 FSSIM 虚拟仿真平台进行通信，并提供了一个 ROS 包，用于将 FSSIM 发布的消息转换成你自己的消息格式。

具体来说，该文档包含以下内容：

- `config`：定义了需要转换的主题名称，在 ROS 中通过配置文件实现。在 FSSIM 和你自己的代码之间建立通信时，需要确保这些主题名称在 FSSIM 和 ROS 之间能够正确匹配。
- 运行 FSSIM：介绍了如何在 ROS 中运行 FSSIM 并与你自己的代码同时运行。通过此方法，你可以在单个终端窗口中同时运行模拟器和你开发的代码，并且可以实时测试代码的功能。具体步骤是：
  1. 使用 `roslaunch fssim_interface only_fssim.launch` 命令启动 FSSIM 节点；
  2. 使用 `roslaunch` 命令启动你自己的节点，例如 `roslaunch control trackdrive.launch`。

总之，该文档提供了一种与 FSSIM 虚拟仿真平台进行通信的方法，并且帮助你快速开始使用 FSSIM 进行车辆自主驾驶算法的开发和测试。