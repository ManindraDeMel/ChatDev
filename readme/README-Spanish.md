# Agentes provechosos para el desarrollo de software

<p align="center">
  <img src='../misc/logo1.png' width=550>
</p>

<p align="center">
    . Inglés | <a href="readme/README-Chinese.md">chino</a> | <a href="readme/README-Japanese.md">japonés</a> | <a href="readme/README-Korean.md">coreano</a> | <a href="readme/README-Filipino.md">Filipino</a> | <a href="readme/README-French.md">francés</a> | <a href="readme/README-Slovak.md">eslovaco</a> | <a href="readme/README-Portuguese.md">portugués</a> | <a href="readme/README-Spanish.md">español</a> | <a href="readme/README-Dutch.md">holandés</a> | <a href="readme/README-Hindi.md">hindi</a>
</p>
<p align="center">
    ✫ 📚 <a href="wiki.md">Wiki</a> | 🚀 <a href="wiki.md#local-demo">Demo local</a> | 👥 <a href="Contribution.md">Software de construcción de la comunidad</a> | 🔧 <a href="wiki.md#customization">Personalización</a>
</p>

## :open_libro: Resumen

- **ChatDev** es una **compañía de software virtual** que opera a través de varios **agentes inteligentes** que tienen roles diferentes, incluido Chief Executive Officer <img src='online_log/static/figures/ceo.png' height=20>, Chief Product Officer <img src='online_log/static/figures/cpo.png' height=20>, Chief Technology Officer <img src='online_log/static/figures/cto.png' height=20>, programador <img src='online_log/static/figures/programmer.png' height=20>, revisor <img src='online_log/static/figures/reviewer.png' height=20>, tester <img src='online_log/static/figures/tester.png' height=20>, diseñador de arte <img src='online_log/static/figures/designer.png' height=20>. Estos agentes forman una estructura organizacional multiagente y están unidos por una misión de "revolucionar el mundo digital a través de la programación". Los agentes dentro de ChatDev **colaboran con** participando en seminarios funcionales especializados, incluyendo tareas como diseño, codificación, pruebas y documentación.
- The primary objective of ChatDev is to offer an **easy-to-use**, **highly customizable** and **extendable** framework, which is based on large language models (LLMs) and serves as an ideal scenario for studying collective intelligence.
<p align="center">
  <img src='../misc/company.png' width=600>
</p>

## 🎉 Noticias

