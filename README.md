# FinetuneQwen-1_8B-Chat-Int4
# 微调千问1.8B的int4量化版本大模型


请先打开 https://github.com/QwenLM/Qwen
然后clone下来


# 安装运行环境

建议使用下面的版本。
```
cuda 11.8
python 3.8
pytorch # 与cuda11.8对应的版本
```

## 启动conda环境

```
conda create -n py38 python=3.8
conda activate py38
```

## 安装Qwen模型依赖
```commandline
pip install -r requirements.txt  -i https://pypi.tuna.tsinghua.edu.cn/simple


pip install modelscope  -i https://pypi.tuna.tsinghua.edu.cn/simple

pip install transformers==4.32.0 accelerate tiktoken einops scipy transformers_stream_generator==0.0.4 peft deepspeed -i https://pypi.tuna.tsinghua.edu.cn/simple

# 因为使用了量化版本 所以请安装这些依赖
pip install auto-gptq optimum -i https://pypi.tuna.tsinghua.edu.cn/simple


```
## 执行微调脚本时报错
请安装下面的依赖，用pip安装有点问题，请使用conda安装
```commandline

conda install mpi4py
```

其他的参考jupter脚本

感谢B站大佬
https://www.bilibili.com/video/BV16a4y1z7LY/?spm_id_from=333.337.top_right_bar_window_history.content.click&vd_source=f9b029812d081f664782ff316df7a3cb