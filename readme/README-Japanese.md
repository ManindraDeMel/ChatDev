# ソフトウェア開発のための通信エージェント

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    【English | <a href="readme/README-Chinese.md">Chinese</a> | <a href="readme/README-Japanese.md">Japanese</a> | <a href="readme/README-Korean.md">Korean</a> | <a href="readme/README-Filipino.md">Filipino</a> | <a href="readme/README-French.md">French</a> | <a href="readme/README-Slovak.md">Slovak</a> | <a href="readme/README-Portuguese.md">Portuguese</a> | <a href="readme/README-Spanish.md">Spanish</a> | <a href="readme/README-Dutch.md">Dutch</a> | <a href="readme/README-Hindi.md">Hindi</a>】
</p>
<p align="center">
    【📚 <a href="wiki.md">Wiki</a> | 🚀 <a href="wiki.md#local-demo">Local Demo</a> | :busts_in_sシルエット: <a href="Contribution.md">Community Built Software</a> | 🔧 <a href="wiki.md#customization">Customization</a>】
</p>

## 📖 概要

- **ChatDev** stands as a **virtual software company** that operates through various **intelligent agents** holding different roles, including Chief Executive Officer <img src='online_log/static/figures/ceo.png' height=20>, Chief Product Officer <img src='online_log/static/figures/cpo.png' height=20>, Chief Technology Officer <img src='online_log/static/figures/cto.png' height=20>, programmer <img src='online_log/static/figures/programmer.png' height=20>, reviewer <img src='online_log/static/figures/reviewer.png' height=20>, tester <img src='online_log/static/figures/tester.png' height=20>, art designer <img src='online_log/static/figures/designer.png' height=20>. これらの エージェントは、マルチエージェント組織構造を形成し、「プログラミングを通じてデジタルワールド に革命をもたらす」という使命によって結束しています。 ChatDev **内のエージェントは、** に特化した機能セミナーに参加し、 の設計、コーディング、テスト、文書化などのタスクに参加します。
- The primary objective of ChatDev is to offer an **easy-to-use**, **highly customizable** and **extendable** framework, which is based on large language models (LLMs) and serves as an ideal scenario for studying collective intelligence.
<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## 🎉 ニュース

