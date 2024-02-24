# LLM Demo Scripts

Just a collection of tools to demonstrate free and open source tools for LLMs.

Install llama.cpp, load a LLM, run the LLM server:
```
git clone https://github.com/ggerganov/llama.cpp.git tools/llama.cpp
make -C tools/llama.cpp
curl -L -o tools/llama.cpp/models/openchat-3.5-0106.Q2_K.gguf https://huggingface.co/TheBloke/openchat-3.5-0106-GGUF/resolve/main/openchat-3.5-0106.Q2_K.gguf
tools/llama.cpp/server --host 0.0.0.0 -t 4 --port 8001 -np 4 -c 8192 -m tools/llama.cpp/models/openchat-3.5-0106.Q2_K.gguf
```

Load a LLM client:
```
git clone https://github.com/imoneoi/openchat-ui.git tools/openchat-ui
git clone https://github.com/susiai/susi_chat.git tools/susi_chat
```