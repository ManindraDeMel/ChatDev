# Agents de communication pour le développement de logiciels

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    【Anglais | <a href="readme/README-Chinese.md">Chinois</a> | <a href="readme/README-Japanese.md">Japonais</a> | <a href="readme/README-Korean.md">Coréen</a> | <a href="readme/README-Filipino.md">Philippin</a> | <a href="readme/README-French.md">Français</a> | <a href="readme/README-Slovak.md">Slovaque</a> | <a href="readme/README-Portuguese.md">Portugais</a> | <a href="readme/README-Spanish.md">Espagnol</a> | <a href="readme/README-Dutch.md">Néerlandais</a> | <a href="readme/README-Hindi.md">Hindi</a>★
</p>
<p align="center">
    【📚 <a href="../wiki.md">Wiki</a> | 🚀 <a href="../wiki.md#local-demo">Démo Locale</a> | 👥 <a href="../Contribution.md">Logiciels de la Communauté</a> | 🔧 <a href="../wiki.md#customization">Personnalisation</a>】
</p>

## 📖 Vue d'ensemble

- **ChatDev** se présente comme une **société de logiciels virtuelle** opérant par le biais de divers **agents intelligents** tenant différents rôles, incluant le Directeur Général <img src='../online_log/static/figures/ceo.png' height=20>, le Directeur de Produit <img src='../online_log/static/figures/cpo.png' height=20>, le Directeur Technologique <img src='../online_log/static/figures/cto.png' height=20>, programmeur <img src='../online_log/static/figures/programmer.png' height=20>, l'auditeur <img src='../online_log/static/figures/reviewer.png' height=20>, le testeur <img src='../online_log/static/figures/tester.png' height=20> et le designer graphique <img src='../online_log/static/figures/designer.png' height=20>. Ces agents forment une structure organisationnelle multi-agents et sont unis par une mission de "révolutionner le monde numérique à travers la programmation." Les agents de ChatDev **collaborent** en participant à des séminaires fonctionnels spécialisés, incluant des tâches telles que la conception, le codage, les tests et la documentation.
- L'objectif principal de ChatDev est de proposer un cadre **facile à utiliser**, **hautement personnalisable** et **extensible**, basé sur de grands modèles linguistiques (LLMs) et servant de scénario idéal pour étudier l'intelligence collective.
<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## 📰 Actualités

