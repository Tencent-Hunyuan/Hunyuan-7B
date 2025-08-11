<p align="left">
   <a href="README.md">English</a>  ｜ 中文</a>&nbsp
</p>
<br><br>

<p align="center">
 <img src="https://dscache.tencent-cloud.cn/upload/uploader/hunyuan-64b418fd052c033b228e04bc77bbc4b54fd7f5bc.png" width="400"/> <br>
</p><p></p>


<p align="center">
    🤗&nbsp;<a href="https://huggingface.co/tencent/"><b>Hugging Face</b></a>&nbsp;&nbsp;|&nbsp;&nbsp;
    <img src="https://avatars.githubusercontent.com/u/109945100?s=200&v=4" width="16"/>&nbsp;<a href="https://modelscope.cn/models/Tencent-Hunyuan/"><b>ModelScope</b></a>&nbsp;&nbsp;|&nbsp;&nbsp;
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




## 模型介绍

混元是腾讯开源的高效大语言模型系列，专为多样化计算环境中的灵活部署而设计。从边缘设备到高并发生产系统，这些模型凭借先进的量化支持和超长上下文能力，在各种场景下都能提供最优性能。

我们发布了一系列混元稠密模型，包括预训练和指令微调两种变体，参数规模涵盖0.5B、1.8B、4B和7B。这些模型采用了与混元-A13B相似的训练策略，因此继承了其强大的性能特征。这个全面的模型家族支持灵活的部署优化 - 从使用小尺寸的模型适配资源受限边缘计算场景，到使用较大尺寸的高性能模型支持高并发低延迟的复杂推理生产环境，在各种场景下都能保持强大的能力。


### 核心特性与优势
- ​**混合推理支持**​：同时支持快思考和慢思考两种模式，支持用户灵活选择
- ​**超长上下文理解**​：原生支持256K上下文窗口，在长文本任务中保持稳定性能
- ​**增强Agent能力**​：优化Agent能力，在BFCL-v3、τ-Bench、C3-Bench等智能体基准测试中领先
- ​**高效推理**​：采用分组查询注意力（GQA）策略，支持多量化格式，实现高效推理

## 新闻
<br>

* 2025.7.30 我们在Hugging Face开源了 **Hunyuan-0.5B-Pretrain** , **Hunyuan-1.8B-Pretrain** , **Hunyuan-4B-Pretrain** , **Hunyuan-7B-Pretrain** , **Hunyuan-0.5B-Instruct** , **Hunyuan-1.8B-Instruct** , **Hunyuan-4B-Instruct** , **Hunyuan-7B-Instruct**。

## Benchmark评估榜单
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

## 使用 transformers 推理
首先，需要安装指定版本的transformers，我们将在不久后完成对transformers主分支的合入
```SHELL
pip install git+https://github.com/huggingface/transformers@4970b23cedaf745f963779b4eae68da281e8c6ca
```
我们的模型默认使用慢思考进行推理，有两种方法可以禁用 CoT 推理。

1. 调用 apply_chat_template 时传递 **enable_thinking=False**。
2. 在 prompt 前添加 **/no_think** 将会强制模型不使用 CoT 推理。同理，在 prompt 前添加 **/think** 将会强制模型执行 CoT 推理。

以下代码片段展示了如何使用 transformers 库加载和使用模型。它还演示了如何禁用推理模式，以及如何解析出“推理过程”和“最终输出”。

