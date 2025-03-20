# MiPortraitSR for NTIRE 2025 Real-World Face Restoration Challenge

## Environment

We test our code based on 
1. python 3.10.16 
2. CUDA 11.8
3. other packages can be found in requirements.txt

## Usage

~~~
conda create -n MPSR python=3.10
conda activate MPSR
pip install -r requirements.txt

// for testing
// If you run the code for the first time, it will take a while to download the SD model file.
// If you can't connect to the huggingface.co, please run 'export HF_ENDPOINT=https://hf-mirror.com' before running the code.
CUDA_VISIBLE_DEVICES=0 python test.py --valid_dir [path to val data dir] --test_dir [path to test data dir] --save_dir [path to your save dir] --model_id 10

// for evaluating
python eval.py \
--mode "test" \
--output_folder "/path/to/your/output_dir_test" \
--lq_ref_folder "/path/to/input_LQ_dir" \
--metrics_save_path "./IQA_results" \
--gpu_ids 0 \
--use_qalign True
~~~



This repo will be a part of the [challenge](https://github.com/zhengchen1999/NTIRE2025_RealWorld_Face_Restoration), please refer the challenge repo for more details.

## License
As a part of the challenge, we adhere to the same licensing terms [link](https://github.com/zhengchen1999/NTIRE2025_RealWorld_Face_Restoration).

## Acknowledgement
This project is based on [DiffBIR](https://github.com/XPixelGroup/DiffBIR), [PiSA-SR](https://github.com/csslc/PiSA-SR), [GFPGAN](https://github.com/TencentARC/GFPGAN), [FFA-Net](https://github.com/zhilin007/FFA-Net). Thanks for their awesome work.

## Contact
If you have any questions, please contact <zhangyun9@xiaomi.com>.