* **26 octobre 2023 : ChatDev est maintenant supporté avec Docker pour une exécution sûre** (merci à la contribution de [ManindraDeMel](https://github.com/ManindraDeMel)). Please see [Docker Start Guide](wiki.md#docker-start).
  <p align="center">
  <img src='./misc/docker.png' width=400>
  </p>
* **25 septembre 2023 : La fonctionnalité **Git** est maintenant disponible**, permettant au programmeur <img src='../online_log/static/figures/programmer.png' height=20> d'utiliser GitHub pour le contrôle de version. Pour activer cette fonction, définissez simplement `"git_management"` sur `"True"` dans `ChatChainConfig.json`. See [guide](wiki.md#git-mode).
  <p align="center">
  <img src='./misc/github.png' width=600>
  </p>
* 20 septembre 2023 : Le mode **Interaction Humain-Agent** est maintenant disponible ! Vous pouvez interagir avec l'équipe ChatDev en jouant le rôle de l'examinateur <img src='../online_log/static/figures/reviewer.png' height=20> et en faisant des suggestions au programmeur <img src='../online_log/static/figures/programmer.png' height=20>; essayez `python3 run.py --task [description_de_votre_idée] --config "Humain"`. Voir le [guide](../wiki.md#human-agent-interaction) et l'[exemple](../WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='./misc/Human_intro.png' width=600>
  </p>
* 1er septembre 2023 : Le mode **Art** est maintenant disponible ! Vous pouvez activer l'agent designer <img src='../online_log/static/figures/designer.png' height=20> pour générer des images utilisées dans le logiciel; essayez `python3 run.py --task [description_de_votre_idée] --config "Art"`. Voir le [guide](../wiki.md#art) et l'[exemple](../WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28 août 2023 : Le système est désormais disponible au public.
* 17 août 2023 : La version v1.0.0 était prête à être publiée.
* 30 juillet 2023 : Les utilisateurs peuvent personnaliser les paramètres de ChatChain, Phase et Rôle. De plus, le mode journal en ligne et le mode de relecture sont désormais pris en charge.
* 16 juillet 2023 : L'[article préimprimé](https://arxiv.org/abs/2307.07924) associé à ce projet a été publié.
* 30 juin 2023 : La version initiale du dépôt ChatDev a été publiée.

## ❓ Que peut faire ChatDev ?

![introduction](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡️ Démarrage rapide

### 🖥️ Démarrage rapide avec le terminal

Pour commencer, suivez ces étapes:

1. **Clonez le dépôt GitHub:** Commencez par cloner le dépôt en utilisant la commande:
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Configurer l'environnement Python:** Assurez-vous que vous disposez d'un environnement Python de version 3.9 ou supérieure. Vous pouvez créer et activer cet environnement en utilisant les commandes suivantes, en remplaçant `ChatDev_conda_env` par votre environnement préféré nom :
   ```
   conda create -n ChatDev_conda_env python=3.9 -y
   conda active ChatDev_conda_env
   ```
3. **Installer les dépendances:** Déplacez-vous dans le répertoire `ChatDev` et installez les dépendances nécessaires en exécutant :
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **Définir la clé API OpenAI:** Exportez votre clé API OpenAI en tant que variable d'environnement. Remplacez `" your_OpenAI_API_key "` par votre clé API proprement dite. Rappelez-vous que cette variable d'environnement est spécifique à une session, vous devez donc la redéfinir à chaque nouvelle instance de terminal. Sous Unix/Linux :
   ```
   Exporter OPENAI_API_KEY="votre_clé OpenAI_API_key"
   ```
   Sous Windows :
   ```
   $env: OPENAI_API_KEY="votre_clé OpenAI_API_key"
   ```
5. **Construisez Votre Logiciel :** Utilisez la commande suivante pour initier la construction de votre logiciel, en remplaçant `[description_of_your_idea]` par la description de votre idée et `[project_name]` par le nom souhaité pour votre projet : Sur Unix/Linux :
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   Sous Windows :
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Exécutez Votre Logiciel :** Une fois généré, vous pouvez trouver votre logiciel dans le répertoire `WareHouse` sous un dossier de projet spécifique, tel que `project_name_DefaultOrganization_timestamp`. Exécutez votre logiciel avec la commande suivante dans ce répertoire : Sur Unix/Linux :
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   Sous Windows :
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 Démarrage rapide avec Docker
- Nous remercions [ManindraDeMel](https://github.com/ManindraDeMel) d'avoir fourni le support Docker. Please see [Docker Start Guide](wiki.md#docker-start).

## ✨ Compétences avancées

Pour plus d'informations détaillées, veuillez consulter notre [Wiki](../wiki.md), où vous pouvez trouver :

- Une introduction à tous les paramètres d'exécution de la commande.
- Un guide simple pour configurer une démo web locale, incluant des logs visualisés améliorés, une démo de revision, et un simple visualiseur ChatChain.
- Un aperçu du framework ChatDev.
- Une introduction complète à tous les paramètres avancés de la configuration ChatChain.
- Des guides pour personnaliser ChatDev, y compris :
    - ChatChain : Concevez votre propre processus de développement de logiciel (ou tout autre processus), comme `AnalyseDeLaDemande -> Codage -> Test -> Manuel`.
    - Phase : Concevez votre propre phase au sein de ChatChain, comme `AnalyseDeLaDemande`.
    - Rôle : Définissez les différents agents de votre entreprise, comme le `Directeur Général`.

## 🤗 Partagez Votre Logiciel !

**Code** : Nous sommes enthousiastes à l'idée de votre intérêt à participer à notre projet open-source. Si vous rencontrez des problèmes, n'hésitez pas à les signaler. N'hésitez pas à créer une demande de pull si vous avez des questions ou si vous êtes prêt à partager votre travail avec nous ! Vos contributions sont très appréciées. Faites-moi savoir s'il y a autre chose dont vous avez besoin !

**Entreprise** : Créer votre propre "ChatDev Entreprise" personnalisée est un jeu d'enfant. Cette configuration personnalisée implique trois simples fichiers JSON de configuration. Consultez l'exemple fourni dans le répertoire `CompanyConfig/Default`. Pour des instructions détaillées sur la personnalisation, reportez-vous à notre [Wiki](../wiki.md).

**Logiciel** : Chaque fois que vous développez un logiciel avec ChatDev, un dossier correspondant est généré contenant toutes les informations essentielles. Partager votre travail avec nous est aussi simple que de faire une demande de pull. Voici un exemple : exécutez la commande `python3 run.py --task "concevoir un jeu 2048" --name "2048"  --org "THUNLP" --config "Default"`. Ceci créera un paquet logiciel et générera un dossier nommé `/WareHouse/2048_THUNLP_timestamp`. A l'intérieur, vous trouverez :

- Tous les fichiers et documents relatifs au logiciel de jeu 2048
- Les fichiers de configuration de l'entreprise responsable de ce logiciel, y compris les trois fichiers JSON de configuration de `CompanyConfig/Default`
- Un journal complet détaillant le processus de construction du logiciel qui peut être utilisé pour rejouer (`timestamp.log`)
- L'invite initiale utilisée pour créer ce logiciel (`2048.prompt`)

**Voir les logiciels contribués par la communauté [ici](../Contribution.md)!**

## Contributor

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

Made with [contrib.rocks](https://contrib.rocks).
## 📑 Citation

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

- Licence du code source : Le code source de notre projet est sous licence Apache 2.0. Cette licence autorise l'utilisation, la modification et la distribution du code, sous réserve de certaines conditions définies dans la Licence Apache 2.0.
- Statut Open-Source du Projet : Le projet est effectivement open-source ; cependant, cette désignation est principalement destinée à des fins non commerciales. Bien que nous encouragions la collaboration et les contributions de la communauté pour la recherche et les applications non commerciales, il est important de noter que toute utilisation des composants du projet à des fins commerciales nécessite des accords de licence séparés.
- Licence des données : Les données associées utilisées dans notre projet sont sous licence CC BY-NC 4.0. Cette licence permet explicitement l'utilisation non commerciale des données. Nous souhaitons souligner que tout modèle formé à l'aide de ces ensembles de données doit strictement respecter la restriction d'utilisation non commerciale et ne doit être utilisé que pour des fins de recherche.

## Historique des Étoiles

[![Graphique de l'Historique des Étoiles](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## ✨️ Compétences Avancées

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## Contact

Si vous avez des questions, des retours ou souhaitez nous contacter, n'hésitez pas à nous envoyer un email à [chatdev.openbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