```python
from transformers import AutoModelForCausalLM, AutoTokenizer
import os
import re

model_name_or_path = os.environ['MODEL_PATH']
# model_name_or_path = "tencent/Hunyuan-7B-Instruct"

tokenizer = AutoTokenizer.from_pretrained(model_name_or_path, trust_remote_code=True)
model = AutoModelForCausalLM.from_pretrained(model_name_or_path, device_map="auto",trust_remote_code=True)  # You may want to use bfloat16 and/or move to GPU here
messages = [
    {"role": "user", "content": "Write a short summary of the benefits of regular exercise"},
]
tokenized_chat = tokenizer.apply_chat_template(
    messages,
    tokenize=False
    add_generation_prompt=True,
    enable_thinking=True
)

model_inputs = tokenizer([text], return_tensors="pt").to(model.device)
model_inputs.pop("token_type_ids", None)
outputs = model.generate(**model_inputs, max_new_tokens=4096)
output_text = tokenizer.decode(outputs[0])

think_pattern = r'<think>(.*?)</think>'
think_matches = re.findall(think_pattern, output_text, re.DOTALL)

answer_pattern = r'<answer>(.*?)</answer>'
answer_matches = re.findall(answer_pattern, output_text, re.DOTALL)

think_content = [match.strip() for match in think_matches][0]
answer_content = [match.strip() for match in answer_matches][0]
print(f"thinking_content:{think_content}\n\n")
print(f"answer_content:{answer_content}\n\n")
```


我们推荐使用下面这组参数进行推理。注意，我们的模型没有默认 system_prompt。

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

## 训练数据格式处理

如果需要微调我们的 Instruct 模型，建议将数据处理成以下格式，分别对应慢思考和快思考的场景。

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

## 使用 LLaMA-Factory 训练

我们将介绍如何使用`LLaMA-Factory`来进行微调混元模型。

### 安装环境

