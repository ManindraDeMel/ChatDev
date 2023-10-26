# Agents de communication pour le développement de logiciels

<p align="center">
  <img src='../misc/logo1.png' width=550>
</p>

<p align="center">
    【Anglais | <a href="readme/README-Chinese.md">Chinois</a> | <a href="readme/README-Japanese.md">Japonais</a> | <a href="readme/README-Korean.md">Coréen</a> | <a href="readme/README-Filipino.md">Philippin</a> | <a href="readme/README-French.md">Français</a> | <a href="readme/README-Slovak.md">Slovaque</a> | <a href="readme/README-Portuguese.md">Portugais</a> | <a href="readme/README-Spanish.md">Espagnol</a> | <a href="readme/README-Dutch.md">Néerlandais</a> | <a href="readme/README-Hindi.md">Hindi</a>★
</p>
<p align="center">
    【📚 <a href="wiki.md">Wiki</a> | 🚀 <a href="wiki.md#local-demo">Démo locale</a> | 👥 <a href="Contribution.md">Community Built Software</a> | 🔧 <a href="wiki.md#customization">Customization</a> 文
</p>

## 📖 Vue d'ensemble

- **ChatDev** est une **société de logiciels virtuels** qui opère à travers divers agents **intelligents** accueillant rôles différents, y compris le Chief Executive Officer <img src='online_log/static/figures/ceo.png' height=20>, Chief Product Officer <img src='online_log/static/figures/cpo.png' height=20>, Chief Technology Officer <img src='online_log/static/figures/cto.png' height=20>, programmeur <img src='online_log/static/figures/programmer.png' height=20>, réviseur <img src='online_log/static/figures/reviewer.png' height=20>, testeur <img src='online_log/static/figures/tester.png' height=20>, concepteur artistique <img src='online_log/static/figures/designer.png' height=20>. Ces agents forment une structure organisationnelle multi-agents et sont unis par une mission de "révolutionner le monde numérique par la programmation". Les agents de ChatDev **collaborent à** en participant à des séminaires fonctionnels spécialisés, incluant des tâches telles que la conception, le codage, le test et la documentation.
- The primary objective of ChatDev is to offer an **easy-to-use**, **highly customizable** and **extendable** framework, which is based on large language models (LLMs) and serves as an ideal scenario for studying collective intelligence.
<p align="center">
  <img src='../misc/company.png' width=600>
</p>

## 🎉 Actualités

