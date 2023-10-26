# Kommunikations-Agenten für Softwareentwicklung

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    <unk> <unk> Englisch | <a href="../readme/README-Chinese.md">Chinesisch</a> | <a href="../readme/README-Japanese.md">Japanisch</a> | <a href="../readme/README-Korean.md">Koreanisch</a> | <a href="../readme/README-Filipino.md">Filipino</a> | <a href="../readme/README-French.md">Französisch</a> | <a href="../readme/README-Slovak.md">Slowakisch</a> | <a href="../readme/README-Portuguese.md">Portugiesisch</a> | <a href="../readme/README-Spanish.md">Spanisch</a> | <a href="../readme/README-Dutch.md">Niederländische</a> | <a href="../readme/README-Hindi.md">Hindi</a>
</p>
<p align="center">
    <unk> 📚 <a href="../wiki.md">Wiki</a> | 🚀 <a href="../wiki.md#local-demo">Lokale Demo</a> | 👥 <a href="../Contribution.md">Community Built Software</a> | 🔧 <a href="../wiki.md#customization">Anpassung</a>
</p>

## 📖 Übersicht

- **ChatDev** steht als **virtuelles Softwareunternehmen** , das über verschiedene **intelligente Agenten** mit verschiedenen Rollen agiert einschließlich Chief Executive Officer <img src='online_log/static/figures/ceo.png' height=20>, Chief Product Officer <img src='online_log/static/figures/cpo.png' height=20>, Chief Technology Officer <img src='online_log/static/figures/cto.png' height=20>, Programmierer <img src='online_log/static/figures/programmer.png' height=20>, Reviewer <img src='online_log/static/figures/reviewer.png' height=20>, Tester <img src='online_log/static/figures/tester.png' height=20>, Kunstdesigner <img src='online_log/static/figures/designer.png' height=20>. Diese Agenten von bilden eine mehrtägige Organisationsstruktur und sind durch eine Mission vereint, „die digitale Welt durch Programmierung zu revolutionieren.“ Die Agenten in ChatDev **arbeiten mit** zusammen, indem sie an spezialisierten funktionalen Seminaren teilnehmen, einschließlich Aufgaben wie Entwurf, Codierung, Testen und Dokumentation.
- Das Hauptziel von ChatDev ist es, eine **einfach zu bedienende**anzubieten, **stark anpassbar** und **erweiterbar** Framework, basiert auf großen Sprachmodellen (LLMs) und dient als ideales Szenario für das Studium kollektiver Intelligenz.
<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## 🎉 News

