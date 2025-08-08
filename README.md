
<p align="left">
    <a href="README_CN.md">中文</a>&nbsp ｜ English</a>
</p>
<br><br>

<p align="center">
 <img src="https://dscache.tencent-cloud.cn/upload/uploader/hunyuan-64b418fd052c033b228e04bc77bbc4b54fd7f5bc.png" width="400"/> <br>
</p><p></p>


<p align="center">
    🤗&nbsp;<a href="https://huggingface.co/tencent/"><b>Hugging Face</b></a>&nbsp;&nbsp;|&nbsp;&nbsp;
    <img src="https://avatars.githubusercontent.com/u/109945100?s=200&v=4" width="16"/>&nbsp;<a href="https://modelscope.cn/models/Tencent-Hunyuan/Hunyuan-A13B-Instruct"><b>ModelScope</b></a>&nbsp;&nbsp;|&nbsp;&nbsp;
<img src="https://cdn-avatars.huggingface.co/v1/production/uploads/6594d0c6c5f1cd69a48b261d/04ZNQlAfs08Bfg4B1o3XO.png" width="14"/>&nbsp;<a href="https://github.com/Tencent/AngelSlim/tree/main"><b>AngelSlim</b></a>
</p>

<p align="center">
    🖥️&nbsp;<a href="https://hunyuan.tencent.com" style="color: red;"><b>Official Website</b></a>&nbsp;&nbsp;|&nbsp;&nbsp;
    🕖&nbsp;<a href="https://cloud.tencent.com/product/hunyuan"><b>HunyuanAPI</b></a>&nbsp;&nbsp;|&nbsp;&nbsp;
    🕹️&nbsp;<a href="https://hunyuan.tencent.com/"><b>Demo</b></a>&nbsp;&nbsp;&nbsp;&nbsp;
</p>

<p align="center">
    <a href="https://github.com/Tencent-Hunyuan/Hunyuan-7B"><b>GITHUB</b></a> | 
    <a href="https://cnb.cool/tencent/hunyuan/Hunyuan-7B"><b>cnb.cool</b></a> | 
    <a href="https://github.com/Tencent-Hunyuan/Hunyuan-7B/blob/main/LICENSE"><b>LICENSE</b></a>
</p>


## Model Introduction

Hunyuan is Tencent's open-source efficient large language model series, designed for versatile deployment across diverse computational environments. From edge devices to high-concurrency production systems, these models deliver optimal performance with advanced quantization support and ultra-long context capabilities.

We have released a series of Hunyuan dense models, comprising both pre-trained and instruction-tuned variants, with parameter scales of 0.5B, 1.8B, 4B, and 7B. These models adopt training strategies similar to the Hunyuan-A13B, thereby inheriting its robust performance characteristics. This comprehensive model family enables flexible deployment optimization - from resource-constrained edge computing with smaller variants to high-throughput production environments with larger models, all while maintaining strong capabilities across diverse scenarios.

### Key Features and Advantages

- **Hybrid Reasoning Support**: Supports both fast and slow thinking modes, allowing users to flexibly choose according to their needs.
- **Ultra-Long Context Understanding**: Natively supports a 256K context window, maintaining stable performance on long-text tasks.
- **Enhanced Agent Capabilities**: Optimized for agent tasks, achieving leading results on benchmarks such as BFCL-v3, τ-Bench and C3-Bench.
- **Efficient Inference**: Utilizes Grouped Query Attention (GQA) and supports multiple quantization formats, enabling highly efficient inference.

## Related News
* 2025.7.30 We have open-sourced  **Hunyuan-0.5B-Pretrain** , **Hunyuan-1.8B-Pretrain** , **Hunyuan-4B-Pretrain** , **Hunyuan-7B-Pretrain** , **Hunyuan-0.5B-Instruct** , **Hunyuan-1.8B-Instruct** , **Hunyuan-4B-Instruct** , **Hunyuan-7B-Instruct** on Hugging Face.
<br>


## Benchmark

Note: The following benchmarks are evaluated by TRT-LLM-backend on several **base models**. 

