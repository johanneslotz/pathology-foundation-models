<div align="center">
<h1>Pathology Feature Extractors and Foundation Models</h1>
</div>

Recent years have witnessed the emergence of many new feature extractors trained using self-supervised learning on large pathology datasets.
This repository aims to provide a comprehensive list of these models, alongside key information about them.

I aim to update this list as new models are released, but please submit a pull request for any models I have missed!

| Name                                                                                  | Group                                                                                             |  Weights           | Released                                                                                              | SSL                                                                             | WSIs     | Tiles    | Patients   | Batch size | Iterations | Architecture     | Parameters | Embed dim | Input size |  Dataset                         | Links                                                                                                                                                                                                                                                                                                                         |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------ | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | -------- | -------- | ---------- | ---------- | ---------- | ---------------- | ---------- | --------- | ---------- | -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CTransPath](https://www.sciencedirect.com/science/article/abs/pii/S1361841522002043) | Sichuan University / Tencent AI Lab                                                               | :white_check_mark: | Dec 2021[\*](https://github.com/Xiyue-Wang/TransPath/commit/4b1c67655dd38cb192567b0981b6c1e9ade59ecf) | [SRCL](https://www.sciencedirect.com/science/article/abs/pii/S1361841522002043) | 32K      | 16M      |            |            |            | Swin-Transformer |            | 768       | 224        | TCGA, PAIP                       | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/Xiyue-Wang/TransPath)                                                                                                                                                                       |
| [RetCCL](https://www.sciencedirect.com/science/article/abs/pii/S1361841522002043)     | Sichuan University / Tencent AI Lab                                                               | :white_check_mark: | Dec 2021[\*](https://github.com/Xiyue-Wang/RetCCL/commit/e6faf0bd85c8e7e617882dd5d74e644d28eac771)    | [CCL](https://www.sciencedirect.com/science/article/abs/pii/S1361841522002043)  | 32K      | 16M      |            |            |            | ResNet-50        |            | 2048      | 224        | TCGA, PAIP                       | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/Xiyue-Wang/RetCCL)                                                                                                                                                                          |
| [REMEDIS](https://www.nature.com/articles/s41551-023-01049-7)                         | [Google Research](https://research.google)                                                        | :white_check_mark: | May 2022[\*](https://arxiv.org/abs/2205.09723v1)                                                      | SimCLR/BiT                                                                      | 29K      | 50M      | 11K cases  | 4096       | 1.2M       | ResNet-50        |            | 2048      | 224        | TCGA                             | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/google-research/medical-ai-research-foundations)                                                                                                                                            |
| [HIPT](https://ieeexplore.ieee.org/document/9880275)                                  | [Mahmood Lab](https://faisal.ai)                                                                  | :white_check_mark: | Jun 2022[\*](https://arxiv.org/abs/2206.02647v1)                                                      | DINOv1                                                                          | 11K      | 104M     |            | 256        | 400K       | ViT-S            |            | 384       | 256        | TCGA                             | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/mahmoodlab/HIPT)                                                                                                                                                                            |
| [Lunit-DINO](https://arxiv.org/abs/2212.04690)                                        | [Lunit](https://www.lunit.io)                                                                     | :white_check_mark: | Dec 2022[\*](https://arxiv.org/abs/2212.04690v1)                                                      | DINOv1                                                                          | 21K      |          |            |            |            | ViT-S            |            | 384       | 224        | TCGA                             | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/lunit-io/benchmark-ssl-pathology)                                                                                                                                                           |
| [Lunit-{BT,MoCoV2,SwAV}](https://arxiv.org/abs/2212.04690)                            | [Lunit](https://www.lunit.io)                                                                     | :white_check_mark: | Dec 2022[\*](https://arxiv.org/abs/2212.04690v1)                                                      | {BT,MoCoV2,SwAV}                                                                | 21K      |          |            |            |            | ResNet-50        |            | 2048      | 224        | TCGA                             | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/lunit-io/benchmark-ssl-pathology)                                                                                                                                                           |
| [Phikon](https://www.medrxiv.org/content/10.1101/2023.07.21.23292757v2)               | [Owkin](https://www.owkin.com)                                                                    | :white_check_mark: | Jul 2023[\*](https://www.medrxiv.org/content/10.1101/2023.07.21.23292757v1)                           | iBOT                                                                            | 6.1K     | 43M      | 5.6K       | 1440       | 155K       | ViT-B            | 86M        | 768       | 224        | TCGA                             | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/owkin/HistoSSLscaling) [<img src="https://huggingface.co/datasets/huggingface/brand-assets/resolve/main/hf-logo.svg" width="25">](https://huggingface.co/owkin/phikon)                      |
| [CONCH](https://www.nature.com/articles/s41591-024-02856-4)                           | [Mahmood Lab](https://faisal.ai)                                                                  | :white_check_mark: | Jul 2023[\*](https://arxiv.org/abs/2307.12914v1)                                                      | iBOT & vision-language pretraining                                              | 21K      | 16M      |            | 1024       | 80 epochs  | ViT-B            | 86M        | 768       | 224        | proprietary                      | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/mahmoodlab/CONCH) [<img src="https://huggingface.co/datasets/huggingface/brand-assets/resolve/main/hf-logo.svg" width="25">](https://huggingface.co/MahmoodLab/CONCH)                       |
| **[UNI](https://www.nature.com/articles/s41591-024-02857-3)**                         | [Mahmood Lab](https://faisal.ai)                                                                  | :white_check_mark: | Aug 2023[\*](https://arxiv.org/abs/2308.15474v1)                                                      | DINOv2                                                                          | **100K** | 100M     |            |            |            | ViT-L            |            | 1024      | 224        | proprietary (Mass-100K)          | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/mahmoodlab/UNI) [<img src="https://huggingface.co/datasets/huggingface/brand-assets/resolve/main/hf-logo.svg" width="25">](https://huggingface.co/MahmoodLab/UNI)                           |
| **[Virchow](https://arxiv.org/abs/2309.07778)**                                       | [Paige](https://paige.ai)                                                                         | :x:                | Sep 2023[\*](https://arxiv.org/abs/2309.07778v1)                                                      | DINOv2                                                                          | **1.5M** |          | 120K       |            |            | ViT-H            | 632M       | 2560      | 224        | proprietary (from MSKCC)         |
| **[Campanella _et al._](https://arxiv.org/abs/2310.07033)** (MAE)                     | [Thomas Fuchs Lab](https://www.hpims.org/labs/thomas-fuchs-lab/)                                  | :x:                | Oct 2023[\*](https://arxiv.org/abs/2310.07033v1)                                                      | MAE                                                                             | **420K** | 3.3B     | 77K        | 1080       | 1.3K INE   | ViT-L            | 303M       |           | 224        | proprietary (MSHS)               |
| **[Campanella _et al._](https://arxiv.org/abs/2310.07033)** (DINO)                    | [Thomas Fuchs Lab](https://www.hpims.org/labs/thomas-fuchs-lab/)                                  | :x:                | Oct 2023[\*](https://arxiv.org/abs/2310.07033v1)                                                      | DINOv1                                                                          | **420K** | 3.3B     | 77K        | 1440       | 2.5K INE   | ViT-L            | 303M       |           | 224        | proprietary (MSHS)               |
| [PathoDuet](https://arxiv.org/abs/2312.09894)                                         | [Shanghai Jiao Tong University](https://life.sjtu.edu.cn/)                                        | :white_check_mark: | Dec 2023[\*](https://arxiv.org/abs/2312.09894v1)                                                      | inspired by MoCoV3                                                              | 11K      | 13M      |            | 2048       | 100 epochs | ViT-B            |            | 4096      | 224        | TCGA                             | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/openmedlab/PathoDuet)                                                                                                                                                                       |
| **[RudolfV](https://arxiv.org/abs/2401.04079)**                                       | [Aignostics](https://www.aignostics.com)                                                          | :x:                | Jan 2024[\*](https://arxiv.org/abs/2401.04079v1)                                                      | DINOv2                                                                          | **100K** | 750M     | 36K        |            |            | ViT-L            |            |           | 224        | proprietary (from EU & US), TCGA |
| [kaiko](https://arxiv.org/abs/2404.15217)                                             | [kaiko.ai](https://www.kaiko.ai)                                                                  | :white_check_mark: | Mar 2024[\*](https://arxiv.org/abs/2404.15217v1)                                                      | DINOv2                                                                          | 29K      | 256M\*\* |            | 512        | 200 INE    | ViT-L            |            | 1024      | 224        | TCGA                             | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/kaiko-ai/towards_large_pathology_fms)                                                                                                                                                       |
| **[Prov-GigaPath](https://www.nature.com/articles/s41586-024-07441-w)**               | [Microsoft](https://www.microsoft.com/en-us/research/) / [Providence](https://www.providence.org) | :white_check_mark: | May 2024[\*](https://www.nature.com/articles/s41586-024-07441-w)                                      | DINOv2                                                                          | **170K** | 1.4B     | 30K        | 384        |            | ViT              |            | 1536      | 224        | proprietary (Providence)         | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/prov-gigapath/prov-gigapath) [<img src="https://huggingface.co/datasets/huggingface/brand-assets/resolve/main/hf-logo.svg" width="25">](https://huggingface.co/prov-gigapath/prov-gigapath) |
| [BEPH](https://www.biorxiv.org/content/10.1101/2024.05.16.594499)                     | [Shanghai Jiao Tong University](https://life.sjtu.edu.cn/)                                        | :white_check_mark: | May 2024[\*](https://www.biorxiv.org/content/10.1101/2024.05.16.594499v1)                             | BEiTv2                                                                          | 12K      | 12M      |            | 1024       |            | ViT-B            | 193M       | 1024      | 224        | TCGA                             | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/Zhcyoung/BEPH)                                                                                                                                                                              |
| **[Hibou-B](https://arxiv.org/abs/2406.05074)**                                       | [HistAI](https://www.hist.ai)                                                                     | :white_check_mark: | Jun 2024[\*](https://arxiv.org/abs/2406.05074v1)                                                      | DINOv2                                                                          | **1.1M** | 510M     | 310K cases | 1024       | 500K       | ViT-B            | 86M        | 768       | 224        | proprietary                      | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/HistAI/hibou) [<img src="https://huggingface.co/datasets/huggingface/brand-assets/resolve/main/hf-logo.svg" width="25">](https://huggingface.co/histai/hibou-b)                             |
| **[Hibou-L](https://arxiv.org/abs/2406.05074)**                                       | [HistAI](https://www.hist.ai)                                                                     | :x:                | Jun 2024[\*](https://arxiv.org/abs/2406.05074v1)                                                      | DINOv2                                                                          | **1.1M** | 1.2B     | 310K cases | 1024       | 1.2M       | ViT-L            |            | 1024      | 224        | proprietary                      | [<img src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/github.svg" width="20">](https://github.com/HistAI/hibou)                                                                                                                                                                               |

Notes:

- Models trained on >100K slides may be considered foundation models and are marked in **bold**
- \# of WSIs, tiles, and patients are reported to 2 significant figures
- INE = ImageNet epochs
- Order is chronological
- Some of these feature extractors have been evaluated in a benchmarking study for whole slide classification [here](https://arxiv.org/abs/2311.11772).
- \*\* means inferred from other numbers provided in the paper
