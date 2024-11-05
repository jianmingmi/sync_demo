为 openvela 做出贡献
====================

\[ [English](CONTRIBUTING.md) | 简体中文 \]

openvela 由一支活跃的软件工程师和研究人员团队开发。欢迎开源社区为改进此项目做出任何贡献！

openvela 采用 Apache License 2.0 许可证。

签署 CLA
--------

您必须签署贡献者许可协议才能做出贡献。

\[ [个人版](https://open-vela.cnbj1.mi-fds.com/open-vela/cla/Xiaomi_Documentation_Open_Source_Individual_CLA.pdf) | [企业版](https://open-vela.cnbj1.mi-fds.com/open-vela/cla/Xiaomi_Documentation_Open_Source_Corporate_CLA.pdf) \]

错误报告
-------

如果您认为在 openvela 中发现了错误，请首先确保您针对最新版本的 openvela 进行测试（您的问题可能已得到修复）。
如果没有，请在 GitHub 上搜索我们的问题列表，以防已经出现类似的问题。

功能请求
-------

如果您希望使用 openvela 中不存在的功能，那么可能不是您一个人。可能还有其他人有类似的需求。openvela 今天的很多功能都是因为我们的用户看到了需求而添加的。
在 GitHub 上的问题列表中打开一个问题，描述您希望看到的功能、您需要它的原因以及它应该如何工作。

贡献代码和文档更改
----------------

如果您想为 openvela 贡献新功能或错误修复，请先在 GitHub 问题上讨论您的想法。如果您的想法没有 GitHub 问题，请打开一个。可能有人已经在处理它，或者在开始实施之前您应该了解特定的复杂性。通常有很多方法可以解决问题，在花时间处理无法合并的 PR 之前，找到正确的方法非常重要。

### fork 并克隆存储库

您需要fork主 openvela 代码或文档存储库并将其克隆到本地机器。请参阅 [GitHub 帮助页面](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) 获取帮助。

### 代码更改提示

在提出拉取请求之前遵循这些提示将加快审核周期。

* 添加适当的单元测试
* 如果适用，添加集成测试
* 确保添加的代码遵循格式指南
* 不属于您更改的行不应被编辑（例如，不要格式化未更改的行，不要重新排序现有的导入）
* 将适当的许可证标头添加到任何新文件

### 提交您的更改

* 测试你的更改
   
        运行测试套件以确保没有出现任何问题。

* 签署贡献者许可协议
   
        请确保您已签署我们的贡献者许可协议。我们并非要求您将版权转让给我们，而是要求我们无限制地分发您的代码。我们要求所有贡献者都这样做，是为了向我们的用户保证代码的来源和持续存在。您只需签署一次 CLA。

* 重新设定你的更改
   
        使用主 openvela 存储库中的最新代码更新您的本地存储库，并将您的分支重新定位到最新主分支之上。我们希望您的初始更改被压缩为单个提交。稍后，如果我们要求您进行更改，请将它们添加为单独的提交。这使其更易于审查。作为合并前的最后一步，我们将要求您自己压缩所有提交，或者我们会为您完成。

* 提交拉取请求
   
        将本地更改推送到您fork的存储库副本并提交拉取请求。在拉取请求中，选择一个总结您所做的更改的标题，并在正文中提供有关更改的更多详细信息。还请提及发生讨论的问题编号，例如“关闭 #123”。
    

### 冲突的处理方式

通常情况下，除非与主分支存在合并冲突，否则您无需重新定位您的拉取请求。当 GitHub 抱怨您的拉取请求“无法自动合并”时，系统会要求您使用以下命令将您的拉取请求重新定位到最新的主分支之上：

* 首先重新定位到最新的主分支

        git remote add upstream https://github.com/open-vela/[repository].git
        git fetch upstream
        git rebase upstream/[branch]

* 然后 git 可能会在无法合并时显示一些冲突，比如`conflict.cpp`，需要
  - 手动修改文件以解决冲突
  - 解决后，将其标记为已解决

        git add conflict.cpp

* 然后你可以通过以下方式继续进行 rebase

        git rebase --continue

* 最后推送到你的 fork，然后 pull request 将会更新

        git push --force
