# Screen Detection from Egocentric Image Streams Leveraging Multi-View Vision Language Model

This is the implementation for "Screen Detection from Egocentric Image Streams Leveraging Multi-View Vision Language Model".

You need to download the Llama-2-7b.


## Data preprocess

You need to install unsloth environment to use the MiniLM to generate text embedding.
```bash
pip install unsloth
python step1_build_group_caption_example_caption.py
python step2_convert_group_caption_into_emb.py
```


## Run the model

The checkpoint file can be downloaded via the link: checkpoint_epoch5_step437.pth.

Please download it and save it into the MVVLM/saved_ckpt folder.

```bash
conda create --name MVVLM --file requirements.txt
cd MVVLM
conda activate MVVLM
bash scripts/run.sh
```

## Postprocessing
After the screen type identification, ChatGPT4 will be utilized to smooth the description for scene understanding.


## Data availability
The dataset used in the paper is not publicly available due to privacy and IRB restrictions

## citation
If you find this code useful, please consider citing it by:
```
@article{li2025tmm,
  title={Screen Detection from Egocentric Image Streams Leveraging Multi-View Vision Language Model},
  author={Li, Xueshen and Shen, Sen and Hou, Xinlong and Gao, Xinran and Huang, Ziyi and and Holiday, Steven and Cribbet Matthew and White, Susan and Sazonov, Edward and Gan, Yu},
  journal={IEEE Transactions on Multimedia},
  year={2025},
  addendum = "(\textbf{IF: 9.7})",
}

```
