# Kommunikativa agenter för programvaruutveckling

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    <unk> Engelska <unk> <a href="readme/README-Chinese.md">Kinesiska</a> <unk> <a href="readme/README-Japanese.md">Japanska</a> <unk> <a href="readme/README-Korean.md">Koreanska</a> <unk> <a href="readme/README-Filipino.md">Filipino</a> <unk> <a href="readme/README-French.md">Franska</a> <unk> <a href="readme/README-Slovak.md">Slovakiska</a> <unk> <a href="readme/README-Portuguese.md">Portugisiska</a> <unk> <a href="readme/README-Spanish.md">Spanska</a> <unk> <a href="readme/README-Dutch.md">Holländska</a> <unk> <a href="readme/README-Hindi.md">Hindi</a> <unk>
</p>
<p align="center">
    <unk> 📚 <a href="wiki.md">Wiki</a> <unk> 🚀 <a href="wiki.md#local-demo">Local Demo</a> <unk> :busts_in_siluette: <a href="Contribution.md">Community Built Software</a> <unk> 🔧 <a href="wiki.md#customization">Anpassning</a> <unk>
</p>

## 📖 Översikt

- **ChatDev** är ett **virtuellt programvaruföretag** som verkar genom olika **intelligenta agenter** som innehar olika roller, inklusive verkställande direktör <img src='online_log/static/figures/ceo.png' height=20>, produktchef <img src='online_log/static/figures/cpo.png' height=20>, teknisk chef <img src='online_log/static/figures/cto.png' height=20>, programmerare <img src='online_log/static/figures/programmer.png' height=20>, granskare <img src='online_log/static/figures/reviewer.png' height=20>, testare <img src='online_log/static/figures/tester.png' height=20>, konstdesigner <img src='online_log/static/figures/designer.png' height=20>. Dessa agenter bildar en organisationsstruktur för flera agenter och förenas av ett uppdrag att "revolutionera den digitala världen genom programmering". Agenterna inom ChatDev **samarbetar** genom att delta i specialiserade funktionella seminarier, inklusive uppgifter som utformning, kodning, testning och dokumentation.
- Det primära målet för ChatDev är att erbjuda en **lättanvänd**, **mycket anpassningsbara** och **utbyggbara** ramverk, som bygger på stora språkmodeller (LLM) och fungerar som ett idealiskt scenario för att studera kollektiv intelligens.
<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## 🎉 Nyheter

