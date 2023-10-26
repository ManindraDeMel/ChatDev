# Коммуникативные агенты для разработки программного обеспечения

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    【Английский | <a href="readme/README-Chinese.md">Китайский</a> | <a href="readme/README-Japanese.md">Японский</a> | <a href="readme/README-Korean.md">Корейский</a> | <a href="readme/README-Filipino.md">Филиппинский</a> | <a href="readme/README-French.md">Французский</a> | <a href="readme/README-Slovak.md">Словацкий</a> | <a href="readme/README-Portuguese.md">Португальский</a> | <a href="readme/README-Spanish.md">Испанский</a> | <a href="readme/README-Dutch.md">Dutch</a> | <a href="readme/README-Hindi.md">Хинди</a> <unk>
</p>
<p align="center">
    【📚 <a href="wiki.md">Wiki</a> | 🚀 <a href="wiki.md#local-demo">Местный демо</a> | 👥 <a href="Contribution.md">Сообщественное программное обеспечение</a> | 🔧 <a href="wiki.md#customization">Кастомизация</a>
</p>

## 📖 обзор

- **ChatDev** stands as a **virtual software company** that operates through various **intelligent agents** holding different roles, including Chief Executive Officer <img src='online_log/static/figures/ceo.png' height=20>, Chief Product Officer <img src='online_log/static/figures/cpo.png' height=20>, Chief Technology Officer <img src='online_log/static/figures/cto.png' height=20>, programmer <img src='online_log/static/figures/programmer.png' height=20>, reviewer <img src='online_log/static/figures/reviewer.png' height=20>, tester <img src='online_log/static/figures/tester.png' height=20>, art designer <img src='online_log/static/figures/designer.png' height=20>. These agents form a multi-agent organizational structure and are united by a mission to "revolutionize the digital world through programming." The agents within ChatDev **collaborate** by participating in specialized functional seminars, including tasks such as designing, coding, testing, and documenting.
- The primary objective of ChatDev is to offer an **easy-to-use**, **highly customizable** and **extendable** framework, which is based on large language models (LLMs) and serves as an ideal scenario for studying collective intelligence.
<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## 🎉 Новости

