---
blocks:
  - body: >
      [Speech Recognition](/speech-recognition) / [Models](/models) /
      [IndicWav2Vec](/indic-wav-2-vec)


      # IndicWav2Vec


      IndicWav2Vec is a multilingual speech model pretrained on 40 Indian
      langauges. This model represents the largest diversity of Indian languages
      in the pool of multilingual speech models. We fine-tune this model for
      downstream ASR for 9 languages and obtain state-of-the-art results on 3
      public benchmarks, namely MUCS, MSR and OpenSLR.


      As part of IndicWav2Vec we create largest publicly available corpora for
      40 languages from 4 different language families. We also trained
      state-of-the-art ASR models for 9 Indian languages.


      ## Benchmarks


      We evaluate our models on 3 publicly available benchmarks MUCS, MSR and
      OpenSLR and below mentioned are our results
    color: default
    _template: content
  - markdownTable: >-
      |Model    | gu   | ta   | te   | gu   | hi   | mr   | or   | ta   | te   |
      bn   | ne   | si   |

      | ------- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
      ---- | ---- | ---- |

      |IndicW2V | 20.5 | 22.1 | 22.9 | 26.2 | 16.0 | 19.3 | 25.6 | 27.3 | 29.3 |
      16.6 | 11.9 | 24.8 |

      |IndicW2V + LM| 11.7 | 13.6 | 11.0 | 17.2 | 14.7 | 13.8 | 17.2 | 25.0 |
      20.5 | 13.6 | 13.6 | - |
    markupTable: ''
    color: default
    _template: table
  - body: "## Updates\n\n21 June 2022\n\n```\nAdded more documentation\r\n\n```\n\n## Table of contents\n\n*   [IndicWav2Vec](https://github.com/AI4Bharat/IndicWav2Vec#indicwav2vec)\n    *   [Benchmarks](https://github.com/AI4Bharat/IndicWav2Vec#benchmarks)\n    *   [Updates](https://github.com/AI4Bharat/IndicWav2Vec#updates)\n    *   [Table of contents](https://github.com/AI4Bharat/IndicWav2Vec#table-of-contents)\n    *   [Resources](https://github.com/AI4Bharat/IndicWav2Vec#resources)\n        *   [Download Models](https://github.com/AI4Bharat/IndicWav2Vec#download-models)\n        *   [Hosted API Usage](https://github.com/AI4Bharat/IndicWav2Vec#hosted-api-usage)\n        *   [Accessing on ULCA](https://github.com/AI4Bharat/IndicWav2Vec#accessing-on-ulca)\n    *   [Quick start](https://github.com/AI4Bharat/IndicWav2Vec#quick-start)\n        *   [Python Inference](https://github.com/AI4Bharat/IndicWav2Vec#python-inference)\n        *   [Huggingface Inference](https://github.com/AI4Bharat/IndicWav2Vec#huggingface-inference)\n    *   [Tutorials](https://github.com/AI4Bharat/IndicWav2Vec#tutorials)\n        *   [Setting up your environment](https://github.com/AI4Bharat/IndicWav2Vec#setting-up-your-environment)\n        *   [Pretraining](https://github.com/AI4Bharat/IndicWav2Vec#pretraining)\n            *   [Data preparation](https://github.com/AI4Bharat/IndicWav2Vec#data-preparation)\n            *   [Manifest Creation](https://github.com/AI4Bharat/IndicWav2Vec#manifest-creation)\n        *   [Training procedure and code](https://github.com/AI4Bharat/IndicWav2Vec#training-procedure-and-code)\n        *   [Finetuning](https://github.com/AI4Bharat/IndicWav2Vec#finetuning)\n            *   [Data preparation](https://github.com/AI4Bharat/IndicWav2Vec#data-preparation-1)\n            *   [Finetuning procedure and code](https://github.com/AI4Bharat/IndicWav2Vec#finetuning-procedure-and-code)\n            *   [Finetuning procedure and code](https://github.com/AI4Bharat/IndicWav2Vec#finetuning-procedure-and-code-1)\n        *   [Language Modelling (LM)](https://github.com/AI4Bharat/IndicWav2Vec#language-modelling-lm)\n            *   [Data preparation](https://github.com/AI4Bharat/IndicWav2Vec#data-preparation-2)\n            *   [Training details](https://github.com/AI4Bharat/IndicWav2Vec#training-details)\n        *   [Evaluating ASR models](https://github.com/AI4Bharat/IndicWav2Vec#evaluating-asr-models)\n        *   [Model exporting](https://github.com/AI4Bharat/IndicWav2Vec#model-exporting)\n        *   [Deployment](https://github.com/AI4Bharat/IndicWav2Vec#deployment)\n    *   [Cite](https://github.com/AI4Bharat/IndicWav2Vec#cite)\n    *   [License](https://github.com/AI4Bharat/IndicWav2Vec#license)\n    *   [Contributors](https://github.com/AI4Bharat/IndicWav2Vec#contributors)\n    *   [Contact](https://github.com/AI4Bharat/IndicWav2Vec#contact)\n\n## Resources\n\n### Download Models\n\nFinetuned Models\n"
    color: default
    _template: content
  - markdownTable: >-
      |Language |Acoustic Model | Dictionary | Language Model | Lexicon | Wandb
      |

      | - | - |  - | - | - | - |

      | Bengali |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/bn/bn.pt)
      \| [[hf]]()|
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/bn/dict.ltr.txt)
      | 
      [KenLM](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/bn/lm.binary)
      |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/bn/lexicon.lst)
      | [link]() |

      | Gujarati |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/gu/gu.pt)
      / [hf]() |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/gu/dict.ltr.txt)
      | 
      [KenLM](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/gu/lm.binary)
      |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/gu/lexicon.lst)
      | [link]() |

      | Hindi |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/hi/hi.pt)
      / [hf]() |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/hi/dict.ltr.txt)
      | 
      [KenLM](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/hi/lm.binary)
      |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/hi/lexicon.lst)
      | [link]() |

      | Marathi |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/mr/mr.pt)
      / [hf]() |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/mr/dict.ltr.txt)
      | 
      [KenLM](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/mr/lm.binary)
      |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/mr/lexicon.lst)
      | [link]() |

      | Nepali |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/ne/ne.pt)
      / [hf]() |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/ne/dict.ltr.txt)
      | 
      [KenLM](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/ne/lm.binary)
      |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/ne/lexicon.lst)
      | [link]() |

      | Odia |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/or/or.pt)
      / [hf]() |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/or/dict.ltr.txt)
      | 
      [KenLM](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/or/lm.binary)
      |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/or/lexicon.lst)
      | [link]() |

      | Tamil |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/ta/ta.pt)
      / [hf]() |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/ta/dict.ltr.txt)
      | 
      [KenLM](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/ta/lm.binary)
      |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/ta/lexicon.lst)
      | [link]() |

      | Telugu |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/te/te.pt)
      / [hf]() |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/te/dict.ltr.txt)
      | 
      [KenLM](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/te/lm.binary)
      |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/te/lexicon.lst)
      | [link]() |

      | Sinhala |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/si/si.pt)
      / [hf]() |
      [link](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/models/si/dict.ltr.txt)
      |  [KenLM]() | [link]() | [link]() |
    markupTable: ''
    color: tint
    _template: table
  - body: |
      Pretained Models
    _template: content
  - markdownTable: >
      |Name |Model Checkpoint | 

      | - | - |  

      | IndicWav2Vec Large |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/pretrained_models/indicw2v_large_pretrained.pt)
      | 

      | IndicWav2Vec Base |
      [fairseq](https://indic-asr-public.objectstore.e2enetworks.net/aaai_ckpts/pretrained_models/indicw2v_base_pretrained.pt)
      | 
    markupTable: >-

      (* Trained on 40 Indian Languages, more details can be found
      [here](https://www.aaai.org/AAAI22Papers/AAAI-12428.JavedT.pdf))
    color: default
    _template: table
  - body: |
      ### Hosted API Usage

      Our models are hosted at the following API end points.
    _template: content
  - markdownTable: >-
      | Langugage| Language Code | API End point |

      | - | - | - |

      | Bengali | bn | [coming soon - will be back shortly]() |

      | Gujarati | gu | [coming soon - will be back shortly]() |

      | Hindi | hi | [Try out
      here](https://bhashini.gov.in/ulca/search-model/63074ab02f73e063a4a83270/model)
      |

      | Marathi | mr| [Try out
      here](https://bhashini.gov.in/ulca/search-model/630c14c32f73e063a4a83272/model)
      |

      | Nepali | ne| [coming soon - will be back shortly]() |

      | Odia | or| [coming soon - will be back shortly]() |

      | Tamil | ta| [Try out
      here](https://bhashini.gov.in/ulca/search-model/63076fe5ecae176a1558ffa4/model)
      |

      | Telugu | te| [Try out
      here](https://bhashini.gov.in/ulca/search-model/6307704d2f73e063a4a83271/model)
      |

      | Sinhala | si| [coming soon - will be back shortly]() |
    color: default
    _template: table
  - body: "Input API data format\n\n```\n{\r\n    \"config\": {\r\n        \"language\":{\r\n          \"sourceLanguage\": \"#Language Code\"\r\n        },\r\n        \"transcriptionFormat\": {\"value\":\"transcript\"},\r\n        \"audioFormat\": \"wav\"\r\n    },\r\n    \"audio\": [{\r\n        \"audioContent\": \"#BASE64 Encoded String\"\r\n    }]\r\n}\r\n\r\nOR\r\n\r\n{\r\n    \"config\": {\r\n        \"language\":{\r\n          \"sourceLanguage\": \"#Language Code\"\r\n        },\r\n        \"transcriptionFormat\": {\"value\":\"transcript\"},\r\n        \"audioFormat\": \"wav\"\r\n    },\r\n    \"audio\": [{\r\n        \"audioUri\": \"#HTTP/GS path to file\"\r\n    }]\r\n}\r\n\r\n\n```\n\nOutput\n\n```\n{\r\n    \"output\": [\r\n        {\r\n            \"source\": \"सेकेंड स्टेप इस देसी है स्पेसिफाइड फॉरेस्ट राइट\"\r\n        }\r\n    ],\r\n    \"status\": \"SUCCESS\"\r\n}\r\n\n```\n\n### Accessing on ULCA\n\nOur models can be directly accessed on\_[ULCA](https://bhashini.gov.in/ulca/model/explore-models)\_by going into ASR section and filtering models by IndicWav2Vec.\n\n## Quick start\n\n### Python Inference\n\nGreedy Decoding\n\n```\npython sfi.py [--audio-file AUDIO_FILE_PATH] \n              [--ft-model FT_MODEL]\n              [--w2l-decoder viterbi]\n```\n\nKenLM Decoding\n\n```\npython sfi.py [--audio-file AUDIO_FILE_PATH]\n              [--ft-model FT_MODEL_PATH]\n              [--w2l-decoder kenlm]\n              [--lexicon LEXICON_PATH]\n              [--kenlm-model KENLM_MODEL_PATH]\n              [--beam-threshold BEAM_THRESHOLD]\n              [--beam-size-token BEAM_SIZE_TOKEN]\n              [--beam BEAM_SIZE]\n              [--word-score WORD_SCORE]\n              [--lm-weight LM_WEIGHT]\n              [--unk-weight UNK_WEIGHT]\n              [--sil-weight SIL_WEIGHT]\n              [--nbest NBEST]\n            \n```\n\n### Huggingface Inference\n\n*   Coming soon\n\n## Tutorials\n\n### Setting up your environment\n\nSetting up conda enviroment\n\n```\nconda create -n <env_name>conda activate <env_name>\n```\n\nInstalling/Updating Libraries\n\n```\nsudo apt-get install liblzma-dev libbz2-dev libzstd-dev libsndfile1-dev libopenblas-dev libfftw3-dev libgflags-dev libgoogle-glog-dev\n\nsudo apt install build-essential cmake libboost-system-dev libboost-thread-dev libboost-program-options-dev libboost-test-dev libeigen3-dev zlib1g-dev libbz2-dev liblzma-dev ffmpeg \n\npip install -r requirements.txt \n\npip install packaging soundfile swifter editdistance omegaconf\n\n```\n\nInstalling Fairseq\n\n```\ngit clone https://github.com/AI4Bharat/fairseq.git\n\ncd fairseq\n\npip install --editable ./     \n\n#[Optional for faster training]\n\ngit clone https://github.com/NVIDIA/apex\n\ncd apex\n\npip install -v --no-cache-dir --global-option=\"--cpp_ext\" --global-option=\"--cuda_ext\" \\--global-option=\"--deprecated_fused_adam\" --global-option=\"--xentropy\" \\--global-option=\"--fast_multihead_attn\" ./\n\ncd ..\n\n```\n\nInstalling KenLM\n\n```\ngit clone https://github.com/kpu/kenlm.git\n\ncd kenlm\n\nmkdir -p build && cd build\n\ncmake .. \n\nmake -j 16\n\ncd ..\n\nexport KENLM_ROOT=$PWD\n\ncd ..\n\n```\n\nInstalling Flashlight\n\n```\ngit clone https://github.com/flashlight/flashlight.git\n\ncd flashlight/bindings/python\n\nexport USE_MKL=0\n\npython setup.py install\n\n```\n\n### Pretraining\n\n#### Data preparation\n\n*   Downloading Audio Dataset (Unlabelled)\n    *   `bash dw_util.sh <path_to_urls> <data_store_path> <num_of_threads>`\n    *   The\_`<data_store_path>`\_refers to the location where the data will be downloaded. The\_`<num_of_threads>`\_can be used to control the parallelization.\n*   Voiced Activity Detection\n    *   `python vad.py <data_read_dir> <data_write_dir> <folder_name>`\n    *   The\_`<data_read_dir>`\_is the root of downloaded files which contain downloaded data in language-named-folders.\n    *   The\_`<data_write_dir>`\_is the location for saving the data after VAD step.\n    *   The\_`<folder_name>`\_refers to the names of language-named-folder for which you want to perform this VAD step.\n    *   \\*The reason why folder\\_name has been kept as a seperate entity is to allow parallelization because one can process multiple folders simultaneously.\n*   SNR Filtering\n    *   `python snr.py <data_path> <folder/language_name>`\n    *   where the\_`<data_path>`\_refers to the root path containing all the audios in language specific folders. Here it refers to the`\_<data_write_dir>`\_from the previous step. The\_`<folder/language_name>`\_refers to name of language\\_specific folder for which snr\\_filtering needs to be done. The audio data that is rejected is moved in the folder\_**\"snr\\_rejected\"**, which is created automatically.\n*   Chunking\n    *   **python chunking.py \\<chunking\\_path>**\n    *   All the audio files present in the\_`<chunking_path>`\_will be chunked and saved in the same location. The original files are\_**removed**.\n\nOr alternatively users can use the one single script\_`process_data.sh`\_to run the entire pipeline\n\n*   Usage:\_`bash process_data.sh </path/to/download> <num_of_threads>`\n*   The\_`</path/to/download>`\_refers to the location where the data will be downloaded.\n*   The\_`<num_of_threads>`\_can be used to control the parallelization.\n*   Please make sure that the relative path is urls directory is\_`../urls`\_from the script.\n\n#### Manifest Creation\n\nFor creating language-wise pretraining manifest\n\n```\npython path/to/lang_wise_manifest_creation.py /path/to/wave/files --dest /manifest/path --ext $ext --valid-percent $valid\r\n\n```\n\nFor\_`/path/to/wav/files/`\_we expect the directory to have one folder per language under the parent directory\n\nIn our pretraing, we use a\_`--valid-percent`\_as\_`0.03`\n\nFor creating a combined validation file for all languages, we concatenate all individual\_`*_valid.tsv`\_files to create a valid.tsv file.\n\n```\nimport pandas as pd\r\nimport glob\r\n\r\nfilenames = glob.glob(\"*_valid.tsv\")\r\n\r\ncombined = []\r\nfor f in filename:\r\n    df = pd.read_csv(f, skiprows=1, names=['f', 'd'], sep='\\t')\r\n    combined.append(df)\r\n\r\ndf_combined = pd.concat(combined, axis=0, ignore_index=True)\r\ndf_combined.to_csv('valid.tsv', index=True, header=False, sep='\\t')\r\n\n```\n\nWe then add the\_`/path/to/wav/files/`\_to the first line of the\_`valid.tsv`\_file\n\n### Training procedure and code\n\nFor pretraining the model we do multi-node training and schedule the runs with slurm.\n\nFollowing is the invocation script for training IndicWav2Vec base starting from Wav2Vec2.0 English base ckeckpoint\n\n```\nfairseq-hydra-train \\\r\n  task.data=/path/to/manifest/directory \\\r\n  common.wandb_project=<wandb project name> \\\r\n  task._name=temp_sampled_audio_pretraining \\\r\n  +task.sampling_alpha=0.7 \\\r\n  common.log_interval=200 \\\r\n  common.log_format=tqdm \\\r\n  dataset.max_tokens=3000000 \\\r\n  common.user_dir=/path/to/custom_task/directory \\\r\n  checkpoint.save_dir=/path/to/save/model/checkpoints \\\r\n  checkpoint.restore_file=/path/to wav2vec2-english-base/checkpoint.pt \\\r\n  +optimization.update_freq='[2]' \\\r\n  optimization.clip_norm=0.5 \\\r\n  checkpoint.reset_optimizer=true \\\r\n  distributed_training.distributed_world_size=<total GPUs> \\\r\n  distributed_training.distributed_port=$PORT \\\r\n  --config-dir /path/to/configs/directory \\\r\n  --config-name wav2vec2_base_librispeech\"\r\n\n```\n\nFor Large model we override the above configuration with\n\n```\n  checkpoint.restore_file=/path/to wav2vec2-english-large/checkpoint.pt \\\r\n  +optimization.update_freq='[6]' \\\r\n  lr_scheduler.warmup_updates=0 \\\r\n  --config-name wav2vec2_large_librivox\"\r\n\n```\n\nConfigs for both the models are provided in the configs directory\n\n### Finetuning\n\n#### Data preparation\n\n*   Sampling correction (if required for a dataset): For datasets, that are not sampled uniformly at 16kHz, the user may run the following command to normalize the data first.\n\n```\nbash normalize_sr.sh <path/to/the/folder/to/normalize> <ext|wav|mp3>\n```\n\n*   Manifest creation\n    *   Make a new directory and name it (say\_`mucs`)\n    *   Download and extract the benchmark data inside mucs. The data should be extracted in such a way that each folder inside should contain data for a particular language i.e each language specific folder should contain train, valid and test folder and within them the audio + transcript.txt\n    *   Note that the transcript.txt contain entries of the following type\n\n```\n<filename1> <transcript1> #just the filename and not the path\n\n<filename2> <transcript2>\n\n<filename3> <transcript3>\n\n<filename4> <transcript4>\n\n...\n```\n\n*   Sample structure of folder tree:\n\n```\nmucs(or msr/openslr)\n    ├── hindi\n    │\_\_ ├── test\n    │\_\_ │\_\_ ├── audio\n    │\_\_ │\_\_ └── transcript.txt\n    │\_\_ ├── train\n    │\_\_ │\_\_ ├── audio\n    │\_\_ │\_\_ └── transcript.txt\n    │\_\_ └── valid\n    │\_\_     ├── audio\n    │\_\_     └── transcript.txt\n    └── marathi\n        ├── test\n        │\_\_ ├── audio\n        │\_\_ └── transcript.txt\n        ├── train\n        │\_\_ ├── audio\n        │\_\_ └── transcript.txt\n        └── valid\n            ├── audio\n            └── transcript.txt\n        .\n        .\n        .\n        .\n```\n\n*   Creating the manifest\n\n```\nbash m_process.sh <path/to/the/root/folder/(mucs)>\n```\n\n*   The would result in creation of manifest folders in each language specific folder which can the be used with fairseq for finetuning.\n\n#### Finetuning procedure and code\n\nFollowing is the invocation script for finetuning IndicWav2Vec large on a particular language\n\n```\nfairseq-hydra-train \\\r\n  task.data=/path/to/finetune/manifest/directory/for/a/particular/language \\\r\n  common.wandb_project=<wandb project name> \\\r\n  model.w2v_path=/path/to/pretrained/model_large.pt \\\r\n  common.log_interval=50 \\\r\n  common.log_format=tqdm \\\r\n  dataset.max_tokens=1000000 \\\r\n  checkpoint.save_dir=/path/to/save/model/fine_tune_checkpoints \\\r\n  +optimization.update_freq='[1]' \\\r\n  distributed_training.distributed_world_size=<total GPUs> \\\r\n  --config-dir /path/to/configs/directory \\\r\n  --config-name ai4b_xlsr\"\r\n\n```\n\nFor IndicWav2Vec Base model we override the above configuration with\n\n```\n  model.w2v_path=/path/to/pretrained/model_base.pt \\\r\n  --config-name ai4b_base\"\r\n\n```\n\nConfigs for both the models are provided in the\_[finetune\\_configs](https://github.com/AI4Bharat/IndicWav2Vec/blob/main)\_directory\n\n#### Finetuning procedure and code\n\n### Language Modelling (LM)\n\nWe train 6-grams Statistical LM using\_[KenLM library](https://kheafield.com/code/kenlm/).\n\n#### Data preparation\n\n*   Prepare training manifest using\_[fairseq](https://github.com/pytorch/fairseq/tree/master/examples/wav2vec)\_and copy its path.\n*   Prepare clean\\_dump.txt containing\_`\"\\n\"`\_separated rows of text data.\n*   Add\_`dict.txt`\_containing\_`comma(,)`\_separated rows of characters and its' index.\n*   Add these two files to the\_`{lang}`\_folder, where\_`lang`\_denotes the language for which lm is to be trained.\n\n> Command to clean transcripts and prepare lexicon for training:\n\n```\npython utils/clean_corpus.py -d=<lm directory path> -l=<lang> --transcript=<speech transcript folder path> --st=<start code of lang> --en=<end code of lang> --top_k=<'k' most frequent words for vocab>\r\n\n```\n\n#### Training details\n\n> Run lm-training:\_`bash scripts/train_lm.sh <lm directory path> <lang>`.\n\nOuput will be generate at:\_`\"<lm directory path>/<lang>\"`.\n\n### Evaluating ASR models\n\n*   Evaluation using fairseq (infer.py)\n\n```\npython3 fairseq/speech_recognition/infer.py ${manifest_path} --task audio_finetuning \\\n--nbest 1 --path ${checkpoint_path} --gen-subset ${valid|test} --results-path ${result_path} --w2l-decoder {viterbi | kenlm} \\\n--lm-weight 0 --word-score 0 --sil-weight 0 --criterion ctc --labels ltr --max-tokens 5000000 \\\n--post-process letter\n```\n\n*   This is default fairseq evaluation command and more documentation about this command can be seen\_[here](https://github.com/AI4Bharat/IndicWav2Vec/blob/main)\n\n### Model exporting\n\n*   Huggingface\n*   ONNX/Torchscript\n\n### Deployment\n\n*   Server (Flask)\n    *   Install Flask\_`pip install flask flask-cors`\n    *   Change path for the acoustic models, decoding strategy, language models and lexicon in the Make path changes in\_`app/models_dict.json`\n    *   run server\_`python app/flask_dep.py`\n*   Server (Torchserve)\n    *   Coming soon\n*   Mobile\n    *   Coming soon\n\n## Cite\n\nPlease cite out work as:\n\n```\n@inproceedings{javed2021building,\r\n    title = {Towards Building ASR Systems for the Next Billion Users},\r\n    author = {Tahir Javed and Sumanth Doddapaneni and Abhigyan Raman and Kaushal Santosh Bhogale and Gowtham Ramesh and Anoop Kunchukuttan and Pratyush Kumar and Mitesh M. Khapra},\r\n    booktitle = \"Proceedings of the AAAI Conference on Artificial Intelligence\",\r\n    year = \"2022 (to appear)\",\r\n}\n```\n\n## License\n\nIndicWav2Vec is\_[MIT](https://choosealicense.com/licenses/mit/)-licensed. The license applies to all the pretrained, fine-tuned and language models\n\n## Contributors\n\n*   Tahir Javed, (IITM, AI4Bharat)\n*   Sumanth Doddapaneni, (AI4Bharat, RBCDSAI)\n*   Abhigyan Raman, (AI4Bharat)\n*   Kaushal Bhogale, (AI4Bharat)\n*   Gowtham Ramesh, (AI4Bharat, RBCDSAI)\n*   Anoop Kunchukuttan, (Microsoft, AI4Bharat)\n*   Pratyush Kumar, (Microsoft, AI4Bharat)\n*   Mitesh Khapra, (IITM, AI4Bharat, RBCDSAI)\n\n## Contact\n\n*   Anoop Kunchukuttan ([anoop.kunchukuttan@gmail.com](mailto:anoop.kunchukuttan@gmail.com))\n*   Mitesh Khapra ([miteshk@cse.iitm.ac.in](mailto:miteshk@cse.iitm.ac.in))\n*   Pratyush Kumar ([pratyush@cse.iitm.ac.in](mailto:pratyush@cse.iitm.ac.in))\n\n## Acknowledgements\n\nWe would like to thank EkStep Foundation for their generous grant which helped in setting up the Centre for AI4Bharat at IIT Madras to support our students, research staff, data and computational requirements. We would like to thank The Ministry of Electronics and Information Technology (NLTM) for its grant to support the creation of datasets and models for Indian languages under its ambitions Bhashini project. We would also like to thank the Centre for Development of Advanced Computing, India (C-DAC) for providing access to the Param Siddhi supercomputer for training our models. Lastly, we would like to thank Microsoft for its grant to create datasets, tools and resources for Indian languages.\n"
    _template: content
---