* **26 oktober, 2023: ChatDev stöds nu med Docker för säkert utförande** (tack vare bidrag från [ManindraDeMel](https://github.com/ManindraDeMel)). Se [Docker Start Guide](wiki.md#docker-start).
  <p align="center">
  <img src='./misc/docker.png' width=400>
  </p>
* 25 september, 2023: läget **Git** är nu tillgängligt, vilket gör det möjligt för programmeraren <img src='online_log/static/figures/programmer.png' height=20> att använda Git för versionskontroll. För att aktivera den här funktionen sätter du helt enkelt `"git_management"` till `"True"` i `ChatChainConfig.json`. Se [guide](wiki.md#git-mode).
  <p align="center">
  <img src='./misc/github.png' width=600>
  </p>
* 20 september 2023: läget **Human-Agent-Interaction** är nu tillgängligt! Du kan engagera dig i ChatDev-teamet genom att spela rollen som recensent <img src='online_log/static/figures/reviewer.png' height=20> och komma med förslag till programmeraren <img src='online_log/static/figures/programmer.png' height=20>; prova `python3 run. y --task [description_of_your_idea] --config "Människa"`. Se [guide](wiki.md#human-agent-interaction) och [exempel](WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='./misc/Human_intro.png' width=600>
  </p>
* 1 september, 2023: läget **Art** är tillgängligt nu! Du kan aktivera designeragenten <img src='online_log/static/figures/designer.png' height=20> för att generera bilder som används i programvaran; prova `python3 run.py --task [description_of_your_idea] --config "Art"`. Se [guide](wiki.md#art) och [exempel](WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28 augusti 2023: Systemet är offentligt tillgängligt.
* 17 augusti, 2023: Versionen v1.0.0 var klar för release.
* 30:e juli, 2023: Användare kan anpassa ChatChain, fas och roll inställningar. Dessutom stöds nu både online loggläge och replay -läge.
* July 16th, 2023: The [preprint paper](https://arxiv.org/abs/2307.07924) associated with this project was published.
* 30 juni, 2023: Den första versionen av ChatDev-arkivet släpptes.

## ❓ Vad kan ChatDev göra?

![intro](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡ Snabbstart

### 🖥️ Quickstart med terminal

Följ dessa steg för att komma igång:

1. **Klona GitHub Repository:** Börja med att klona utvecklingskatalogen med kommandot:
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Ställ in Pythonmiljö:** Se till att du har en version 3.9 eller högre Pythonmiljö. Du kan skapa och aktivera denna miljö med följande kommandon, ersätta `ChatDev_conda_env` med ditt önskade miljö -namn:
   ```
   conda skapa -n ChatDev_conda_env python=3,9 -y
   conda aktivera ChatDev_conda_env
   ```
3. **Installera beroenden:** Flytta till `ChatDev` -katalogen och installera nödvändiga beroenden genom att köra:
   ```
   cd ChatDev
   pip3 installera -r requirements.txt
   ```
4. **Set OpenAI API Key:** Exportera din OpenAI API-nyckel som en miljövariabel. Ersätt `"your_OpenAI_API_key"` med din faktiska API-nyckel. Kom ihåg att denna miljövariabel är sessionsspecifik, så du måste ställa in den igen om du öppnar en ny terminalsession. På Unix/Linux:
   ```
   exportera OPENAI_API_KEY="your_OpenAI_API_key"
   ```
   På Windows:
   ```
   $env:OPENAI_API_KEY="din_OpenAI_API_key"
   ```
5. **Bygg din programvara:** Använd följande kommando för att initiera byggandet av din programvara, ersätter `[description_of_your_idea]` med din idés beskrivning och `[project_name]` med ditt önskade projekt namn: På Unix/Linux:
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   På Windows:
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Kör din Programvara:** En gång genereras, du kan hitta din programvara i `WareHouse` -katalogen under en specifik projektmapp, såsom `project_name_DefaultOrganization_timestamp`. Kör din programvara med följande kommando i den katalogen: På Unix/Linux:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   På Windows:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 Snabbstart med Docker
- Vi tackar [ManindraDeMel](https://github.com/ManindraDeMel) för att ha gett Docker-stöd. Se [Docker Start Guide](wiki.md#docker-start).

## ✨ Avancerade färdigheter

För mer detaljerad information, se vår [Wiki](wiki.md), där du kan hitta:

- En introduktion till alla kommando-körparametrar.
- En enkel guide för att skapa en lokal webbdemo, som inkluderar förbättrade visualiserade loggar, en reprisdemo, och en enkel ChatChain Visualizer.
- En översikt över ChatDevs ramverk.
- En omfattande introduktion till alla avancerade parametrar i ChatChain-konfiguration.
- Guider för att anpassa ChatDev, inklusive:
    - ChatChain: Designa din egen programvaruutvecklingsprocess (eller någon annan process), sådan som `DemandAnalysis -> Kodning -> Testing -> Manuell`.
    - Fas: Designa din egen fas inom ChatChain, som `DemandAnalysis`.
    - Roll: Definiera olika agenter i ditt företag, såsom `VD`.

## 🤗 Dela din programvara!

**Kod**: Vi är entusiastiska över ditt intresse för att delta i vårt projekt med öppen källkod. Om du stöter på några problem, tveka inte att rapportera dem. Skapa gärna en pullförfrågan om du har några frågor eller om du är beredd att dela ditt arbete med oss! Dina bidrag är högt värderade. Please let me know if there's anything else you need assistance!

**Företag**: Skapa din egen anpassade "ChatDev Company" är en vind. Denna personliga inställning omfattar tre enkla konfigurationsfiler för JSON. Kolla in exemplet som finns i `Företagskonfigur/Standard` -katalogen. För detaljerade instruktioner om anpassning, se vår [Wiki](wiki.md).

**Software**: När du utvecklar programvara med ChatDev, genereras en motsvarande mapp som innehåller all nödvändig information för . Att dela ditt arbete med oss är lika enkelt som att göra en pull-förfrågan. Här är ett exempel: kör kommandot `python3 run.py --task "design a 2048 game" --name "2048" --org "THUNLP" --config "Standard"`. Detta kommer skapa ett programpaket och generera en mapp som heter `/WareHouse/2048_THUNLP_timestamp`. Inuti hittar du:

- Alla filer och dokument relaterade till spelprogrammet 2048
- Konfigurationsfiler för det företag som ansvarar för denna programvara, inklusive de tre JSON-konfigurationsfilerna från `CompanyConfig/Default`
- En omfattande logg som beskriver programvarans byggprocess som kan användas för att spela upp (`timestamp.log`)
- Den första prompten som används för att skapa denna programvara (`2048.prompt`)

**Se communitybidrog programvara [här](Contribution.md)!**

## 👨‍💻<unk> Bidragsgivare

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

Gjord med [contrib.rocks](https://contrib.rocks).
## 🔎 Referens

```
@misc{qian2023communicativ,
      title={Communicative Agents for Software Development}, 
      författare={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      år={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      primary Class={cs.SE}
}
```

## ⚖️ Licens

- Källkodslicens: Vårt projekts källkod är licensierad under Apache 2.0-licensen. Denna licens tillåter användning, modifiering och distribution av koden, med förbehåll för vissa villkor som beskrivs i Apache 2.0-licensen.
- Status för projektet Öppen källkod: Projektet är verkligen öppen källkod; men denna beteckning är främst avsedd för icke-kommersiella ändamål. Samtidigt som vi uppmuntrar samarbete och bidrag från samhället för forskning och icke-kommersiella tillämpningar, Det är viktigt att notera att all användning av projektets komponenter för kommersiella ändamål kräver separata licensavtal.
- Data Licensiering: De relaterade data som används i vårt projekt licensieras under CC BY-NC 4.0. Denna licens tillåter uttryckligen icke-kommersiell användning av uppgifterna. Vi vill betona att alla modeller som utbildats med hjälp av dessa dataset strikt bör följa den icke-kommersiella användningsbegränsningen och endast användas för forskningsändamål.

## 🌟 Stjärnhistorik

[![Stjärnhistorik Diagram](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 Erkännanden

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 Kontakt

Om du har frågor, feedback, eller vill höra av dig, tveka inte att nå ut till oss via e-post på [chatdev. penbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