* **26 октября 2023: ChatDev теперь поддерживается Docker для безопасного исполнения** (благодаря вкладу от [ManindraDeMel](https://github.com/ManindraDeMel)). См. руководство по запуску [Docker Start Guide](wiki.md#docker-start).
  <p align="center">
  <img src='./misc/docker.png' width=400>
  </p>
* 25 сентября 2023 г. доступен режим **Git** , позволяющий программисту <img src='online_log/static/figures/programmer.png' height=20> использовать Git для управления версиями. Чтобы включить эту функцию, просто установите `"git_management"` на `"True"` в `ChatChainConfig.json`. See [guide](wiki.md#git-mode).
  <p align="center">
  <img src='./misc/github.png' width=600>
  </p>
* September 20th, 2023: The **Human-Agent-Interaction** mode is now available! You can get involved with the ChatDev team by playing the role of reviewer <img src='online_log/static/figures/reviewer.png' height=20> and making suggestions to the programmer <img src='online_log/static/figures/programmer.png' height=20>; try `python3 run.py --task [description_of_your_idea] --config "Human"`. See [guide](wiki.md#human-agent-interaction) and [example](WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='./misc/Human_intro.png' width=600>
  </p>
* 1 сентября 2023 года: доступен режим **Art**! Вы можете активировать дизайнерский агент <img src='online_log/static/figures/designer.png' height=20> для создания изображений, используемых в программе; попробуйте запустить `python3.py --task [description_of_your_idea] --config "Art"`. See [guide](wiki.md#art) and [example](WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28 августа 2023 года: Система доступна для общественности.
* 17 августа 2023: Версия v1.0.0 была готова к выпуску.
* 30 июля 2023 года: Пользователи могут настраивать параметры ChatChain, Phase, and Role Additionally, both online Log mode and replay mode are now supported.
* July 16th, 2023: The [preprint paper](https://arxiv.org/abs/2307.07924) associated with this project was published.
* 30 июня 2023 года: Выпущена первоначальная версия репозитория ChatDev.

## ❓ Что можно сделать ChatDev?

![интро](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡ Быстрый старт

### 🖥️ Быстрый старт с терминалом

Для начала выполните следующие действия:

1. **Клонировать репозиторий GitHub:** Начать клонирование репозитория, используя команду:
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Настройте окружение Python:** Убедитесь, что у вас есть окружение версии 3.9 или выше Python. Вы можете создать и активировать эту среду, используя следующие команды, заменив `ChatDev_conda_env` предпочитаемой окружением :
   ```
   conda создать -n ChatDev_conda_env python=3.9 -y
   консоли активировать ChatDev_conda_env
   ```
3. **Зависимости установки:** Перемещение в директорию `ChatDev` и установка необходимых зависимостей путем запуска:
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **Установить OpenAI API ключ:** Экспорт вашего OpenAI API ключа как переменной среды. Replace `"your_OpenAI_API_key"` with your actual API key. Помните, что эта переменная специфична для сессии, поэтому если откроет новый терминальный сеанс. На Unix/Linux:
   ```
   экспорт OPENAI_API_KEY="ваш_OpenAI_API_key"
   ```
   На Windows:
   ```
   $env:OPENAI_API_KEY="ваш_OpenAI_API_key"
   ```
5. **Создайте свое программное обеспечение:** Используйте следующую команду для создания вашего программного обеспечения, заменить `[description_of_your_idea]` на описание вашей идеи и `[project_name]` желаемым проектом названием: На Unix/Linux:
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   На Windows:
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Run Your Software:** Once generated, you can find your software in the `WareHouse` directory under a specific project folder, such as `project_name_DefaultOrganization_timestamp`. Запустите программное обеспечение, используя следующую команду в этой директории: On Unix/Linux:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   main.py
   ```
   На Windows:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   main.py
   ```

### 🐳 Быстрый старт с Docker
- Мы благодарим [ManindraDeMel](https://github.com/ManindraDeMel) за поддержку Docker. См. руководство по запуску [Docker Start Guide](wiki.md#docker-start).

## ✨ Расширенные навыки

For more detailed information, please refer to our [Wiki](wiki.md), where you can find:

- Введение во все параметры запуска команды.
- A straightforward guide for setting up a local web demo, which includes enhanced visualized logs, a replay demo, and a simple ChatChain Visualizer.
- An overview of the ChatDev framework.
- Полное введение ко всем расширенным параметрам в конфигурации ChatChain.
- Руководства по настройке ChatDev, включая:
    - ChatChain: Создайте свой собственный процесс разработки ПО (или любой другой процесс), Такие как `DemandAnalysis -> Coding -> Testing -> Manual`.
    - Фаза: Создайте свою собственную фазу в ChatChain, например `DemandAnalysis`.
    - Role: Defining the various agents in your company, such as the `Chief Executive Officer`.

## 🤗 Поделитесь своим ПО!

**Code**: Мы с энтузиазмом относимся к Вашему интересу к участию в нашем проекте с открытым исходным кодом. If you come across any problems, don't hesitate to report them. Feel free to create a pull request if you have any inquiries or if you are prepared to share your work with us! Ваш вклад высоко ценен. Please let me know if there's anything else you need assistance!

**Компания**: Создание собственной настраиваемой компании "ChatDev Company" является бризом. This personalized setup involves three simple configuration JSON files. Посмотрите пример каталога `CompanyConfig/Default`. For detailed instructions on customization, refer to our [Wiki](wiki.md).

**Software**: Whenever you develop software using ChatDev, a corresponding folder is generated containing all the essential information. Совместное использование вашей работы с нами так же просто, как и создание Pull request. Пример: выполните команду `python3 run.py --task "design a 2048 game" --name "2048" --org "THUNLP" --config "Default"`. This will create a software package and generate a folder named `/WareHouse/2048_THUNLP_timestamp`. Внутри вы найдете:

- Все файлы и документы, относящиеся к игровому программному обеспечению 2048 года
- Configuration files of the company responsible for this software, including the three JSON config files from `CompanyConfig/Default`
- Полноценный журнал с подробным описанием процесса создания программного обеспечения, который может быть использован для повтора (`timestamp.log`)
- Первоначальная подсказка, используемая для создания этого программного обеспечения (`2048.prompt`)

**See community contributed software [here](Contribution.md)!**

## 👨‍💻<unk> Авторы

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

Сделано из [contrib.rocks](https://contrib.rocks).
## 🔎 Цитата

```
@misc{qian2023communicative,
      title={Communicative Agents for Software Development}, 
      author={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      год={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      основной класс={cs.SE}
}
```
## ⚖️ лицензия

- Лицензирование исходного кода: Исходный код нашего проекта распространяется на условиях лицензии Apache 2.0. Эта лицензия позволяет использовать, модифицировать и распространять код с учетом определенных условий, изложенных в лицензии Apache 2.0.
- Статус проекта с открытым исходным кодом: Проект действительно является открытым исходным кодом; однако это назначение в первую очередь предназначено для некоммерческих целей. Хотя мы поощряем сотрудничество и участие сообщества в исследовательских и некоммерческих прикладных программах, Важно отметить, что любое использование компонентов проекта в коммерческих целях требует отдельных лицензионных соглашений.
- Лицензирование данных: Соответствующие данные, используемые в нашем проекте, лицензированы в соответствии с CC BY-NC 4.0. Эта лицензия разрешает некоммерческое использование данных. Мы хотели бы подчеркнуть, что любые модели, подготовленные с использованием этих наборов данных, должны строго придерживаться ограничений некоммерческого использования и должны использоваться исключительно в исследовательских целях.

## 🌟 История звёзд

[![График Истории Звёзд](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 Благодарности

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 Контакт

Если у вас есть вопросы, обратная связь или вы хотите связаться с нами, пожалуйста, не стесняйтесь связаться с нами по электронной почте на сайте [chatdev. penbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