| Model            | Hunyuan-0.5B-Pretrain | Hunyuan-1.8B-Pretrain | Hunyuan-4B-Pretrain | Hunyuan-7B-Pretrain|
|:------------------:|:---------------:|:--------------:|:-------------:|:---------------:|
| MMLU             | 54.02          | 64.62         | 74.01        | 79.82         |
| MMLU-Redux              |  54.72         | 64.42        | 73.53       | 79         |
| MMLU-Pro        | 31.15             | 38.65            | 51.91        | 57.79          |
| SuperGPQA    |  17.23         | 24.98          | 27.28           | 30.47          |
| BBH       | 45.92          | 74.32         | 75.17        | 82.95          |
| GPQA             | 27.76             | 35.81            | 43.52        | 44.07          |
| GSM8K | 55.64             | 77.26            | 87.49       | 88.25         |
| MATH             | 42.95          | 62.85          | 72.25        | 74.85          |
| EvalPlus             | 39.71          | 60.67          | 67.76        | 66.96          |
| MultiPL-E            | 21.83          | 45.92         | 59.87        | 60.41          |
| MBPP            | 43.38          | 66.14         | 76.46        | 76.19          |
| CRUX-O         | 30.75             | 36.88           | 56.5        | 60.75          |
| Chinese SimpleQA            | 12.51             | 22.31            | 30.53        | 38.86          |
| simpleQA (5shot)            | 2.38             | 3.61            | 4.21        | 5.69          |


| Topic               |                        Bench                         | Hunyuan-0.5B-Instruct | Hunyuan-1.8B-Instruct | Hunyuan-4B-Instruct | Hunyuan-7B-Instruct|
|:-------------------:|:----------------------------------------------------:|:-------------:|:------------:|:-----------:|:---------------------:|
| **Mathematics**     |            AIME 2024<br>AIME 2025<br>MATH            | 17.2<br>20<br>48.5 | 56.7<br>53.9<br>86 | 78.3<br>66.5<br>92.6 | 81.1<br>75.3<br>93.7 |
| **Science**         |            GPQA-Diamond<br>OlympiadBench             | 23.3<br>29.6 | 47.2<br>63.4 | 61.1<br>73.1 | 60.1<br>76.5 |
| **Coding**          |           Livecodebench<br>Fullstackbench            | 11.1<br>20.9 | 31.5<br>42   | 49.4<br>54.6 | 57<br>56.3 |
| **Reasoning**       |              BBH<br>DROP<br>ZebraLogic               | 40.3<br>52.8<br>34.5 | 64.6<br>76.7<br>74.6 | 83<br>78.2<br>83.5 | 87.8<br>85.9<br>85.1 |
| **Instruction<br>Following** |        IF-Eval<br>SysBench                  | 49.7<br>28.1 | 67.6<br>55.5 | 76.6<br>68 | 79.3<br>72.7 |
| **Agent**           | BFCL v3<br> τ-Bench<br>ComplexFuncBench<br> C3-Bench | 49.8<br>14.4<br>13.9<br>45.3 | 58.3<br>18.2<br>22.3<br>54.6 | 67.9<br>30.1<br>26.3<br>64.3 | 70.8<br>35.3<br>29.2<br>68.5 |
| **Long<br>Context** | PenguinScrolls<br>longbench-v2<br>FRAMES          | 53.9<br>34.7<br>41.9 | 73.1<br>33.2<br>55.6 | 83.1<br>44.1<br>79.2 | 82<br>43<br>78.6 |


&nbsp;

### Use with transformers
First, please install transformers. We will merge it into the main branch later.
```SHELL
pip install git+https://github.com/huggingface/transformers@4970b23cedaf745f963779b4eae68da281e8c6ca
```
Our model defaults to using slow-thinking reasoning, and there are two ways to disable CoT reasoning. 
1. Pass **"enable_thinking=False"** when calling apply_chat_template.
2. Adding **"/no_think"** before the prompt will force the model not to use perform CoT reasoning. Similarly, adding **"/think"** before the prompt will force the model to perform CoT reasoning.

