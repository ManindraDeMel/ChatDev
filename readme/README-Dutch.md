# Communicatieve agenten voor softwareontwikkeling

<p align="center">
  <img src='../misc/logo1.png' width=550>
</p>

<p align="center">
    【English | <a href="readme/README-Chinese.md">Chinese</a> | <a href="readme/README-Japanese.md">Japanese</a> | <a href="readme/README-Korean.md">Korean</a> | <a href="readme/README-Filipino.md">Filipino</a> | <a href="readme/README-French.md">French</a> | <a href="readme/README-Slovak.md">Slovak</a> | <a href="readme/README-Portuguese.md">Portuguese</a> | <a href="readme/README-Spanish.md">Spanish</a> | <a href="readme/README-Dutch.md">Dutch</a> | <a href="readme/README-Hindi.md">Hindi</a>】
</p>
<p align="center">
    (unnamed@@0) 📚 <a href="wiki.md">Wiki</a> ½ 🚀 <a href="wiki.md#local-demo">Lokale Demo</a> ## 👥 <a href="Contribution.md">Community Built Software</a> ½ 🔧 <a href="wiki.md#customization">Aanpassen</a>(%)
</p>

## 📖 Overzicht

- **ChatDev** staat als een **virtueel softwarebedrijf** dat opereert via verschillende **intelligente agenten** met verschillende rollen houd. inclusief Chief Executive Officer <img src='online_log/static/figures/ceo.png' height=20>, Chief Product Officer <img src='online_log/static/figures/cpo.png' height=20>, Chief Technology Officer <img src='online_log/static/figures/cto.png' height=20>, programmeur <img src='online_log/static/figures/programmer.png' height=20>, reviewer <img src='online_log/static/figures/reviewer.png' height=20>, tester <img src='online_log/static/figures/tester.png' height=20>, art designer <img src='online_log/static/figures/designer.png' height=20>. These agents form a multi-agent organizational structure and are united by a mission to "revolutionize the digital world through programming." De agenten binnen ChatDev **werken samen** door deel te nemen aan gespecialiseerde functionele seminars, inclusief taken zoals het ontwerpen, coderen, testen en documenteren.
- Het primaire doel van ChatDev is om een **makkelijk te gebruiken**, **zeer aanpasbaar** en **uitbreidbaar** framework die is gebaseerd op grote taalmodellen (LLM's) en fungeert als een ideaal scenario voor het bestuderen van collectieve intelligentie.
<p align="center">
  <img src='../misc/company.png' width=600>
</p>

## 🎉 Nieuws

* **26 oktober, 2023: ChatDev wordt nu ondersteund met Docker voor een veilige executie** (dankzij de bijdrage van [ManindraDeMel](https://github.com/ManindraDeMel)). Zie [Start Guide van Docker](wiki.md#docker-start).
  <p align="center">
  <img src='../misc/docker.png' width=400>
  </p>
* 25 september, 2023: De **Git** modus is nu beschikbaar, zodat de programmeur <img src='online_log/static/figures/programmer.png' height=20> Git kan gebruiken voor versiemanagement. Om deze functie in te schakelen, stel `"git_management"` in op `"True"` in `ChatChainConfig.json`. Zie [handleiding](wiki.md#git-mode).
  <p align="center">
  <img src='../misc/github.png' width=600>
  </p>
* 20 September 2023: De **Human-Agent-Interactie** modus is nu beschikbaar! U kunt betrokken raken bij het ChatDev team door de rol van reviewer <img src='online_log/static/figures/reviewer.png' height=20> te spelen en suggesties te doen aan de programmeur <img src='online_log/static/figures/programmer.png' height=20>; probeer `python3 run. y --task [description_of_your_idea] --config "Human"`. Zie [handleiding](wiki.md#human-agent-interaction) en [voorbeeld](WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='../misc/Human_intro.png' width=600>
  </p>
* 1 September 2023: De **Kunst** modus is nu beschikbaar! Je kunt de designer agent <img src='online_log/static/figures/designer.png' height=20> activeren om afbeeldingen te genereren die gebruikt worden in de software; probeer `python3 run.py --task [description_of_your_idea] --config "Art"`. Zie [handleiding](wiki.md#art) en [voorbeeld](WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28 augustus 2023: het systeem is openbaar beschikbaar.
* 17de augustus, 2023: de v1.0.0 versie was klaar voor release.
* 30 juli, 2023: Gebruikers kunnen ChatChain, Fase en Rol instellingen aanpassen. Bovendien, worden zowel de online logmodus als de replay modus nu ondersteund.
* 16, 2023: de [voordruk papier](https://arxiv.org/abs/2307.07924) geassocieerd met dit project is gepubliceerd.
* 30 juni, 2023: De eerste versie van de ChatDev repository is vrijgegeven.

## ❓ Wat kan ChatDev doen?

![intro](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡ Quickstart

### 🖥️ Quickstart met terminal

Volg deze stappen om te beginnen:

1. **Kloon de GitHub Repository:** Begin door de repository te klonen met behulp van de opdracht:
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Stel Python Environment in:** Zorg ervoor dat je een versie 3.9 of een hogere Python omgeving hebt. U kunt deze omgeving maken en activeren met behulp van de volgende commando's, vervang `ChatDev_conda_env` door uw gewenste omgeving naam:
   ```
   conda maakt -n ChatDev_conda_env python=3.9 y
   conda activeer ChatDev_conda_env
   ```
3. **Installeer Afhankelijkheden:** Verplaats naar de `ChatDev` map en installeer de benodigde afhankelijkheden door uit te voeren:
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **Set OpenAI API-sleutel:** Exporteer uw OpenAI API-sleutel als een omgevingsvariabele. Vervang `"your_OpenAI_API_key"` met je werkelijke API-sleutel. Onthoud dat deze omgevingsvariabele sessie-specifiek is, dus moet je hem opnieuw instellen als je een nieuwe terminale sessie opent. In Unix/Linux:
   ```
   export OPENAI_API_KEY="jouw_OpenAI_API_key"
   ```
   In Windows:
   ```
   $env:OPENAI_API_KEY="jouw_OpenAI_API_key"
   ```
5. **Bouw Uw Software:** Gebruik het volgende commando om het bouwen van uw software te starten, vervangt `[description_of_your_idea]` door uw idea's beschrijving en `[project_name]` door het gewenste project naam: On Unix/Linux:
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   In Windows:
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Voer Uw Software uit:** Eenmaal gegenereerd, u kunt uw software vinden in de `Magazijn` directory onder een specifieke projectmap, zoals `project_name_DefaultOrganization_timestamp`. Voer uw software uit met behulp van de volgende opdracht binnen die directory: On Unix/Linux:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   In Windows:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 Quickstart met Docker
- Wij danken [ManindraDeMel](https://github.com/ManindraDeMel) voor het bieden van Docker ondersteuning. Zie [Start Guide van Docker](wiki.md#docker-start).

## ✨ Geavanceerde Vaardigheden

Raadpleeg voor meer gedetailleerde informatie onze [Wiki](wiki.md), waar je het kan vinden:

- Een introductie tot alle commando-uitvoeringsparameters.
- Een eenvoudige handleiding voor het opzetten van een lokale webdemo, die uitgebreide visualiseerde logs, een replay demo, en een simpele ChatChain Visualizer.
- Een overzicht van het ChatDev framework.
- Een uitgebreide introductie van alle geavanceerde parameters in de ChatChain-configuratie.
- Handleidingen voor het aanpassen van ChatDev, waaronder:
    - ChatChain: Ontwerp uw eigen softwareontwikkelingsproces (of elk ander proces), zoals als `DemandAnalyse -> Codering -> Testen -> Handmatig`.
    - Fase: Ontwerp je eigen fase binnen ChatChain, zoals `DemandAnalyse`.
    - Rol: Definiëren van de verschillende agenten van uw bedrijf, zoals de `Chief Executive Officer`.

## 🤗 Deel uw Software!

**Code**: We zijn enthousiast over je interesse in deelname aan ons open-source project. If you come across any problems, don't hesitate to report them. Voel je vrij om een pull-aanvraag te maken als je vragen hebt of bereid bent om je werk met ons te delen! Uw bijdragen worden zeer gewaardeerd. Laat het me weten als er iets anders is je hulp nodig hebt!

**Bedrijf**: het maken van uw eigen aangepaste "ChatDev Bedrijf" is een fluitje. Deze gepersonaliseerde configuratie omvat drie eenvoudige configuratie JSON bestanden. Bekijk het voorbeeld in de `CompanyConfig/Default` map. Voor gedetailleerde instructies over aanpassingen, ga naar onze [Wiki](wiki.md).

**Software**: Wanneer u software ontwikkelt met ChatDev, wordt er een overeenkomstige map gegenereerd met alle essentiële informatie van . Het delen van je werk met ons is zo eenvoudig als het doen van een pull-verzoek. Hier is een voorbeeld: voer de command `python3 run.py --task "design een spel" --name "2048" --org "THUNLP" --config "Default"`. Dit zal een softwarepakket maken en een map aanmaken met de naam `/WareHouse/2048_THUNLP_timestamp`. Binnen zal je het vinden:

- Alle bestanden en documenten die gerelateerd zijn aan de 2048 spel software
- Configuratiebestanden van het bedrijf dat verantwoordelijk is voor deze software, inclusief de drie JSON configuratiebestanden van `CompanyConfig/Default`
- Een uitgebreid logboek met daarin het bouwproces van de software dat kan worden gebruikt om te herspelen (`timestamp.log`)
- De eerste prompt die werd gebruikt om deze software te maken (`2048.prompt`)

**Zie community bijgedragen software [hier](Contribution.md)!**

## 👨‍💻58 bijdragers

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

Gemaakt met [contrib.rocks](https://contrib.rocks).
## 🔎 Citatie

```
@misc{qian20communicatief,
      title={Communicative Agents for Software Development}, 
      auteur ={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      jaar ={2023},
      eprint={2307.07924},
      archiefvoorvoegsel={arXiv}
      primaryClass={cs.SE}
}
```

## :balance_schaal: Licentie

- Broncode licentie: de broncode van ons project is gelicentieerd onder de Apache 2.0 License. Deze licentie staat het gebruik, wijziging en distributie van de code toe, onder bepaalde voorwaarden zoals beschreven in de Apache 2.0 licentie.
- Open-Source project status: het project is inderdaad open source; deze benaming is echter voornamelijk bedoeld voor niet-commerciële doeleinden. Terwijl we samenwerking en bijdragen van de gemeenschap voor onderzoek en niet-commerciële toepassingen aanmoedigen, het is belangrijk op te merken dat voor elk gebruik van de onderdelen van het project voor commerciële doeleinden aparte licentieovereenkomsten nodig zijn.
- Gegevenslicentie: de gerelateerde gegevens gebruikt in ons project is gelicenseerd onder CC BY-NC 4.0. Deze licentie staat uitdrukkelijk niet-commercieel gebruik van de gegevens toe. Wij willen benadrukken dat alle modellen die worden opgeleid met behulp van deze datasets strikt de hand moeten houden aan de beperking van het niet-commerciële gebruik en uitsluitend voor onderzoeksdoeleinden moeten worden gebruikt.

## 🌟 Stergeschiedenis

[![Ster Geschiedenis Grafiek](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 Kennisgevingen

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 Contact

Als u vragen, feedback heeft of contact met u wilt hebben, Voel je vrij om ons te bereiken via e-mail via [chatdev. penbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