* **October 26th, 2023: ChatDev is now supported with Docker for safe execution** (thanks to contribution from [ManindraDeMel](https://github.com/ManindraDeMel)). [Docker スタートガイド](wiki.md#docker-start) をご覧ください。
  <p align="center">
  <img src='./misc/docker.png' width=400>
  </p>
* 2023年9月25日: **Git** モードが利用可能になり、プログラマ <img src='online_log/static/figures/programmer.png' height=20> がGitをバージョン管理に利用できるようになりました。 この機能を有効にするには、 `"git_management"` を `"True"` を `ChatChainConfig.json` に設定するだけです。 [ガイド](wiki.md#git-mode) をご覧ください。
  <p align="center">
  <img src='./misc/github.png' width=600>
  </p>
* 2023年9月20日: **ヒューマンエージェント対話** モードが利用可能になりました! You can get involved with the ChatDev team by playing the role of reviewer <img src='online_log/static/figures/reviewer.png' height=20> and making suggestions to the programmer <img src='online_log/static/figures/programmer.png' height=20>; try `python3 run.py --task [description_of_your_idea] --config "Human"`. [ガイド](wiki.md#human-agent-interaction) と [例](WareHouse/Gomoku_HumanAgentInteraction_20230920135038) を参照してください。
  <p align="center">
  <img src='./misc/Human_intro.png' width=600>
  </p>
* 2023年9月1日： **アート** モードが登場！ You can activate the designer agent <img src='online_log/static/figures/designer.png' height=20> to generate images used in the software; try `python3 run.py --task [description_of_your_idea] --config "Art"`. [ガイド](wiki.md#art) と [例](WareHouse/gomokugameArtExample_THUNLP_20230831122822) を参照してください。
* 2023年8月28日：システムが一般公開される。
* 2023年8月17日: v1.0.0バージョンがリリースされました。
* 2023年7月30日:ChatChain、Phase、Role の設定をユーザがカスタマイズできるようになりました。 さらに、オンラインログモードとリプレイ モードがサポートされるようになりました。
* 2023年7月16日: このプロジェクトに関連する [プリプリント ペーパー](https://arxiv.org/abs/2307.07924) を発行しました。
* 2023年6月30日: ChatDev リポジトリの初期バージョンをリリースしました。

## ❓ ChatDev は何ができますか？

![intro](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡ クイックスタート

### 🖥️ 端末からクイックスタート

開始するには、以下の手順に従ってください:

1. **GitHub リポジトリのクローン:** コマンドを使用してリポジトリをクローンします。
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Python 環境のセットアップ:** バージョン 3.9 以上の Python 環境があることを確認してください。 次のコマンドを使用して作成して アクティブ化することができます。 `ChatDev_conda_env` をお好みの環境 名に置き換えます:
   ```
   conda create -n ChatDev_conda_env python=3.9 -y
   conda activate ChatDev_conda_env
   ```
3. **依存関係のインストール:** `ChatDev` ディレクトリに移動し、必要な依存関係を実行してインストールします。
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **OpenAI APIキーを設定:** OpenAI APIキーを環境変数としてエクスポートします。 `"your_OpenAI_API_key"` を実際の API キーに 置き換えます。 Remember that this environment variable is session-specific, so you need to set it again if you open a new terminal session. Unix/Linuxの場合:
   ```
   export OPENAI_API_KEY="your_OpenAI_API_key"
   ```
   Windows の場合:
   ```
   $env:OPENAI_API_KEY="your_OpenAI_API_key"
   ```
5. **ソフトウェアのビルド:** ソフトウェアのビルドを開始するには、次のコマンドを使用します。 ** ** `[description_of_your_idea]` をアイデアの説明に置き換え、 `[project_name]` ご希望のプロジェクト 名前: Unix/Linux の場合:
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   Windows の場合:
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Run Your Software:** Once generated, you can find your software in the `WareHouse` directory under a specific project folder, such as `project_name_DefaultOrganization_timestamp`. Run your software using the following command within that directory: On Unix/Linux:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   Windows の場合:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 Dockerでクイックスタート
- Dockerのサポートをご提供いただき、 [ManindraDeMel](https://github.com/ManindraDeMel) に感謝します。 [Docker スタートガイド](wiki.md#docker-start) をご覧ください。

## ✨ 上級スキル

詳細については、 [Wiki](wiki.md)を参照してください。見つけることができます:

- すべてのコマンド実行パラメータの紹介。
- 強化された可視化されたログ、リプレイデモ、および シンプルなChatChain Visualizerを含むローカルWebデモを設定するための簡単なガイド。
- ChatDevフレームワークの概要。
- ChatChain設定のすべての高度なパラメータの包括的な紹介。
- 以下を含むChatDevのカスタマイズのためのガイド:
    - ChatChain: 独自のソフトウェア開発プロセス(またはその他のプロセス)を設計します。 such as `DemandAnalysis -> Coding -> Testing -> Manual`.
    - フェーズ: `DemandAnalysis` のように、ChatChain内で独自のフェーズを設計します。
    - 役割: `CEO` など、会社の様々なエージェントを定義します。

## 🤗 あなたのソフトウェアを共有！

**コード**: オープンソースプロジェクトに参加することに熱心に取り組んでいます。 問題に遭遇した場合は、遠慮なく報告してください。 お問い合わせがある場合、または の方は、お気軽にプルリクエストを作成してください! あなたの貢献は高く評価されています。 Please let me know if there's anything else you need assistance!

**Company**: 独自のカスタマイズされた「ChatDev Company」を作成するのは簡単です。 このパーソナライズされたセットアップには、3つのシンプルな 構成 JSONファイルが含まれます。 `CompanyConfig/Default` ディレクトリの例を確認してください。 For detailed instructions on customization, refer to our [Wiki](wiki.md).

**ソフトウェア**: ChatDevを使用してソフトウェアを開発するたびに、すべての 必須情報を含む対応するフォルダが生成されます。 私たちとあなたの作品を共有することは、プルリクエストを作成するのと同じくらい簡単です。 例: コマンド `python3 run.py --task "design a 2048 game" --name "2048" --org "THUNLP" --config "Default"` を実行します。 ソフトウェアパッケージを作成し、 `/WareHouse/2048_THUNLP_timestamp` という名前のフォルダを生成します。 内部で見つけることができます:

- 2048年のゲームソフトウェアに関連するすべてのファイルとドキュメント
- CompanyConfig/Default `の 3 つの JSON 設定ファイル` を含む、このソフトウェアの責任者の設定ファイル
- リプレイに使用できるソフトウェアのビルドプロセスを詳述した包括的なログ (`timestamp.log`)
- このソフトウェアを作成するための最初のプロンプト（`2048.prompt`）

**See community contributed software [here](Contribution.md)!**

## 👨‍💻<unk> 貢献者

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

[contrib.rock](https://contrib.rocks) で作られました。
## 🔎 文献情報

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

## ⚖️ ライセンス

- ソースコードライセンス: プロジェクトのソースコードは Apache 2.0 ライセンスに基づいてライセンスされています。 このライセンスは、Apache 2.0 ライセンスに記載されている特定の条件に従い、コードの使用、変更、配布を許可します。
- プロジェクト オープンソースの状態: このプロジェクトはオープンソースですが、この指定は主に非営利目的を目的としています。 我々は、研究と非商用アプリケーションのためにコミュニティからの協力と貢献を奨励する一方で、 プロジェクトの部品を商業目的に活用するには別々のライセンス契約が必要であることに注意することが重要です。
- データライセンス: 当社のプロジェクトで使用される関連データは、CC BY-NC 4.0でライセンスされています。 このライセンスは、データの非商用利用を明示的に許可します。 私たちは、これらのデータセットを使用して訓練されたすべてのモデルが非商用利用制限を厳密に遵守し、研究目的のみに使用されるべきであることを強調したいと思います。

## 🌟 星の歴史

[![星の履歴チャート](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 Acknowledgments

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 連絡先

If you have any questions, feedback, or would like to get in touch, please feel free to reach out to us via email at [chatdev.openbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