* **26. Oktober 2023: ChatDev wird jetzt mit Docker zur sicheren Ausführung von** unterstützt (dank des Beitrags von [ManindraDeMel](https://github.com/ManindraDeMel)). Siehe [Docker Start Guide](wiki.md#docker-start).
  <p align="center">
  <img src='./misc/docker.png' width=400>
  </p>
* 25. September 2023: Der **Git** Modus ist jetzt verfügbar, so dass der Programmierer <img src='online_log/static/figures/programmer.png' height=20> Git für die Versionskontrolle verwenden kann. Um diese Funktion zu aktivieren, setzen Sie einfach `"git_management"` auf `"True"` in `ChatChainConfig.json`. Siehe [Guide](wiki.md#git-mode).
  <p align="center">
  <img src='./misc/github.png' width=600>
  </p>
* 20. September 2023: Der **Mensch-Agent-Interaktion** Modus ist jetzt verfügbar! Du kannst dich mit dem ChatDev-Team beteiligen, indem du die Rolle des Überprüfers <img src='online_log/static/figures/reviewer.png' height=20> spielst und dem Programmierer <img src='online_log/static/figures/programmer.png' height=20>Vorschläge machst. versuche `python3 run. y --task [description_of_your_idea] --config "Mensch"`. Siehe [Guide](wiki.md#human-agent-interaction) und [Beispiel](WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='./misc/Human_intro.png' width=600>
  </p>
* 1. September 2023: Der **Art** Modus ist jetzt verfügbar! Sie können den Designer Agent <img src='online_log/static/figures/designer.png' height=20> aktivieren, um in der Software verwendete Bilder zu generieren; versuchen Sie `python3 run.py --task [description_of_your_idea] --config "Art"`. Siehe [Guide](wiki.md#art) und [Beispiel](WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28. August 2023: Das System ist öffentlich zugänglich.
* 17. August 2023: Die v1.0.0 Version war zur Veröffentlichung bereit.
* 30. Juli 2023: Benutzer können ChatChain, Phase und Rollen anpassen. Zusätzlich werden sowohl der Online-Log-Modus als auch der Wiedergabemodus unterstützt.
* 16. Juli 2023: Das diesem Projekt zugeordnete [Vorabdruckpapier](https://arxiv.org/abs/2307.07924) wurde veröffentlicht.
* 30. Juni 2023: Die ursprüngliche Version des ChatDev Repositories wurde veröffentlicht.

## ❓ Was kann ChatDev tun?

![einleitung](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## :High_Spannung: Schnellstart

### 🖥️ Schnellstart mit Terminal

Um loszulegen, folgen Sie diesen Schritten:

1. **Klone das GitHub Repository:** Beginne mit dem Klonen des Repositorys mit dem Befehl:
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Python-Umgebung einrichten:** Stellen Sie sicher, dass Sie eine Version 3.9 oder höher Python-Umgebung haben. Sie können diese Umgebung mit den folgenden Befehlen erstellen und aktivieren und `ChatDev_conda_env` mit dem Namen Ihrer bevorzugten Umgebung ersetzen:
   ```
   conda create -n ChatDev_conda_env python=3.9 -y
   conda aktivieren ChatDev_conda_env
   ```
3. **Abhängigkeiten installieren:** In das `ChatDev` Verzeichnis verschieben und die notwendigen Abhängigkeiten installieren, indem du ausführst:
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **OpenAI API-Schlüssel:** Den OpenAI API-Schlüssel als Umgebungsvariable exportieren. Ersetzen Sie `"your_OpenAI_API_key"` durch Ihren aktuellen API-Schlüssel. Denken Sie daran, dass diese Umgebungsvariable sessionsspezifisch ist, also müssen Sie sie erneut einstellen, wenn Sie eine neue Terminalsitzung öffnen. Unter Unix/Linux:
   ```
   OPENAI_API_KEY="deine_OpenAI_API_key" exportieren
   ```
   Unter Windows:
   ```
   $env:OPENAI_API_KEY="dein_OpenAI_API_key"
   ```
5. **Erstellen Sie Ihre Software:** Verwenden Sie den folgenden Befehl, um die Erstellung Ihrer Software zu initiieren ersetzen Sie `[description_of_your_idea]` mit der Beschreibung Ihrer Idee und `[project_name]` mit Ihrem gewünschten Projekt Namen: unter Unix/Linux:
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   Unter Windows:
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Starten Sie Ihre Software:** Einmal generiert, finden Sie Ihre Software im `WareHouse` Verzeichnis unter einem bestimmten Projektordner zum Beispiel `project_name_DefaultOrganization_timestamp`. Führen Sie Ihre Software mit dem folgenden Befehl in diesem Verzeichnis aus: unter Unix/Linux:
   ```
   cd WareHouse/Projekt_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   Unter Windows:
   ```
   cd WareHouse/Projekt_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 Schnellstart mit Docker
- Wir danken [ManindraDeMel](https://github.com/ManindraDeMel) für die Unterstützung des Dockers. Siehe [Docker Start Guide](wiki.md#docker-start).

## ✨ Erweiterte Fähigkeiten

Für genauere Informationen lesen Sie bitte unser [Wiki](wiki.md), wo Sie finden können:

- Eine Einführung in alle Kommandolaufparameter.
- Ein einfacher Leitfaden zum Einrichten einer lokalen Web-Demo mit verbesserten visualisierten Logs, einer Replay-Demo und einem einfachen ChatChain Visualizer.
- Eine Übersicht des ChatDev Frameworks.
- Eine umfassende Einführung in alle erweiterten Parameter in der ChatChain-Konfiguration.
- Anleitungen zum Anpassen von ChatDev, einschließlich:
    - ChatChain: Gestalten Sie Ihren eigenen Softwareentwicklungsprozess (oder einen anderen Prozess), so wie `DemandAnalysis -> Coding -> Testing -> Manuelle`.
    - Phase: Gestalten Sie Ihre eigene Phase innerhalb der ChatChain, wie z.B. `DemandAnalysis`.
    - Rolle: Definieren der verschiedenen Agenten in Ihrem Unternehmen, wie der `Chief Executive Officer`.

## 🤗 Teilen Sie Ihre Software!

**Code**: Wir sind begeistert von Ihrem Interesse an der Teilnahme an unserem Open-Source-Projekt. Wenn du auf Probleme mit stößt, zögere nicht, sie zu melden. Zögern Sie nicht, einen Pull-Request zu erstellen, wenn Sie irgendwelche Anfragen haben oder wenn Sie bereit sind, Ihre Arbeit mit uns zu teilen! Ihre Beiträge sind sehr wertvoll. Bitte lass mich wissen, wenn es etwas anderes gibt, benötigst du Hilfe!

**Firma**: Erstellen Sie Ihre eigene angepasste "ChatDev Company" ist ein Kinderspiel. Dieses personalisierte Setup beinhaltet drei einfache Konfigurationsdateien für JSON. Sehen Sie sich das Beispiel im Verzeichnis `CompanyConfig/Default` an. Detaillierte Anweisungen zur Anpassung finden Sie in unserem [Wiki](wiki.md).

**Software**: Wann immer Sie mit ChatDev Software entwickeln, wird ein entsprechender Ordner mit allen wichtigen Informationen generiert. Ihre Arbeit mit uns zu teilen ist so einfach wie eine Pull-Request-Anfrage. Hier ist ein Beispiel: Führen Sie den Befehl `python3 run.py --task "design a 2048 game" --name "2048" --org "THUNLP" --config "Default"` aus. Dies wird ein Softwarepaket erstellen und einen Ordner mit dem Namen `/WareHouse/2048_THUNLP_timestamp` erzeugen. Im Inneren findest du:

- Alle Dateien und Dokumente im Zusammenhang mit der Spielsoftware 2048
- Konfigurationsdateien des für diese Software verantwortlichen Unternehmens, einschließlich der drei JSON-Konfigurationsdateien von `CompanyConfig/Default`
- Ein umfangreiches Protokoll, das den Bauprozess der Software detailliert darstellt (`timestamp.log`)
- Die erste Eingabeaufforderung, mit der diese Software erstellt wurde (`2048.prompt`)

**Schaue dir die Software [hier](Contribution.md) an!**

## 👨‍💻<unk> Mitwirkende

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

Hergestellt mit [contrib.rocks](https://contrib.rocks).
## 🔎 Zitat

```
@misc{qian2023communicative,
      title={Communicative Agents for Software Development}, 
      author={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      Jahr={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      primaryClass={cs.SE}
}
```

## ⚖️ Lizenz

- Source Code Licensing: Der Quellcode unseres Projekts ist unter der Apache 2.0 Lizenz lizenziert. Diese Lizenz erlaubt die Verwendung, Änderung und Verbreitung des Codes unter bestimmten Bedingungen der Apache 2.0-Lizenz.
- Projekt Open-Source-Status: Das Projekt ist in der Tat Open-Source; diese Bezeichnung ist jedoch in erster Linie für nicht-kommerzielle Zwecke bestimmt. Während wir die Zusammenarbeit und Beiträge der Community für Forschung und nicht-kommerzielle Anwendungen fördern Es ist wichtig zu beachten, dass jede Nutzung der Komponenten für kommerzielle Zwecke gesonderte Lizenzvereinbarungen erfordert.
- Datenlizenz: Die in unserem Projekt verwendeten Daten sind unter CC BY-NC 4.0 lizenziert. Diese Lizenz erlaubt ausdrücklich die nicht-kommerzielle Nutzung der Daten. Wir möchten betonen, dass alle Modelle, die unter Verwendung dieser Datensätze ausgebildet werden, strikt an die nicht-kommerzielle Nutzungsbeschränkung gebunden sein und ausschließlich für Forschungszwecke verwendet werden sollten.

## 🌟 Sternverlauf

[![Sternhistorie-Diagramm](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 Danksagungen

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="../misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="../misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="../misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 Kontakt

Wenn du Fragen hast, Feedback hast oder Kontakt aufnehmen möchtest, bitte zögern Sie nicht, uns per E-Mail an [chatdev zu kontaktieren. penbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
