### env 
OS: Ubuntu 20.04.6 LTS

### build

```
sudo ln -s /home/xl/cuda /usr/local/cuda
sudo apt-get install libsdl2-dev

cd whisper.cpp
GGML_CUDA=1 make -j talk-llama
```
### run
```
cd whisper.cpp
./talk-llama -mw ../models/ggml-medium-q5_0.bin -ml ../models/mistral-7b-instruct-v0.2.Q3_K_L.gguf -p "bot" -t 8
```

### download models
https://huggingface.co/ggerganov/whisper.cpp/tree/main  
https://huggingface.co/TheBloke/LLaMa-13B-GGML/tree/main  
https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.2-GGUF/tree/main  