The following code snippet shows how to use the transformers library to load and apply the model. It also demonstrates how to enable and disable the reasoning mode , and how to parse the reasoning process along with the final output.

we use tencent/Hunyuan-7B-Instruct for example

```python
from transformers import AutoModelForCausalLM, AutoTokenizer
import os
import re

model_name_or_path = "tencent/Hunyuan-7B-Instruct"

tokenizer = AutoTokenizer.from_pretrained(model_name_or_path)
model = AutoModelForCausalLM.from_pretrained(model_name_or_path, device_map="auto")  # You may want to use bfloat16 and/or move to GPU here
messages = [
    {"role": "user", "content": "Write a short summary of the benefits of regular exercise"},
]
tokenized_chat = tokenizer.apply_chat_template(messages, tokenize=True, add_generation_prompt=True,return_tensors="pt",
                                                enable_thinking=True # Toggle thinking mode (default: True)
                                                )
                                                
outputs = model.generate(tokenized_chat.to(model.device), max_new_tokens=2048)

output_text = tokenizer.decode(outputs[0])
print("output_text=",output_text)
think_pattern = r'<think>(.*?)</think>'
think_matches = re.findall(think_pattern, output_text, re.DOTALL)

answer_pattern = r'<answer>(.*?)</answer>'
answer_matches = re.findall(answer_pattern, output_text, re.DOTALL)

think_content = [match.strip() for match in think_matches][0]
answer_content = [match.strip() for match in answer_matches][0]
print(f"thinking_content:{think_content}\n\n")
print(f"answer_content:{answer_content}\n\n")


```

We recommend using the following set of parameters for inference. Note that our model does not have the default system_prompt.

```json

{
  "do_sample": true,
  "top_k": 20,
  "top_p": 0.8,
  "repetition_penalty": 1.05,
  "temperature": 0.7
}
```

&nbsp;

### Training Data Format

If you need to fine-tune our Instruct model, we recommend processing the data into the following format, corresponding to both slow-thinking and fast-thinking scenarios.

```python
# think_pattern
think = ""
answer = ""
think_pattern = f"<think>\n{think}\n</think>\n<answer>\n{answer}\n</answer>"

# fast think pattern
messages = [
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "/no_think海水为什么是咸的" },
    {"role": "assistant", "content": "<think>\n\n</think>\n<answer>\n海水是咸的主要是因为其中含有许多溶解在水中的盐类和矿物质。这些盐类和矿物质来自于地球表面的岩石和土壤中的化学物质，随着时间的推移，它们被带到了海洋中。当海水蒸发时，水分蒸发掉了，但盐类和矿物质仍然留在水中，导致海水变得更加咸味。因此，海水的咸度是由其中的盐类和矿物质的含量决定的。\n</answer>"}
]

# slow think pattern
messages = [
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "1+1=" },
    {"role": "assistant", "content": "<think>\n嗯，用户问的是1加1等于多少。首先，我需要确认这是一个基本的算术问题。1加1在十进制的数学体系中，通常的结果是2。不过，可能需要考虑是否有其他情况，比如二进制或者其他数制，但用户没有特别说明，所以默认应该是十进制。另外，有时候可能会有脑筋急转弯的情况，比如在某些语境下1+1可能等于1（比如1滴水加1滴水还是1滴水），但通常数学问题中都是2。所以最准确的回答应该是2。</think>\n<answer>\n在十进制的基本算术运算中，1加1的结果是2。这是数学中最基础的加法运算之一，遵循自然数的加法规则。因此，1 + 1 = 2。\n</answer>"}
]

from transformers import AutoTokenizer
tokenizer = AutoTokenizer.from_pretrained("your_tokenizer_path", trust_remote_code=True)
train_ids = tokenizer.apply_chat_template(messages)
```

&nbsp;

### Train with LLaMA-Factory

In the following chapter, we will introduce how to use `LLaMA-Factory` to fine-tune the `Hunyuan` model.

#### Prerequisites

