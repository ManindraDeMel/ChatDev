# Agentes Comunicativos para Desenvolvimento de Software

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    【English | <a href="readme/README-Chinese.md">Chinese</a> | <a href="readme/README-Japanese.md">Japanese</a> | <a href="readme/README-Korean.md">Korean</a> | <a href="readme/README-Filipino.md">Filipino</a> | <a href="readme/README-French.md">French</a> | <a href="readme/README-Slovak.md">Slovak</a> | <a href="readme/README-Portuguese.md">Portuguese</a> | <a href="readme/README-Spanish.md">Spanish</a> | <a href="readme/README-Dutch.md">Dutch</a> | <a href="readme/README-Hindi.md">Hindi</a>】
</p>
<p align="center">
    【📚 <a href="wiki.md">Wiki</a> ├🚀 <a href="wiki.md#local-demo">Demo Local</a> ├👥 <a href="Contribution.md">Community Built Software</a> ├🔧 <a href="wiki.md#customization">Personalização</a>】
</p>

## 📖 Visão geral

- **ChatDev** é como uma **empresa de software virtual** que opera através de vários agentes **inteligentes** segurando funções diferentes, incluindo Diretor Executivo <img src='online_log/static/figures/ceo.png' height=20>, Diretor Geral de Produto <img src='online_log/static/figures/cpo.png' height=20>, Diretor Tecnológico <img src='online_log/static/figures/cto.png' height=20>programador <img src='online_log/static/figures/programmer.png' height=20>, revisor <img src='online_log/static/figures/reviewer.png' height=20>, testador <img src='online_log/static/figures/tester.png' height=20>, designer de arte <img src='online_log/static/figures/designer.png' height=20>. Estes agentes formam uma estrutura organizacional de vários agentes e estão unidos por uma missão de "revolucionar o mundo digital através da programação". Os agentes dentro do ChatDev **colaboram** participando de seminários funcionais especializados, incluindo tarefas como criação, codificação, testes e documentação.
- The primary objective of ChatDev is to offer an **easy-to-use**, **highly customizable** and **extendable** framework, which is based on large language models (LLMs) and serves as an ideal scenario for studying collective intelligence.
<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## 🎉 Notícias

