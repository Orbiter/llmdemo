# LLM Demo Scripts

Just a collection of tools to demonstrate free and open source tools for LLMs.

Select a LLM Model:
click on any of https://huggingface.co/spaces/lmsys/chatbot-arena-leaderboard
copy the model name and search for it PLUS „gguf“
download the gguf model file into the models subdirectory of llama.cpp (see below)

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

Run the LLM client (here SUSI):
- just doubleclick on susi_chat/chat_terminal/index.html