* **26 de octubre de 2023: ChatDev ahora está soportado con Docker para ejecución segura** (gracias a la contribución de [ManindraDeMel](https://github.com/ManindraDeMel)). Por favor vea [Docker Start Guide](wiki.md#docker-start).
  <p align="center">
  <img src='../misc/docker.png' width=400>
  </p>
* 25 de septiembre de 2023: El modo **Git** ya está disponible, permitiendo al programador <img src='online_log/static/figures/programmer.png' height=20> utilizar Git para el control de versión. Para activar esta función, simplemente establece `"git_management"` a `"True"` en `ChatChainConfig.json`. Ver [guía](wiki.md#git-mode).
  <p align="center">
  <img src='../misc/github.png' width=600>
  </p>
* 20 de septiembre de 2023: ¡El modo **Human-Agent-Interaction** ya está disponible! Puedes involucrarte con el equipo de ChatDev jugando el rol del revisor <img src='online_log/static/figures/reviewer.png' height=20> y haciendo sugerencias al programador <img src='online_log/static/figures/programmer.png' height=20>; prueba `ejecución de python3. y --task [description_of_your_idea] --config "Human"`. Ver [guía](wiki.md#human-agent-interaction) y [ejemplo](WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='../misc/Human_intro.png' width=600>
  </p>
* 1 de septiembre de 2023: ¡El modo **Art** está disponible ahora! Puede activar el agente diseñador <img src='online_log/static/figures/designer.png' height=20> para generar imágenes usadas en el software; pruebe `python3 run.py --task [description_of_your_idea] --config "Art"`. Ver [guía](wiki.md#art) y [ejemplo](WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28 de agosto de 2023: El sistema está disponible públicamente.
* 17 de agosto de 2023: La versión v1.0.0 estaba lista para su lanzamiento.
* 30 de julio de 2023: Los usuarios pueden personalizar los ajustes de ChatChain, Fase y Role. Además, ahora se admiten tanto el modo de registro en línea como el modo de repetición .
* 16 de julio de 2023: El [papel preimpreso](https://arxiv.org/abs/2307.07924) asociado con este proyecto fue publicado.
* 30 de junio de 2023: La versión inicial del repositorio ChatDev fue lanzada.

## ❓ ¿Qué puede hacer ChatDev Do?

![intro](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡ Inicio rápido

### 🖥️ Inicio rápido con terminal

Para empezar, siga estos pasos:

1. **Clone the GitHub Repository:** Begin by cloning the repository using the command:
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Configurar Entorno Python:** Asegúrese de tener un entorno Python versión 3.9 o superior. Puedes crear y activar este entorno usando los siguientes comandos, reemplazando `ChatDev_conda_env` con tu nombre de entorno preferido:
   ```
   conda create -n ChatDev_conda_env python=3.9 -y
   conda active ChatDev_conda_env
   ```
3. **Instalar dependencias:** Mover al directorio `ChatDev` e instalar las dependencias necesarias ejecutando:
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **Establezca la clave API OpenAI:** Exporte su clave OpenAI API como una variable de entorno. Reemplaza `"tu_OpenAI_API_key"` por tu clave API real. Remember that this environment variable is session-specific, so you need to set it again if you open a new terminal session. En Unix/Linux:
   ```
   export OPENAI_API_KEY="your_OpenAI_API_key"
   ```
   En Windows:
   ```
   $env:OPENAI_API_KEY="su_clave de OpenAI_API_"
   ```
5. **Construir su Software:** Utilice el siguiente comando para iniciar la construcción de su software, reemplazando `[description_of_your_idea]` con la descripción de tu idea y `[project_name]` con el nombre de tu proyecto deseado : en Unix/Linux:
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   En Windows:
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Ejecuta tu Software:** Una vez generado, puedes encontrar tu software en el directorio `WareHouse` en una carpeta específica de proyecto , tal como `project_name_DefaultOrganization_timestamp`. Ejecute su software usando el siguiente comando dentro de ese directorio: en Unix/Linux:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   En Windows:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 Comenzar rápidamente con Docker
- Damos las gracias a [ManindraDeMel](https://github.com/ManindraDeMel) por proporcionar apoyo a Docker. Por favor vea [Docker Start Guide](wiki.md#docker-start).

## ✨ Habilidades Avanzadas

Para obtener información más detallada, consulta nuestra [Wiki](wiki.md), donde puedes encontrar:

- Una introducción a todos los parámetros de ejecución del comando.
- Una guía directa para configurar una demostración web local, que incluye registros visualizados mejorados, una demostración de repetición y un simple Visualizador de ChatChain .
- Una visión general del framework ChatDev.
- Una introducción completa a todos los parámetros avanzados en la configuración de ChatChain.
- Guías para personalizar ChatDev, incluyendo:
    - ChatChain: Diseña tu propio proceso de desarrollo de software (o cualquier otro proceso), tal as `DemandAnalysis -> Coding -> Testing -> Manual`.
    - Fase: Diseña tu propia fase dentro de ChatChain, como `DemandAnalysis`.
    - Rol: Definición de los diversos agentes de su empresa, como el `Director Ejecutivo`.

## 🤗 ¡Comparte tu software!

**Código**: Somos entusiasmados con su interés en participar en nuestro proyecto de código abierto. If you come across any problems, don't hesitate to report them. Siéntete libre de crear un pull request si tienes alguna consulta o si estás preparado para compartir tu trabajo con nosotros! Sus contribuciones son muy valiosas. ¡Por favor, házmelo saber si hay algo más que necesitas ayuda!

**Empresa**: Crear tu propia "Empresa ChatDev" personalizada es una brisa. Esta configuración personalizada involucra tres archivos simple de configuración JSON. Revisa el ejemplo proporcionado en el directorio `CompanyConfig/Default`. Para instrucciones detalladas sobre personalización, consulte nuestra [Wiki](wiki.md).

**Software**: Siempre que desarrolle software usando ChatDev, se genera una carpeta correspondiente que contiene toda la información esencial . Compartir tu trabajo con nosotros es tan sencillo como hacer un pull request. Aquí hay un ejemplo: ejecutar el comando `python3 run.py --task "diseñar un juego 2048" --name "2048" --org "THUNLP" --config "Default"`. This will create a software package and generate a folder named `/WareHouse/2048_THUNLP_timestamp`. Dentro encontrará:

- Todos los archivos y documentos relacionados con el software de juego 2048
- Archivos de configuración de la empresa responsable de este software, incluyendo los tres archivos de configuración JSON de `CompanyConfig/Default`
- Un registro completo que detalla el proceso de construcción del software que puede utilizarse para repetirse (`timestamp.log`)
- El indicador inicial utilizado para crear este software (`2048.prompt`)

**¡Mira el software aportado por la comunidad [aquí](Contribution.md)!**

## 👨‍💻► Colaboradores

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

Hecho con [contrib.rocks](https://contrib.rocks).
## 🔎 Citación

```
@misc{qian2023communicative,
      title={Communicative Agents for Software Development} 
      autor={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      año={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      primaryClass={cs.SE}
}
```

## ⚖️ Licencia

- Licencia de código fuente: El código fuente de nuestro proyecto está bajo la licencia Apache 2.0. Esta licencia permite el uso, modificación y distribución del código, sujeto a ciertas condiciones descritas en la Licencia Apache 2.0.
- Estado de Código Abierto del Proyecto: El proyecto es de código abierto; sin embargo, este diseño está destinado principalmente a fines no comerciales. Mientras fomentamos la colaboración y las contribuciones de la comunidad para la investigación y aplicaciones no comerciales, es importante señalar que cualquier utilización de los componentes del proyecto para fines comerciales necesita acuerdos de licencia separados.
- Licencia de datos: Los datos relacionados utilizados en nuestro proyecto están licenciados bajo CC BY-NC 4.0. Esta licencia permite explícitamente el uso no comercial de los datos. Queremos subrayar que cualquier modelo capacitado con estos conjuntos de datos debe respetar estrictamente las restricciones de uso no comercial y debe emplearse exclusivamente para fines de investigación.

## 🌟 Historial de estrellas

[![Gráfico Historial de Estrellas](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 Reconocimientos

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 Contacto

Si tienes alguna pregunta, comentario o quieres ponerte en contacto, por favor no dudes en contactarnos por correo electrónico a [chatdev. penbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
