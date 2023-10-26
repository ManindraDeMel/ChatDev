# 软件开发通信代理

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    【English | <a href="../readme/README-Chinese.md">Chinese</a> | <a href="../readme/README-Japanese.md">Japanese</a> | <a href="../readme/README-Korean.md">Korean</a> | <a href="../readme/README-Filipino.md">Filipino</a> | <a href="../readme/README-French.md">French</a> | <a href="../readme/README-Slovak.md">Slovak</a> | <a href="../readme/README-Portuguese.md">Portuguese</a> | <a href="../readme/README-Spanish.md">Spanish</a> | <a href="../readme/README-Dutch.md">Dutch</a> | <a href="../readme/README-Hindi.md">Hindi</a>】
</p>
<p align="center">
    [📚 <a href="../wiki.md">Wiki</a> | :ro火箭: <a href="../wiki.md#local-demo">Local Demo</a> | 👥 <a href="../Contribution.md">Community Built Software</a> | 🔧 <a href="../wiki.md#customization">Customization</a> expert
</p>

## 📖 概览

- **ChatDev** 代表 **虚拟软件公司** 通过各种 **智能代理** 持有 不同的角色 包括首席执行干事 <img src='online_log/static/figures/ceo.png' height=20>、首席产品干事 <img src='online_log/static/figures/cpo.png' height=20>、首席技术干事 <img src='online_log/static/figures/cto.png' height=20>、 程序员 <img src='online_log/static/figures/programmer.png' height=20>, 审核员 <img src='online_log/static/figures/reviewer.png' height=20>, 测试员 <img src='online_log/static/figures/tester.png' height=20>, 艺术设计师 <img src='online_log/static/figures/designer.png' height=20> These agents form a multi-agent organizational structure and are united by a mission to "revolutionize the digital world through programming." The agents within ChatDev **collaborate** by participating in specialized functional seminars, including tasks such as designing, coding, testing, and documenting.
- ChatDev的主要目标是提供 **易用的** **高度可自定义的** 和 **可扩展的** 框架 基于大型语言模式(LLMs)，是研究集体情报的理想情景。
<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## :party_poper: 新闻

* **2023年10月26日：ChatDev现在被Docker支持安全执行** (感谢 [Manindrade Mel](https://github.com/ManindraDeMel) 的贡献)。 请参阅 [停靠首页指南](wiki.md#docker-start)
  <p align="center">
  <img src='./misc/docker.png' width=400>
  </p>
* 2023年9月25日： **Git** 模式现在可用，使程序员 <img src='online_log/static/figures/programmer.png' height=20> 能够使用Git来控制版本。 要启用此功能，只需将 `"git_management"` 设置为 `"True"` 设置为 `ChatChainConfig.json` 中。 见 [指南](wiki.md#git-mode)。
  <p align="center">
  <img src='./misc/github.png' width=600>
  </p>
* 2023年9月20日： **人际交流** 模式现在可用！ You can get involved with the ChatDev team by playing the role of reviewer <img src='online_log/static/figures/reviewer.png' height=20> and making suggestions to the programmer <img src='online_log/static/figures/programmer.png' height=20>; try `python3 run.py --task [description_of_your_idea] --config "Human"`. 见 [指南](wiki.md#human-agent-interaction) 和 [示例](WareHouse/Gomoku_HumanAgentInteraction_20230920135038)。
  <p align="center">
  <img src='./misc/Human_intro.png' width=600>
  </p>
* 2023年9月1日： **Art** 模式现在可用！ 您可以激活设计代理 <img src='online_log/static/figures/designer.png' height=20> 生成软件中使用的图像； 请尝试 `python3 run.py --task [description_of_your_idea] --config "Art"` 见 [指南](wiki.md#art) 和 [示例](WareHouse/gomokugameArtExample_THUNLP_20230831122822)。
* 2023年8月28日：该系统可供公众使用。
* 2023年8月17日：v1.0.0版本已准备就绪。
* 2023年7月30日：用户可以自定义聊天链、阶段和角色设置。 此外，现在支持在线日志模式和重播 模式。
* 2023年7月16日：与这个项目相关的 [预印文件](https://arxiv.org/abs/2307.07924) 已经出版。
* 2023年6月30日：最初版本的ChatDev仓库已经发布。

## ❓ ChatDev Do是什么？

![介绍者](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## :hig_voltag: 快速开始

### :desktop_compute：快速开启终端

要开始, 请按照以下步骤:

1. **克隆GitHub 仓库：** 通过使用命令克隆仓库：
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **设置 Python 环境：** 确保您有 3.9 或更高版本的 Python 环境。 You can create and activate this environment using the following commands, replacing `ChatDev_conda_env` with your preferred environment name:
   ```
   conda create -n ChatDev_conda_env python=3.9 -y
   conda 激活 ChatDev_conda_env
   ```
3. **安装依赖关系:** 移动到 `ChatDev` 目录并通过运行以下列方式安装必要的依赖关系：
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **Set OpenAI API Key:** Export your OpenAI API key as an environment variable. Replace `"your_OpenAI_API_key"` with your actual API key. 请记住，这个环境变量是针对会话的，所以如果您 打开一个新的终端会话，您需要重新设置它。 在 Unix/Linux 上：
   ```
   导出 OPENAI_API_KEY="your_OpenAI_API_key"
   ```
   窗口：
   ```
   $env:OPENAI_API_KEY="your_OpenAI_API_key"
   ```
5. **构建您的软件：** 使用以下命令来启动软件的构建。 用您的想法说明取代 `[description_of_your_idea]` 以及 `[project_name]` 使用您所期望的项目 名称： Unix/Linux：
   ```
   python3 run.py --task "[description_of_your_idea]"--name "[project_name]
   ```
   窗口：
   ```
   python run.py --task "[description_of_your_idea]"--name "[project_name]
   ```
6. **运行您的软件：** 生成后， 您可以在 `仓库` 指定的 项目文件夹下找到您的软件 例如 `project_name_DefaultOrganization_timestamp` 在该目录中使用以下命令 运行您的软件： Unix/Linux：
   ```
   cd Warehouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   窗口：
   ```
   cd Warehouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### :affecting_whale: 快速启动 Docker
- 我们感谢 [ManindradeMel](https://github.com/ManindraDeMel) 提供Docker支持。 请参阅 [停靠首页指南](wiki.md#docker-start)

## :sparkles：高级技能

欲了解更多详细信息，请参阅我们的 [Wiki](wiki.md)，您可以在那里找到：

- 所有命令运行参数的导言。
- 用于设置本地网页演示的直截了当的指南，包括强化可视化日志、回放演示和 简单的ChatChain Visualizer。
- ChatDev框架概览。
- ChatChain 配置中所有高级参数的全面介绍。
- 自定义 ChatDev的指南，包括：
    - ChatChain: Design your own software development process (or any other process), such as `DemandAnalysis -> Coding -> Testing -> Manual`.
    - 阶段：设计您自己在聊天链中的相应阶段，例如 `需求分析`
    - 角色：界定您公司中的各种代理人，如 `首席执行官`

## 🤗 分享你的软件!

**代码**: 我们对您参与我们开源项目的兴趣很热情。 如果你遇到任何 问题，请不要犹豫地报告它们。 如果您有任何查询或者 准备与我们分享您的工作，请随时创建拉取请求！ 您的贡献价值很高。 Please let me know if there's anything else you need assistance!

**公司**: 创建您自己自定义的“ChatDev Company”是一种简易。 此个性化设置涉及三个简单的 配置 JSON 文件。 查看在 `CompanyConfig/默认` 目录中提供的示例。 关于自定义的详细 说明，请参阅我们的 [Wiki](wiki.md)

**软件**: 每当您使用 ChatDev开发软件时，都会生成包含所有 基本信息的相应文件夹。 与我们分享您的工作与提出拉取请求一样简单。 下面是一个示例：执行 命令 `python3 run.py --task "design a 2048 game" --name "2048" --org "THUNP" --config "Default"` 这将 创建一个软件包，并生成一个名为 `/Warehouse/2048_THUNGP_timestamp` 的文件夹。 在内部，您会找到：

- 所有与2048游戏软件相关的文件和文档
- Configuration files of the company responsible for this software, including the three JSON config files from `CompanyConfig/Default`
- 详细说明软件构建流程的完整日志 (`timestamp.log`)
- 用于创建此软件的初始提示(`2048.mound`)

**See community contributed software [here](Contribution.md)!**

## 👨‍💻contributors

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

使用 [contrib.rocks](https://contrib.rocks)
## 🔎 引用

```
@misc{qian2023communicative,
      title={Communicative Agents for Software Development}, 
      author={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      year={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      primaryClass={cs.SE}
}
```

## :balanc_scale : 许可协议

- 源代码许可：我们的项目源代码是在 Apache 2.0 许可下授权的。 该许可证允许使用、修改和分发代码，但须遵守Apache 2.0 许可证中概述的某些条件。
- 开放源码项目：该项目的确是开放源码的；然而，这一指定主要是为了非商业目的。 我们鼓励社区在研究和非商业应用方面进行合作和作出贡献。 必须指出，任何将项目部件用于商业目的的做法都需要有单独的许可证协议。
- 数据许可：我们项目中使用的相关数据是根据CCBY-NC 4.0许可的。 该许可证明确允许非商业性地使用数据。 我们要强调，任何使用这些数据集培训的模型都应严格遵守非商业性使用限制，并应专门用于研究。

## 🌟 星历

[![星历图](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 鸣谢

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="../misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="../misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="../misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 联系人

如果您有任何问题，反馈或想要联系， 请随时通过 [chatdev 通过电子邮件联系我们。 penbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