* **October 26th, 2023: ChatDev is now supported with Docker for safe execution** (thanks to contribution from [ManindraDeMel](https://github.com/ManindraDeMel)). Please see [Docker Start Guide](wiki.md#docker-start).
  <p align="center">
  <img src='./misc/docker.png' width=400>
  </p>
* September 25th, 2023: The **Git** mode is now available, enabling the programmer <img src='online_log/static/figures/programmer.png' height=20> to utilize Git for version control. Para ativar este recurso, simplesmente defina `"git_management"` para `"True"` em `ChatChainConfig.json`. See [guide](wiki.md#git-mode).
  <p align="center">
  <img src='./misc/github.png' width=600>
  </p>
* 20 de setembro de 2023: O modo **Human-Agent-Interaction** está agora disponível! Você pode se envolver com a equipe do ChatDev desempenhando o papel de revisor <img src='online_log/static/figures/reviewer.png' height=20> e fazendo sugestões para o programador <img src='online_log/static/figures/programmer.png' height=20>; tente `python3 executar. y --task [description_of_your_idea] --config "Human"`. Consulte o [guia](wiki.md#human-agent-interaction) e [exemplo](WareHouse/Gomoku_HumanAgentInteraction_20230920135038).
  <p align="center">
  <img src='./misc/Human_intro.png' width=600>
  </p>
* 1 de Setembro de 2023: O modo **Art** está disponível agora! Você pode ativar o agente de designer <img src='online_log/static/figures/designer.png' height=20> para gerar imagens usadas no software; tente `python3 run.py --task [description_of_your_idea] --config "Art"`. Consulte o [guia](wiki.md#art) e [exemplo](WareHouse/gomokugameArtExample_THUNLP_20230831122822).
* 28 de agosto, 2023: O sistema está disponível ao público.
* 17 de agosto, 2023: A versão v1.0.0 estava pronta para o lançamento.
* 30 de julho de 2023: Os usuários podem personalizar as Configurações de ChatChain, Phase e Papel. Além disso, tanto o modo Log online quanto o modo replay são suportados.
* 16 de Julho de 2023: O papel [pré-impresso](https://arxiv.org/abs/2307.07924) associado a este projeto foi publicado.
* 30 de junho de 2023: A versão inicial do repositório do ChatDev foi lançada.

## ❓ O que pode ChatDev Do?

![Introdução](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## ⚡ Início rápido

### 🖥️ Quickstart with terminal

Para começar, siga estes passos:

1. **Clone the GitHub Repository:** Begin by cloning the repository using the command:
   ```
   git clone https://github.com/OpenBMB/ChatDev.git
   ```
2. **Configurar o ambiente Python:** Garanta que você tem a versão 3.9 ou superior ambiente Python. Você pode criar e ativar este ambiente usando os seguintes comandos, substituindo `ChatDev_conda_env` pelo nome de seu ambiente preferido :
   ```
   conda create -n ChatDev_conda_env python=3.9 -y
   conda activate ChatDev_conda_env
   ```
3. **Instale as dependências:** Ir para o diretório `ChatDev` e instale as dependências necessárias executando:
   ```
   cd ChatDev
   pip3 install -r requirements.txt
   ```
4. **Definir chave de API OpenAI:** Exportar sua chave de API OpenAI como uma variável de ambiente. Substitua `"your_OpenAI_API_key"` pela sua chave de API real. Remember that this environment variable is session-specific, so you need to set it again if you open a new terminal session. No Unix/Linux:
   ```
   Exportar OPENAI_API_KEY="sua_chave_OpenAI_API"
   ```
   No Windows:
   ```
   $env:OPENAI_API_KEY="sua_chave_OpenAI_API"
   ```
5. **Construa seu software:** Use o seguinte comando para iniciar a construção do seu software, substituindo `[description_of_your_idea]` pela descrição da sua ideia e `[project_name]` pelo nome desejado do seu projeto . No Unix/Linux:
   ```
   python3 run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
   No Windows:
   ```
   python run.py --task "[description_of_your_idea]" --name "[project_name]"
   ```
6. **Rode seu Software:** Uma vez gerado, você pode encontrar o seu software no diretório `WareHouse` sob uma pasta de projetos específica, tais como `project_name_DefaultOrganization_timestamp`. Execute seu software usando o seguinte comando dentro desse diretório: No Unix/Linux:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python3 main.py
   ```
   On Windows:
   ```
   cd WareHouse/project_name_DefaultOrganization_timestamp
   python main.py
   ```

### 🐳 Quickstart with Docker
- We thank [ManindraDeMel](https://github.com/ManindraDeMel) for providing Docker support. Please see [Docker Start Guide](wiki.md#docker-start).

## ✨ Habilidades Avançadas

Para obter informações mais detalhadas, consulte o nosso [Wiki](wiki.md), onde você pode encontrar:

- Uma introdução a todos os parâmetros de execução de comando.
- Um guia direto para a criação de uma demonstração da web local, que inclui logs aprimorados visualizados, um demo de replay e um visualizador simples de ChatChain Visualizer.
- Uma visão geral do framework Chatdev.
- Uma introdução abrangente a todos os parâmetros avançados na configuração do ChatChain.
- Guias para personalizar o ChatDev, incluindo:
    - ChatChain: Projete seu próprio processo de desenvolvimento de software (ou qualquer outro processo), como `DemandAnalysis -> Codificação -> Testando -> Manual`.
    - Fase: Projete sua própria fase dentro do ChatChain, como `DemandAnalysis`.
    - Papel: Definindo os vários agentes em sua empresa, como o `Chefe Executivo`.

## 🤗 Compartilhe seu software!

**Código**: Estamos entusiasmados com seu interesse em participar de nosso projeto de código aberto. Se você se deparar com algum problema, não hesite em denunciá-lo. Sinta-se à vontade para criar um pull request se tiver alguma dúvida ou se estiver preparado para compartilhar seu trabalho conosco! Suas contribuições são altamente valorizadas. Please let me know if there's anything else you need assistance!

**Company**: Criar sua própria "ChatDev Company" é uma brisa. Esta configuração personalizada envolve três arquivos JSON de configuração simples do . Confira o exemplo fornecido no diretório `CompanyConfig/Padrão`. Para obter instruções detalhadas do na personalização, consulte o nosso [Wiki](wiki.md).

**Software**: Whenever you develop software using ChatDev, a corresponding folder is generated containing all the essential information. Compartilhar seu trabalho conosco é tão simples quanto fazer um pull request. Here's an example: execute the command `python3 run.py --task "design a 2048 game" --name "2048"  --org "THUNLP" --config "Default"`. This will create a software package and generate a folder named `/WareHouse/2048_THUNLP_timestamp`. Lá dentro, você encontrará:

- Todos os arquivos e documentos relacionados com o software de jogo 2048
- Arquivos de configuração da empresa responsável por este software, incluindo os três arquivos de configuração JSON da `EmpresyConfig/Padrão`
- Um registro abrangente detalhando o processo de construção do software que pode ser usado para replay (`timestamp.log`)
- A prompt inicial usada para criar este software (`2048.prompt`)

**Veja o software da comunidade com [aqui](Contribution.md)!**

## 👨‍💻‍ Contributors

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

Made with [contrib.rocks](https://contrib.rocks).
## :magnifying_glass_tilted_direita: Citação

```
@misc{qian2023communicative,
      title={Communicative Agents for Software Development}, 
      author={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      ano={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      primaryClass={cs.SE}
}
```

## Licença ⚖️

- Licença do código-fonte: O código-fonte do nosso projeto é licenciado sob a licença Apache 2.0. Esta licença permite o uso, a modificação e a distribuição do código, sujeito a certas condições descritas na Licença Apache 2.0.
- Project Open-Source Status: O projeto é de fato de código aberto; no entanto, essa designação é primordialmente destinada a fins não comerciais. Embora encorajemos a colaboração e os contributos da comunidade para a investigação e aplicações não comerciais, É importante notar que qualquer utilização das componentes do projecto para fins comerciais exige acordos de autorização separados.
- Licença de Dados: Os dados relacionados utilizados em nosso projeto estão licenciados sob a CC BY-NC 4.0. Esta licença explicitamente permite o uso não comercial dos dados. Gostaríamos de salientar que quaisquer modelos formados através destes conjuntos de dados devem respeitar rigorosamente a restrição de utilização não comercial e devem ser utilizados exclusivamente para fins de investigação.

## 🌟 Histórico de Estrelas

[![Gráfico de História Estelar](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)


## 🤝 Conhecimentos

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://aibrb.com/introducing-herbie-your-super-employee-for-streamlined-productivity/"><img src="https://aibrb.com/wp-content/uploads/2023/09/Featured-on-AIBRB.com-white-1.png"  height=50pt></a>

## 📬 Contato

If you have any questions, feedback, or would like to get in touch, please feel free to reach out to us via email at [chatdev.openbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)
