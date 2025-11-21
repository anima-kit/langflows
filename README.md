# <img src="https://anima-kit.github.io/langflows/assets/langflow.svg" alt="Langflow" style="width: 32px; height: 32px; vertical-align: middle;">  Langflows

## 🔖 About This Project 

This repo demonstrates how to create various AI systems in [Langflow][langflow] with an emphasis on *local* RAG and agents. There are various JSONs that represent `flows` which can be uploaded to Langflow and used right away in the `Playground`.

This project is part of my broader goal to create tutorials and resources for building AI systems. For more details about how to use this repo and other easily digestible modules, [check it out here][animakit].

Now, let's get building!

## 🏁 Getting Started 

1.  Install [Langflow][langflow]. You can do this [many different ways][langflow-install], but I chose to `uv pip` install.
    ```
    uv venv venv
    venv/Scripts/activate
    uv pip install -U -r requirements.txt
    ```

1.  Run Langflow
    ```
    uv run langflow run
    ```

1.  Navigate to [http://localhost:7860](http://localhost:7860) to start playing.

## 📝 Example Use Cases 

I like to use *local* servers for my AI systems, so I'm pretty sure every `flow` I add here will use locally hosted LLMs, embeddings, etc. which can easily be used in Langflow.

**Setting up LLMs and Embeddings**

> My go-tos for LLMs and embeddings are [Ollama][ollama] and [LM Studio][lm-studio]. You can install the desktop version of Ollama [here][ollama-desktop] and LM Studio [here][lm-studio-install]. 

**Setting up Vectorstores and DBs**

> For document storage and query, I like to use [Milvus][milvus] or [Chroma][chroma]. When installing Langflow, Chroma is installed automatically, so there's no need for any extra installation instructions.

> If you're on Linux or Mac, you can install [Milvus Lite][milvus-lite]. However, Windows users will need to use Milvus Standalone or Milvus Distributed. See [here][milvus-install] for more details

**Setting up in Docker**

> You can also setup both Ollama and Milvus in Docker. I've included various example `docker-compose` files. For example, to build and run Milvus and Ollama with GPU support:

  ```
  docker compose -f docker-compose/milvus-ollama-gpu.yml up -d
  ```

> You can also checkout the official instructions for [Ollama][ollama-docker] and [Milvus][milvus-docker] to setup your own.

Now that everything is setup, you can upload this repo's JSONs to Langflow and test them out in the `Playground`.

<p align="center">
  <img src="https://anima-kit.github.io/langflows/assets/langflow-start.gif" alt="animated"/>
</p>

## 📚 Next Steps & Learning Resources 

This project is part of a series on building AI agents. For a deeper dive, [check out my tutorials][tutorials]. Topics include:

- Discussing various aspects of AI
- Implementing RAG techniques to accelerate document understanding
- Setting up local servers to power agents
- Example agent workflows (simple chatbots to specialized agents)

Want to learn how to expand this setup? [Visit my portfolio][animakit] to explore more tutorials and projects!

## ⚙️ Tech 

- [Chroma][chroma]: For storing and querying data
- [Docker][docker]: For containerizing LLM, embedding, and vectorstore servers
- [Langflow][langflow]: No-code to very-much-code builder for AI systems
- [LM Studio][lm-studio]: For hosting LLMs and embeddings
- [Milvus][milvus]: For storing and querying data
- [Ollama][ollama]: For hosting LLMs and embeddings

## 🔗 Contributing 

This repo is a work in progress. If you'd like to suggest or add improvements, fix bugs or typos etc., feel free to contribute. Check out the [contributing guidelines][contributing] to get started.

<!-- LINKS -->
[ak-milvus-docker]: https://github.com/anima-kit/milvus-docker/blob/main/README.md#-getting-started
[ak-ollama-docker]: https://github.com/anima-kit/ollama-docker/blob/main/README.md#-getting-started
[animakit]: http://anima-kit.github.io/
[chroma]: https://www.trychroma.com/
[contributing]: CONTRIBUTING.md
[docker]: https://www.docker.com/
[langflow]: https://www.langflow.org/
[langflow-install]: https://github.com/langflow-ai/langflow?tab=readme-ov-file#%EF%B8%8F--langflow-desktop
[lm-studio]: https://lmstudio.ai/
[lm-studio-install]: https://lmstudio.ai/download
[milvus]: https://milvus.io/
[milvus-docker]: https://milvus.io/docs/install_standalone-docker.md
[milvus-install]: https://milvus.io/docs/install-overview.md 
[milvus-lite]: https://milvus.io/docs/milvus_lite.md
[ollama]: https://www.ollama.com/
[ollama-desktop]: https://www.ollama.com/download
[ollama-docker]: https://ollama.com/blog/ollama-is-now-available-as-an-official-docker-image
[tutorials]: https://anima-kit.github.io/tutorials/