Verify installation of the following dependencies:  
- **LLaMA-Factory**: Follow [official installation guide](https://github.com/hiyouga/LLaMA-Factory)
- **DeepSpeed** (optional): Follow [official installation guide](https://github.com/deepspeedai/DeepSpeed#installation)
- **Transformer Library**: Use the companion branch (Hunyuan-submitted code is pending review)
    ```
    pip install git+https://github.com/huggingface/transformers@4970b23cedaf745f963779b4eae68da281e8c6ca
    ```

#### Data preparation

We need to prepare a custom dataset:
1. Organize your data in `json` format and place it in the `data` directory in `LLaMA-Factory`. The current implementation uses the `sharegpt` dataset format, which requires the following structure:
```
[
  {
    "messages": [
      {
        "role": "system",
        "content": "System prompt (optional)"
      },
      {
        "role": "user",
        "content": "Human instruction"
      },
      {
        "role": "assistant",
        "content": "Model response"
      }
    ]
  }
]
```
Refer to the [Data Format](#training-data-format) section mentioned earlier for details.

2. Define your dataset in the data/dataset_info.json file using the following format:
```
"dataset_name": {
  "file_name": "dataset.json",
  "formatting": "sharegpt",
  "columns": {
    "messages": "messages"
  },
  "tags": {
    "role_tag": "role",
    "content_tag": "content",
    "user_tag": "user",
    "assistant_tag": "assistant",
    "system_tag": "system"
  }
}
```

#### Training execution

1. Copy all files from the `train/llama_factory_support/example_configs` directory to the `example/hunyuan` directory in `LLaMA-Factory`.
2. Modify the model path and dataset name in the configuration file `hunyuan_full.yaml`. Adjust other configurations as needed:
```
### model
model_name_or_path: [!!!add the model path here!!!]

### dataset
dataset: [!!!add the dataset name here!!!]
```
3. Execute training commands:
    *​​Single-node training​​
    Note: Set the environment variable DISABLE_VERSION_CHECK to 1 to avoid version conflicts.
    ```
    export DISABLE_VERSION_CHECK=1
    llamafactory-cli train examples/hunyuan/hunyuan_full.yaml
    ```
    *Multi-node training​​
    Execute the following command on each node. Configure NNODES, NODE_RANK, MASTER_ADDR, and MASTER_PORT according to your environment:
    ```
    export DISABLE_VERSION_CHECK=1
    FORCE_TORCHRUN=1 NNODES=${NNODES} NODE_RANK=${NODE_RANK} MASTER_ADDR=${MASTER_ADDR} MASTER_PORT=${MASTER_PORT} \
    llamafactory-cli train examples/hunyuan/hunyuan_full.yaml
    ```

&nbsp;


## Quantization Compression
We used our own [AngleSlim](https://github.com/tencent/AngelSlim) compression tool to produce FP8 and INT4 quantization models. `AngleSlim` is a toolset dedicated to creating a more user-friendly, comprehensive and efficient model compression solution.

### FP8 Quantization
We use FP8-static quantization, FP8 quantization adopts 8-bit floating point format, through a small amount of calibration data (without training) to pre-determine the quantization scale, the model weights and activation values will be converted to FP8 format, to improve the inference efficiency and reduce the deployment threshold. We you can use AngleSlim quantization, you can also directly download our quantization completed open source model to use [LINK](https://huggingface.co/).

### Int4 Quantization
We use the GPTQ and AWQ algorithm to achieve W4A16 quantization.

GPTQ processes the model weights layer by layer, uses a small amount of calibration data to minimize the reconfiguration error of the quantized weights, and adjusts the weights layer by layer by the optimization process of approximating the Hessian inverse matrix. The process eliminates the need to retrain the model and requires only a small amount of calibration data to quantize the weights, improving inference efficiency and lowering the deployment threshold. 
AWQ using a small amount of calibration data (without the need for training), the amplitude of the activation values is statistically calculated. For each weight channel, a scaling coefficient s is computed to expand the numerical range of important weights, allowing more information to be retained during quantization.

You can use  [AngleSlim](https://github.com/tencent/AngelSlim) quantization, you can also directly download our quantization completed open source model to use [LINK](https://huggingface.co/).



#### Quantization Benchmark
This subsection describes the Benchmark metrics for the Hunyuan quantitative model.

|     Bench     |           Quantization            |    Hunyuan-0.5B-Instruct     |     Hunyuan-1.8B-Instruct      |     Hunyuan-4B-Instruct      |     Hunyuan-7B-Instruct      |
|:-------------:|:---------------------------------:|:----------------------------:|:------------------------------:|:----------------------------:|:----------------------------:|
|     DROP      | B16<br>FP8<br>Int4GPTQ<br>Int4AWQ | 52.8<br>51.6<br>50.9<br>48.9 |  76.7<br>75.1<br>73.0<br>71.7  | 78.2<br>78.3<br>78.1<br>78.2 | 85.9<br>86.0<br>85.7<br>85.9 |
| GPQA-Diamond  | B16<br>FP8<br>Int4GPTQ<br>Int4AWQ | 23.3<br>22.5<br>23.3<br>23.3 | 47.2<br>47.7<br>44.43<br>43.62 |  61.1<br>60.2<br>58.1<br>-   | 60.1<br>60.1<br>60.0<br>60.1 |
| OlympiadBench | B16<br>FP8<br>Int4GPTQ<br>Int4AWQ | 29.6<br>29.6<br>26.8<br>26.3 |  63.4<br>62.5<br>60.9<br>61.7  | 73.1<br>73.1<br>71.1<br>71.2 | 76.5<br>76.6<br>76.2<br>76.4 |
|   AIME 2024   | B16<br>FP8<br>Int4GPTQ<br>Int4AWQ |    17.2<br>17.2<br>-<br>-    |    56.7<br>55.17<br>-<br>-     |    78.3<br>76.6<br>-<br>-    | 81.1<br>80.9<br>81.0<br>80.9 |


## Deployment   

For deployment, you can use frameworks such as **TensorRT-LLM**, **vLLM**, or **SGLang** to serve the model and create an OpenAI-compatible API endpoint.

image: https://hub.docker.com/r/hunyuaninfer/hunyuan-7B/tags 


### TensorRT-LLM

#### Docker Image 

We provide a pre-built Docker image based on the latest version of TensorRT-LLM.

We use tencent/Hunyuan-7B-Instruct for example
- To get started:

https://hub.docker.com/r/hunyuaninfer/hunyuan-large/tags 

```
docker pull hunyuaninfer/hunyuan-7B:hunyuan-moe-7B-trtllm
```
```
docker run --privileged --user root --name hunyuanLLM_infer --rm -it --ipc=host --ulimit memlock=-1 --ulimit stack=67108864 --gpus=all hunyuaninfer/hunyuan-7B:hunyuan-moe-7B-trtllm
```

- Prepare Configuration file:

```
cat >/path/to/extra-llm-api-config.yml <<EOF
use_cuda_graph: true
cuda_graph_padding_enabled: true
cuda_graph_batch_sizes:
- 1
- 2
- 4
- 8
- 16
- 32
print_iter_log: true
EOF
```


- Start the API server:


```
trtllm-serve \
  /path/to/HunYuan-moe-7B \
  --host localhost \
  --port 8000 \
  --backend pytorch \
  --max_batch_size 32 \
  --max_num_tokens 16384 \
  --tp_size 2 \
  --kv_cache_free_gpu_memory_fraction 0.6 \
  --trust_remote_code \
  --extra_llm_api_options /path/to/extra-llm-api-config.yml
```


### vllm

#### Start
Please use vLLM version v0.10.0 or higher for inference.

We use tencent/Hunyuan-7B-Instruct for example
- Download Model file: 
  - Huggingface:  will download automicly by vllm.
  - ModelScope: `modelscope download --model Tencent-Hunyuan/Hunyuan-7B-Instruct`
  
- model download by huggingface:
```shell
export MODEL_PATH=tencent/Hunyuan-7B-Instruct
``` 

- model downloaded by modelscope:
```shell
export MODEL_PATH=/root/.cache/modelscope/hub/models/Tencent-Hunyuan/Hunyuan-7B-Instruct/
```

- Start the API server:

```shell
python3 -m vllm.entrypoints.openai.api_server \
    --host 0.0.0.0 \
    --port 8000 \
    --trust-remote-code \
    --model ${MODEL_PATH} \
    --tensor-parallel-size 1 \
    --dtype bfloat16 \
    --quantization experts_int8 \
    --served-model-name hunyuan \
    2>&1 | tee log_server.txt
``` 
- After running service script successfully, run the request script
```shell
curl http://0.0.0.0:8000/v1/chat/completions -H 'Content-Type: application/json' -d '{
"model": "hunyuan",
"messages": [
    {
        "role": "system",
        "content": [{"type": "text", "text": "You are a helpful assistant."}]
    },
    {
        "role": "user",
        "content": [{"type": "text", "text": "请按面积大小对四大洋进行排序，并给出面积最小的洋是哪一个？直接输出结果。"}]
    }
],
"max_tokens": 2048,
"temperature":0.7,
"top_p": 0.6,
"top_k": 20,
"repetition_penalty": 1.05,
"stop_token_ids": [127960]
}'
```
#### Quantitative model deployment
This section describes the process of deploying a post-quantization model using vLLM.

Default server in BF16.

##### Int8 quantitative model deployment
Deploying the Int8-weight-only version of the HunYuan-7B model only requires setting the environment variables

Next we start the Int8 service. Run:
```shell
python3 -m vllm.entrypoints.openai.api_server \
    --host 0.0.0.0 \
    --port 8000 \
    --trust-remote-code \
    --model ${MODEL_PATH} \
    --tensor-parallel-size 1 \
    --dtype bfloat16 \
    --served-model-name hunyuan \
    --quantization experts_int8 \
    2>&1 | tee log_server.txt
```


##### Int4 quantitative model deployment
Deploying the Int4-weight-only version of the HunYuan-7B model only requires setting the environment variables , using the GPTQ method
```shell
export MODEL_PATH=PATH_TO_INT4_MODEL
```
Next we start the Int4 service. Run
```shell
python3 -m vllm.entrypoints.openai.api_server \
    --host 0.0.0.0 \
    --port 8000 \
    --trust-remote-code \
    --model ${MODEL_PATH} \
    --tensor-parallel-size 1 \
    --dtype bfloat16 \
    --served-model-name hunyuan \
    --quantization gptq_marlin \
    2>&1 | tee log_server.txt
```

##### FP8 quantitative model deployment
Deploying the W8A8C8 version of the HunYuan-7B model only requires setting the environment variables


Next we start the FP8 service. Run
```shell
python3 -m vllm.entrypoints.openai.api_server \
    --host 0.0.0.0 \
    --port 8000 \
    --trust-remote-code \
    --model ${MODEL_PATH} \
    --tensor-parallel-size 1 \
    --dtype bfloat16 \
    --served-model-name hunyuan \
    --kv-cache-dtype fp8 \
    2>&1 | tee log_server.txt
```




### SGLang

#### Docker Image 

We also provide a pre-built Docker image based on the latest version of SGLang.

We use tencent/Hunyuan-7B-Instruct for example

To get started:

- Pull the Docker image

```
docker pull lmsysorg/sglang:latest
```

- Start the API server:

```
docker run --entrypoint="python3" --gpus all \
    --shm-size 32g \
    -p 30000:30000 \
    --ulimit nproc=10000 \
    --privileged \
    --ipc=host \
     lmsysorg/sglang:latest \
    -m sglang.launch_server --model-path hunyuan/huanyuan_7B --tp 4 --trust-remote-code --host 0.0.0.0 --port 30000
```

## Community Resources

- [Hunyuan-7B Quick Start on CNB](https://cnb.cool/tencent/hunyuan/examples/Hunyuan-7B-Instruct-quick-start)

## Contact Us

If you would like to leave a message for our R&D and product teams, Welcome to contact our open-source team . You can also contact us via email (hunyuan_opensource@tencent.com).