开始之前，确保你已经安装了以下代码库：
1. 使用[LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory)官方指导进行安装。
2. 使用[DeepSpeed](https://github.com/deepspeedai/DeepSpeed#installation)官方指导进行安装（可选）。
3. 安装配套的transformer库。当前混元提交的transformer代码正在评审中，需要获取配套的分支。
```
pip install git+https://github.com/huggingface/transformers@4970b23cedaf745f963779b4eae68da281e8c6ca
```

### 准备数据

我们需要准备自定义的数据集：

1. 请将您的数据以`json`格式进行组织，并将数据放入`LLaMA-Factory`的`data`目录中。当前使用的是`sharegpt`格式的数据集，需要遵循以下格式：
```
[
  {
    "messages": [
      {
        "role": "system",
        "content": "系统提示词（选填）"
      },
      {
        "role": "user",
        "content": "人类指令"
      },
      {
        "role": "assistant",
        "content": "模型回答"
      }
    ]
  }
]
```
可以参考前面章节中对[数据格式](#训练数据格式处理)的说明。

2. 在`data/dataset_info.json`文件中提供您的数据集定义，并采用以下格式：
```
"数据集名称": {
  "file_name": "data.json",
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

### 训练

1. 将`llama_factory_support/example_configs`目录下的文件都拷贝到`LLaMA-Factory`的`example/hunyuan`目录下。
2. 修改配置文件`hunyuan_full.yaml`中的模型路径和数据集名称，其他的配置请根据需要进行修改。
  ```
  ### model
  model_name_or_path: [!!!add the model path here!!!]

  ### dataset
  dataset: [!!!add the data set name here!!!]
  ```
3. 执行训练命令
    * 运行单机训练
    请注意这里需要设置`DISABLE_VERSION_CHECK`环境变量，避免版本冲突。
    ```
    export DISABLE_VERSION_CHECK=1
    llamafactory-cli train examples/hunyuan/hunyuan_full.yaml
    ```
    * 运行多机训练
    在每个节点上执行以下命令。请注意将`torchrun`需要的`NNODES`、`NODE_RANK`、`MASTER_ADDR`和`MASTER_PORT`按照您运行的环境进行配置。
    ```
    export DISABLE_VERSION_CHECK=1
    FORCE_TORCHRUN=1 NNODES=${NNODES} NODE_RANK=${NODE_RANK} MASTER_ADDR=${MASTER_ADDR} MASTER_PORT=${MASTER_PORT} \
    llamafactory-cli train examples/hunyuan_full.yaml
    ```

&nbsp;

## 量化压缩

我们使用了 [AngleSlim](https://github.com/tencent/AngelSlim) 压缩工具来生成 FP8 和 INT4 量化模型。`AngleSlim` 是一款专门致力于打造更易用、更全面且更高效的模型压缩解决方案的工具。

### FP8 量化
我们采用FP8-static量化，FP8量化采用8位浮点格式，通过少量校准数据（无需训练）预先确定量化scale，将模型权重与激活值转换为FP8格式，提升推理效率并降低部署门槛。 我们您可以使用AngleSlim量化，你也可以直接下载我们量化完成的开源模型使用 [AngelSlim](https://huggingface.co/AngelSlim).

### Int4 Quantization
Int4量化我们采用GPTQ和AWQ算法实现W4A16量化。

GPTQ算法采用逐层处理模型权重，利用少量校准数据最小化量化后的权重重构误差，通过近似Hessian逆矩阵的优化过程逐层调整权重。流程无需重新训练模型，仅需少量校准数据即可量化权重，提升推理效率并降低部署门槛。
AWQ使用少量校准数据（无需进行训练）来计算激活值的幅度，从而进行统计计算。对于每个权重通道，都会计算一个缩放系数s，以扩大重要权重的数值表达范围，从而在量化过程中能够保留更多的信息。

您可以使用 [AngleSlim](https://github.com/tencent/AngelSlim) 量化，也可以直接下载我们量化完成的开源模型使用 [AngelSlim](https://huggingface.co/AngelSlim) 。


#### 量化 Benchmark
本小节介绍了混元量化模型的基准指标。

|     Bench     |           Quantization            |    Hunyuan-0.5B-Instruct     |     Hunyuan-1.8B-Instruct      |     Hunyuan-4B-Instruct      |     Hunyuan-7B-Instruct      |
|:-------------:|:---------------------------------:|:----------------------------:|:------------------------------:|:----------------------------:|:----------------------------:|
|     DROP      | B16<br>FP8<br>Int4GPTQ<br>Int4AWQ | 52.8<br>51.6<br>50.9<br>48.9 |  76.7<br>75.1<br>73.0<br>71.7  | 78.2<br>78.3<br>78.1<br>78.2 | 85.9<br>86.0<br>85.7<br>85.9 |
| GPQA-Diamond  | B16<br>FP8<br>Int4GPTQ<br>Int4AWQ | 23.3<br>22.5<br>23.3<br>23.3 | 47.2<br>47.7<br>44.43<br>43.62 |  61.1<br>60.2<br>58.1<br>-   | 60.1<br>60.1<br>60.0<br>60.1 |
| OlympiadBench | B16<br>FP8<br>Int4GPTQ<br>Int4AWQ | 29.6<br>29.6<br>26.8<br>26.3 |  63.4<br>62.5<br>60.9<br>61.7  | 73.1<br>73.1<br>72.9<br>72.8 | 76.5<br>76.6<br>76.2<br>76.4 |
|   AIME 2024   | B16<br>FP8<br>Int4GPTQ<br>Int4AWQ |    17.2<br>17.2<br>-<br>-    |    56.7<br>55.17<br>-<br>-     |    78.3<br>76.6<br>-<br>-    | 81.1<br>80.9<br>81.0<br>80.9 |



&nbsp;

## 推理和部署

HunyuanLLM可以采用TensorRT-LLM, vLLM或sglang部署。为了简化部署过程HunyuanLLM提供了预构建docker镜像，详见一下章节。

镜像：https://hub.docker.com/r/hunyuaninfer/hunyuan-7b/tags

## 使用TensorRT-LLM推理
### Docker:

为了简化部署过程，HunyuanLLM提供了预构建docker镜像 (注意： 该镜像要求Host的Cuda版本为12.8以上）：

[hunyuaninfer/hunyuan-7b:hunyuan-7b-trtllm](https://hub.docker.com/r/hunyuaninfer/hunyuan-7b/tags) 。您只需要下载模型文件并用下面代码启动docker即可开始推理模型。
```shell
# 拉取
国内：
docker pull docker.cnb.cool/tencent/hunyuan/hunyuan-7b:hunyuan-7b-trtllm
国外：
docker pull hunyuaninfer/hunyuan-7b:hunyuan-7b-trtllm

# 启动
docker run --privileged --user root --name hunyuanLLM_infer --rm -it --ipc=host --ulimit memlock=-1 --ulimit stack=67108864 --gpus=all hunyuaninfer/hunyuan-7b:hunyuan-7b-trtllm
```

注: Docker容器权限管理。以上代码采用特权模式（--privileged）启动Docker容器会赋予容器较高的权限，增加数据泄露和集群安全风险。建议在非必要情况下避免使用特权模式，以降低安全威胁。对于必须使用特权模式的场景，应进行严格的安全评估，并实施相应的安全监控、加固措施。

### BF16部署

#### Step1：执行推理

#### 方式1：命令行推理

下面我们展示一个代码片段，采用`TensorRT-LLM`快速请求chat model：
修改 examples/pytorch/quickstart_advanced.py 中如下代码：


```python
def setup_llm(args):
    kv_cache_config = KvCacheConfig(
        enable_block_reuse=not args.disable_kv_cache_reuse,
        free_gpu_memory_fraction=args.kv_cache_fraction,
    )
    spec_config = None

    hf_ckpt_path="$your_hunyuan_model_path"
    tokenizer = AutoTokenizer.from_pretrained(hf_ckpt_path, trust_remote_code=True)
    llm = LLM(
        tokenizer=tokenizer,
        model=args.model_dir,
        backend='pytorch',
        disable_overlap_scheduler=args.disable_overlap_scheduler,
        kv_cache_dtype=args.kv_cache_dtype,
        kv_cache_config=kv_cache_config,
        attn_backend=args.attention_backend,
        use_cuda_graph=args.use_cuda_graph,
        cuda_graph_padding_enabled=args.cuda_graph_padding_enabled,
        cuda_graph_batch_sizes=args.cuda_graph_batch_sizes,
        load_format=args.load_format,
        print_iter_log=args.print_iter_log,
        enable_iter_perf_stats=args.print_iter_log,
        torch_compile_config=TorchCompileConfig(
            enable_fullgraph=args.use_torch_compile,
            enable_inductor=args.use_torch_compile,
            enable_piecewise_cuda_graph= \
                args.use_piecewise_cuda_graph)
        if args.use_torch_compile else None,
        moe_backend=args.moe_backend,
        enable_trtllm_sampler=args.enable_trtllm_sampler,
        max_seq_len=args.max_seq_len,
        max_batch_size=args.max_batch_size,
        max_num_tokens=args.max_num_tokens,
        enable_attention_dp=args.enable_attention_dp,
        tensor_parallel_size=args.tp_size,
        pipeline_parallel_size=args.pp_size,
        moe_expert_parallel_size=args.moe_ep_size,
        moe_tensor_parallel_size=args.moe_tp_size,
        moe_cluster_parallel_size=args.moe_cluster_size,
        enable_chunked_prefill=args.enable_chunked_prefill,
        speculative_config=spec_config,
        trust_remote_code=args.trust_remote_code,
        gather_generation_logits=args.return_generation_logits)

    sampling_params = SamplingParams(
        end_id=127960,
        max_tokens=args.max_tokens,
        temperature=args.temperature,
        top_k=args.top_k,
        top_p=args.top_p,
        return_context_logits=args.return_context_logits,
        return_generation_logits=args.return_generation_logits,
        logprobs=args.logprobs)
    return llm, sampling_params


def main():
    args = parse_arguments()
    prompts = args.prompt if args.prompt else example_prompts

    llm, sampling_params = setup_llm(args)
    new_prompts = []
    for prompt in prompts:
        messages = [{"role": "user", "content": f"{prompt}"}]
        new_prompts.append(
            llm.tokenizer.apply_chat_template(messages,
                                                tokenize=False,
                                                add_generation_prompt=True))
    prompts = new_prompts
    outputs = llm.generate(prompts, sampling_params)

    for i, output in enumerate(outputs):
        prompt = output.prompt
        generated_text = output.outputs[0].text
        print(f"[{i}] Prompt: {prompt!r}, Generated text: {generated_text!r}")
```

运行方式：

```shell
python3 quickstart_advanced.py --model_dir "HunyuanLLM模型路径" --tp_size 1
```

#### 方式2：服务化推理

下面我们展示使用`TensorRT-LLM`服务化的方式部署模型和请求。

以tencent/Hunyuan-7B-Instruct为例
准备配置文件：

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

启动服务：

```shell
trtllm-serve \
  /path/to/HunYuan-7b \
  --host localhost \
  --port 8000 \
  --backend pytorch \
  --max_batch_size 32 \
  --max_num_tokens 16384 \
  --tp_size 1 \
  --kv_cache_free_gpu_memory_fraction 0.6 \
  --trust_remote_code \
  --extra_llm_api_options /path/to/extra-llm-api-config.yml
```

服务启动成功后, 使用 OpenAI API 进行模型推理调用：
```
curl -X POST "http://localhost:8000/v1/chat/completions" \
  -H "Content-Type: application/json" \
  --data '{
    "model": "HunYuan/HunYuan-7b",
    "messages": [
      {
        "role": "user",
        "content": "Write a short summary of the benefits of regular exercise"
      }
    ]
  }'
```

#### FP8/Int4量化模型部署：
目前 TensorRT-LLM 的 fp8 和 int4 量化模型正在支持中，敬请期待。


## 使用vLLM推理
### 版本要求:

请使用vLLM v0.10.0之后的版本进行部署和推理

需要安装指定版本的transformers，我们将在不久后完成对transformers主分支的合入
```SHELL
pip install git+https://github.com/huggingface/transformers@4970b23cedaf745f963779b4eae68da281e8c6ca
```
### BF16部署

以tencent/Hunyuan-7B-Instruct为例，已经通过上述的transformers获取了模型地址
```shell
export MODEL_PATH=PATH_TO_MODEL
```

#### Step1：执行推理

#### 方式1：命令行推理

下面我们展示一个代码片段，采用`vLLM`快速请求chat model：

注: vLLM组件远程代码执行防护。下列代码中vLLM组件的trust-remote-code配置项若被启用，将允许加载并执行来自远程模型仓库的代码，这可能导致恶意代码的执行。除非业务需求明确要求，否则建议该配置项处于禁用状态，以降低潜在的安全威胁。


```python
import os
from typing import List, Optional
from vllm import LLM, SamplingParams
from vllm.inputs import PromptType
from transformers import AutoTokenizer

model_path=os.environ.get('MODEL_PATH')
tokenizer = AutoTokenizer.from_pretrained(model_path, trust_remote_code=True)

llm = LLM(model=model_path,
        tokenizer=model_path,
        trust_remote_code=True,
        dtype='bfloat16',
        tensor_parallel_size=4,
        gpu_memory_utilization=0.9)

sampling_params = SamplingParams(
    temperature=0.7, top_p=0.8, max_tokens=4096, top_k=20, repetition_penalty=1.05)

messages = [
    {
        "role": "system",
        "content": "You are a helpful assistant.",
    },
    {"role": "user", "content": "Write a short summary of the benefits of regular exercise"},
]

tokenized_chat = tokenizer.apply_chat_template(messages, tokenize=True, add_generation_prompt=True, return_tensors="pt")

dummy_inputs: List[PromptType] = [{
    "prompt_token_ids": batch
} for batch in tokenized_chat.numpy().tolist()]

outputs = llm.generate(dummy_inputs, sampling_params)

# Print the outputs.
for output in outputs:
    prompt = output.prompt
    generated_text = output.outputs[0].text
    print(f"Prompt: {prompt!r}, Generated text: {generated_text!r}")
```

#### 方式2：服务化推理

下面我们展示使用`vLLM`服务化的方式部署模型并请求

我们启动服务，运行 :
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

运行成功后, 运行请求脚本：
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

### 量化模型部署：

本部分介绍采用vLLM部署量化后模型的流程。


#### Int8量化模型部署：
部署Int8-weight-only版本HunYuan-7B模型

我们启动Int8服务，运行：
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

#### Int4量化模型部署：
部署Int4-weight-only版本HunYuan-7B模型，采用GPTQ方式：

```shell
export MODEL_PATH=PATH_TO_INT4_MODEL
```
接着我们启动Int4服务，运行：
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


#### FP8量化模型部署：
部署W8A8C8版本HunYuan-7B模型

我们启动FP8服务，运行：
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

## 使用sglang推理

### BF16部署

#### Step1: 拉取镜像


```
docker pull lmsysorg/sglang:latest
```

- 启动 API server:

```
docker run --entrypoint="python3" --gpus all \
    --shm-size 32g \
    -p 30000:30000 \
    --ulimit nproc=10000 \
    --privileged \
    --ipc=host \
     lmsysorg/sglang:latest \
    -m sglang.launch_server --model-path hunyuan/huanyuan_7B --tp 1 --trust-remote-code --host 0.0.0.0 --port 30000
```

#### Step2：执行推理

#### 方式1：命令行推理

下面我们展示一个代码片段，采用`sglang`快速请求chat model：


```python
import sglang as sgl
from transformers import AutoTokenizer

model_path=os.environ.get('MODEL_PATH')


tokenizer = AutoTokenizer.from_pretrained(model_path, trust_remote_code=True)

messages = [
    {
        "role": "system",
        "content": "You are a helpful assistant.",
    },
    {"role": "user", "content": "Write a short summary of the benefits of regular exercise"},
]
prompts = []
prompts.append(tokenizer.apply_chat_template(
    messages,
    tokenize=False,
    add_generation_prompt=True
))
print(prompts)

llm = sgl.Engine(
    model_path=model_path,
    tp_size=1,
    trust_remote_code=True,
    mem_fraction_static=0.7,
)

sampling_params = {"temperature": 0.7, "top_p": 0.8, "top_k": 20, "max_new_tokens": 4096}
outputs = llm.generate(prompts, sampling_params)
for prompt, output in zip(prompts, outputs):
    print(f"Prompt: {prompt}\nGenerated text: {output['text']}")
```

#### 方式2：服务化推理

下面我们展示使用`sglang`服务化的方式部署模型和请求。

```shell
model_path="HunyuanLLM模型路径"
python3 -u -m sglang.launch_server \
    --model-path $model_path \
    --tp 4 \
    --trust-remote-code
```

服务启动成功后, 运行请求脚本：
```python
import openai
client = openai.Client(
    base_url="http://localhost:30000/v1", api_key="EMPTY")

response = client.chat.completions.create(
    model="default",
    messages= [
        {"role": "user", "content": "Write a short summary of the benefits of regular exercise"},
    ],
    temperature=0.7,
    max_tokens=4096,
    extra_body={"top_p": 0.8, "top_k": 20}
)
print(response)
```

#### FP8/Int4量化模型部署：
目前 sglang 的 fp8 和 int4 量化模型正在支持中，敬请期待。

## 交互式Demo Web
hunyuan-7B 现已开放网页demo。访问 https://hunyuan.tencent.com/?model=hunyuan-7b 即可简单体验我们的模型。

## 社区资源

- [Hunyuan-7B 在 CNB 中快速开始](https://cnb.cool/tencent/hunyuan/examples/Hunyuan-7B-Instruct-quick-start)

## 联系我们
如果你想给我们的研发和产品团队留言，欢迎联系我们腾讯混元LLM团队。你可以通过邮件（hunyuan_opensource@tencent.com）联系我们。