* **26 octobre 2023 : ChatDev est maintenant supporté avec Docker pour une exécution sûre** (merci à la contribution de [ManindraDeMel](https://github.com/ManindraDeMel)). Please see [Docker Start Guide](wiki.md#docker-start).
  <p align="center">
  <img src='../misc/docker.png' width=400>
  </p>
* 25 Septembre 2023 : Le mode **Git** est maintenant disponible, permettant au programmeur <img src='online_log/static/figures/programmer.png' height=20> d'utiliser Git pour le contrôle de version. Pour activer cette fonctionnalité, définissez simplement `"git_management"` à `"True"` dans `ChatChainConfig.json`. See [guide](wiki.md#git-mode).
  <p align="center">
  <img src='../misc/github.png' width=600>
  </p>
* 20 Septembre 2023 : Le mode **Human-Agent-Interaction** est maintenant disponible ! Vous pouvez vous impliquer dans l'équipe de ChatDev en jouant le rôle de l'évaluateur <img src='online_log/static/figures/reviewer.png' height=20> et en faisant des suggestions au programmeur <img src='online_log/static/figures/programmer.png' height=20>; essayer `python3 run. y --task [description_of_your_idea] --config "Human"`. Voir [guide](wiki.md#human-agent-interaction) et [exemple](WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='../misc/Human_intro.png' width=600>
  </p>
* Le 1er septembre 2023 : Le mode **Art** est disponible dès maintenant ! Vous pouvez activer l'agent concepteur <img src='online_log/static/figures/designer.png' height=20> pour générer des images utilisées dans le logiciel; essayez `python3 run.py --task [description_of_your_idea] --config "Art"`. Voir [guide](wiki.md#art) et [exemple](WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28 août 2023 : Le système est accessible au public.
* 17 août 2023: La version 1.0.0 était prête à être publiée.
* 30 juillet 2023 : Les utilisateurs peuvent personnaliser les paramètres ChatChain, Phase et Rôle. De plus, le mode de journal en ligne et le mode de relecture sont maintenant pris en charge.
* 16 juillet 2023 : Le [papier préimprimé](https://arxiv.org/abs/2307.07924) associé à ce projet a été publié.
* 30 juin 2023 : La version initiale du dépôt ChatDev a été publiée.

## ❓ Que peut faire ChatDev ?

![introduction](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡ Démarrage rapide

### 🖥️ Démarrage rapide avec le terminal

Pour commencer, suivez ces étapes:

1. **Cloner le dépôt GitHub :** Commencez par cloner le dépôt en utilisant la commande :
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Configurer l'environnement Python :** Assurez-vous que vous avez un environnement Python 3.9 ou supérieur. Vous pouvez créer et activer cet environnement en utilisant les commandes suivantes, en remplaçant `ChatDev_conda_env` par votre nom d'environnement préféré :
   ```
   conda create -n ChatDev_conda_env python=3.9 -y
   conda active ChatDev_conda_env
   ```
3. **Installez des dépendances :** Déplacez dans le répertoire `ChatDev` et installez les dépendances nécessaires en exécutant :
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **Définir la clé API OpenAI :** Exporter votre clé API OpenAI en tant que variable d'environnement. Remplacez `"votre_OpenAI_API_key"` par votre clé API réelle. Remember that this environment variable is session-specific, so you need to set it again if you open a new terminal session. Sous Unix/Linux :
   ```
   Exporter OPENAI_API_KEY="votre_clé OpenAI_API_key"
   ```
   Sous Windows:
   ```
   $env: OPENAI_API_KEY="votre_clé OpenAI_API_key"
   ```
5. **Build Your Software:** Use the following command to initiate the building of your software, replacing `[description_of_your_idea]` with your idea's description and `[project_name]` with your desired project name: On Unix/Linux:
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   Sous Windows:
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Run Your Software:** Once generated, you can find your software in the `WareHouse` directory under a specific project folder, such as `project_name_DefaultOrganization_timestamp`. Run your software using the following command within that directory: On Unix/Linux:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   Sous Windows:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 Démarrage rapide avec Docker
- Nous remercions [ManindraDeMel](https://github.com/ManindraDeMel) d'avoir fourni le support Docker. Please see [Docker Start Guide](wiki.md#docker-start).

## ✨ Compétences avancées

For more detailed information, please refer to our [Wiki](wiki.md), where you can find:

- Une introduction à tous les paramètres d'exécution de la commande.
- A straightforward guide for setting up a local web demo, which includes enhanced visualized logs, a replay demo, and a simple ChatChain Visualizer.
- Un aperçu du framework ChatDev.
- Une introduction complète à tous les paramètres avancés dans la configuration de ChatChain.
- Tutoriels pour personnaliser ChatDev, y compris :
    - ChatChain: Concevez votre propre processus de développement logiciel (ou tout autre processus), comme comme `DemandAnalysis -> Coding -> Tests -> Manuel`.
    - Phase : Concevez votre propre phase au sein de ChatChain, comme `DemandAnalysis`.
    - Role: Defining the various agents in your company, such as the `Chief Executive Officer`.

## 🤗 Partagez votre Logiciel!

**Code**: We are enthusiastic about your interest in participating in our open-source project. If you come across any problems, don't hesitate to report them. Feel free to create a pull request if you have any inquiries or if you are prepared to share your work with us! Vos contributions sont très appréciées. S'il vous plaît faites-moi savoir s'il y a autre chose vous avez besoin d'aide !

**Compagnie**: Créer votre propre "ChatDev Company" personnalisé est un jeu d'enfant. Cette configuration personnalisée implique trois fichiers de configuration JSON simples . Consultez l'exemple fourni dans le répertoire `CompanyConfig/Default`. Pour des instructions détaillées sur la personnalisation, reportez-vous à notre [Wiki](wiki.md).

**Software**: Whenever you develop software using ChatDev, a corresponding folder is generated containing all the essential information. Partagez votre travail avec nous est aussi simple que de faire une pull request. Voici un exemple : exécutez la commande `python3 run.py --task "design a 2048 game" --name "2048" --org "THUNLP" --config "Default"`. Ceci va créer un package logiciel et générer un dossier nommé `/WareHouse/2048_THUNLP_timestamp`. À l'intérieur, vous trouverez :

- Tous les fichiers et documents liés au logiciel du jeu 2048
- Fichiers de configuration de la société responsable de ce logiciel, y compris les trois fichiers de configuration JSON de `CompanyConfig/Default`
- Un journal détaillé détaillant le processus de construction du logiciel qui peut être utilisé pour rejouer (`timestamp.log`)
- L'invite initiale utilisée pour créer ce logiciel (`2048.prompt`)

**See community contributed software [here](Contribution.md)!**

## :man_technologiste:<unk> Contributeurs

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

Made with [contrib.rocks](https://contrib.rocks).
## :magnifying_verre_tilted_right: Citation

```
@misc{qian2023communicative,
      title={Communicative Agents for Software Development}, 
      auteur={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      year={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      Classe primaire ={cs.SE}
}
```

## ⚖️ Licence

- Licence de code source : le code source de notre projet est sous licence Apache 2.0. Cette licence permet l'utilisation, la modification et la distribution du code, sous réserve de certaines conditions décrites dans la licence Apache 2.0.
- Project Open-Source Status: Le projet est en effet open-source; cependant, cette désignation est principalement destinée à des fins non commerciales. Tandis que nous encourageons la collaboration et les contributions de la communauté pour la recherche et les applications non commerciales, il est important de noter que toute utilisation des composants du projet à des fins commerciales nécessite des accords de licence distincts.
- Licence de données : Les données connexes utilisées dans notre projet sont sous licence CC BY-NC 4.0. Cette licence permet explicitement une utilisation non commerciale des données. Nous tenons à souligner que tous les modèles formés à l'utilisation de ces jeux de données doivent respecter strictement la restriction d'utilisation non commerciale et doivent être employés exclusivement à des fins de recherche.

## 🌟 Historique des étoiles

[![Graphique d'histoire des étoiles](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 Remerciements

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 Contact

Si vous avez des questions, des commentaires ou si vous souhaitez nous contacter, n'hésitez pas à nous contacter par e-mail à [chatdev. penbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
