To reproduce LLMSafe, follow these steps:

1. Install the Hugging Face Transformers and torch library:
```bash
pip install transformers
pip install torch
```
2. Download [Qwen1.5-1.8B-Chat](https://huggingface.co/Qwen/Qwen1.5-1.8B-Chat) to directory Qwen_Qwen1_5-1_8B-Chat
3. Open llmsafe.ipynb and encrypt the model by LLMSafe by run code until 7th cell.
4. Run cells 8 to 10 to observe that the encrypted model cannot output correctly without the proper inverse transformation.
5. Copy modeling_qwen2.py to the Transformers site-packages directory:
``` bash
cp modeling_qwen2.py path-to-python-site-packages/transformers/models/qwen2/
```
6. Restart llmsafe.ipynb to apply the changes and run all cells to see the effect of LLMSafe.