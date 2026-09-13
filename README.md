# Multimodal Knowledge Graph Construction: Companion Repository

An awesome-style, curated and categorized reading list accompanying the survey **"Multimodal Knowledge Graph Construction: A Survey of Methods, Modalities, and Open Challenges"** (A. Janakiraman and B. Ghoraani, Florida Atlantic University). It contains every one of the 118 references in the survey's corpus, classified by research area, contribution type, and modality coverage, together with the modality-coverage matrix, the dataset limitation notes, the cross-task comparison criteria, and the reporting checklist proposed in the survey. Contributions (corrections, additions, new benchmarks and evaluation protocols) are welcome via pull request.

Modality codes: **T** text, **I** image, **A** audio, **V** video, **B** table, **S** graph structure only. Document-centric methods that read tables as page layout are marked T,I,B, following Fig. 4 of the survey. Links are given for arXiv preprints; for published works please use the venue and year.

## Contents
- [Corpus at a glance](#corpus-at-a-glance)
- [Reading list by research area](#reading-list-by-research-area)
- [Modality-coverage matrix](#modality-coverage-matrix)
- [Datasets and their limitations](#datasets-and-their-limitations)
- [Cross-task comparison criteria](#cross-task-comparison-criteria)
- [Reporting checklist for construction papers](#reporting-checklist-for-construction-papers)
- [Machine-readable classification](#machine-readable-classification)

## Corpus at a glance

- 118 references: 86 primary works across six research areas, 7 prior surveys, 25 foundational references.
- Primary works by contribution type: 9 construction pipelines/methods, 24 extraction/parsing components, 20 completion/representation/alignment methods, 21 datasets/benchmarks/resources, 8 retrieval/reasoning systems, 4 transfer methods.
- Modality coverage of primary works: 22 text/structure only; 43 text+image; 13 three or more modalities; none covers all five (TIVA-KG, with four, is the widest).
- Preprints among primary works: 13 (all 2024 or later); please check them against final proceedings.

## Reading list by research area

### Prior surveys

- **Knowledge Graph Embedding: A Survey of Approaches and Applications** — Wang et al., *IEEE Transactions on Knowledge and Data Engineering*, 2017. `survey` · modalities: S
- **A Comprehensive Survey on Automatic Knowledge Graph Construction** — Zhong et al., *ACM Computing Surveys*, 2023. `survey` · modalities: T
- **A Survey on Knowledge-Enhanced Multimodal Learning** — Lymperaiou et al., *Artificial Intelligence Review*, 2024. `survey` · modalities: T,I
- **Knowledge Graphs Meet Multi-Modal Learning: A Comprehensive Survey** — Chen et al., *arXiv preprint arXiv:2402.05391*, 2024. `survey` · modalities: T,I [[arXiv]](https://arxiv.org/abs/2402.05391)
- **Multi-Modal Knowledge Graph Construction and Application: A Survey** — Zhu et al., *IEEE Transactions on Knowledge and Data Engineering*, 2024. `survey` · modalities: T,I
- **LLM-Empowered Knowledge Graph Construction: A Survey** — Bian, *arXiv preprint arXiv:2510.20345*, 2025. `survey` · modalities: T [[arXiv]](https://arxiv.org/abs/2510.20345)
- **A Survey of Graph Retrieval-Augmented Generation for Customized Large Language Models** — Zhang et al., *arXiv preprint arXiv:2501.13958*, 2025. `survey` · modalities: T [[arXiv]](https://arxiv.org/abs/2501.13958)

### Foundations: encyclopedic graphs, embedding models, modality encoders, parameter-efficient adaptation

- **DBpedia: A Nucleus for a Web of Open Data** — Auer et al., *Proc. ISWC/ASWC*, 2007. `knowledge graph resource` · modalities: T
- **YAGO: A Core of Semantic Knowledge** — Suchanek et al., *Proc. WWW*, 2007. `knowledge graph resource` · modalities: T
- **Freebase: A Collaboratively Created Graph Database for Structuring Human Knowledge** — Bollacker et al., *Proc. ACM SIGMOD*, 2008. `knowledge graph resource` · modalities: T
- **Translating Embeddings for Modeling Multi-relational Data** — Bordes et al., *Proc. NeurIPS*, 2013. `completion/representation/alignment` · modalities: S
- **Wikidata: A Free Collaborative Knowledgebase** — Vrandevcic, *Communications of the ACM*, 2014. `knowledge graph resource` · modalities: T
- **Observed versus Latent Features for Knowledge Base and Text Inference** — Toutanova et al., *Proc. Workshop on Continuous Vector Space Models and their Compositionality*, 2015. `dataset/benchmark/resource` · modalities: S
- **Embedding Entities and Relations for Learning and Inference in Knowledge Bases** — Yang et al., *Proc. ICLR*, 2015. `completion/representation/alignment` · modalities: S
- **Complex Embeddings for Simple Link Prediction** — Trouillon et al., *Proc. ICML*, 2016. `completion/representation/alignment` · modalities: S
- **Audio Set: An Ontology and Human-Labeled Dataset for Audio Events** — Gemmeke et al., *Proc. IEEE ICASSP*, 2017. `dataset/benchmark/resource` · modalities: A
- **Visual Genome: Connecting Language and Vision Using Crowdsourced Dense Image Annotations** — Krishna et al., *International Journal of Computer Vision*, 2017. `dataset/benchmark/resource` · modalities: T,I
- **Convolutional 2D Knowledge Graph Embeddings (ConvE)** — Dettmers et al., *Proc. AAAI*, 2018. `completion/representation/alignment` · modalities: S
- **Parameter-Efficient Transfer Learning for NLP** — Houlsby et al., *Proc. ICML*, 2019. `transfer method` · modalities: T
- **RotatE: Knowledge Graph Embedding by Relational Rotation in Complex Space** — Sun et al., *Proc. ICLR*, 2019. `completion/representation/alignment` · modalities: S
- **wav2vec 2.0: A Framework for Self-Supervised Learning of Speech Representations** — Baevski et al., *Proc. NeurIPS*, 2020. `modality encoder (enabler)` · modalities: A
- **Knowledge Graphs** — Hogan et al., *ACM Computing Surveys*, 2021. `survey` · modalities: S
- **The Power of Scale for Parameter-Efficient Prompt Tuning** — Lester et al., *Proc. EMNLP*, 2021. `transfer method` · modalities: T
- **Learning Transferable Visual Models from Natural Language Supervision** — Radford et al., *Proc. ICML*, 2021. `modality encoder (enabler)` · modalities: T,I
- **LoRA: Low-Rank Adaptation of Large Language Models** — Hu et al., *Proc. ICLR*, 2022. `transfer method` · modalities: T
- **A Survey on Knowledge Graphs: Representation, Acquisition, and Applications** — Ji et al., *IEEE Transactions on Neural Networks and Learning Systems*, 2022. `survey` · modalities: S
- **CLAP: Learning Audio Concepts from Natural Language Supervision** — Elizalde et al., *Proc. IEEE ICASSP*, 2023. `modality encoder (enabler)` · modalities: A,T
- **ImageBind: One Embedding Space to Bind Them All** — Girdhar et al., *Proc. IEEE/CVF CVPR*, 2023. `modality encoder (enabler)` · modalities: T,I,A
- **BLIP-2: Bootstrapping Language-Image Pre-training with Frozen Image Encoders and Large Language Models** — Li et al., *Proc. ICML*, 2023. `modality encoder (enabler)` · modalities: T,I
- **Visual Instruction Tuning** — Liu et al., *Proc. NeurIPS*, 2023. `modality encoder (enabler)` · modalities: T,I
- **Robust Speech Recognition via Large-Scale Weak Supervision** — Radford et al., *Proc. ICML*, 2023. `modality encoder (enabler)` · modalities: A,T
- **Video-LLaMA: An Instruction-tuned Audio-Visual Language Model for Video Understanding** — Zhang et al., *Proc. EMNLP System Demonstrations*, 2023. `modality encoder (enabler)` · modalities: T,A,V

### 1. Text-based and LLM-driven construction

- **Leveraging Linguistic Structure for Open Domain Information Extraction** — Angeli et al., *Proc. ACL*, 2015. `extraction/parsing component` · modalities: T
- **DocRED: A Large-Scale Document-Level Relation Extraction Dataset** — Yao et al., *Proc. ACL*, 2019. `dataset/benchmark/resource` · modalities: T
- **REBEL: Relation Extraction By End-to-end Language generation** — Huguet Cabot et al., *Findings of EMNLP*, 2021. `extraction/parsing component` · modalities: T
- **Document-Level Relation Extraction with Adaptive Thresholding and Localized Context Pooling** — Zhou et al., *Proc. AAAI*, 2021. `extraction/parsing component` · modalities: T
- **Revisiting DocRED -- Addressing the False Negative Problem in Relation Extraction** — Tan et al., *Proc. EMNLP*, 2022. `dataset/benchmark/resource` · modalities: T
- **LLMs4OL: Large Language Models for Ontology Learning** — Babaei Giglou et al., *Proc. ISWC*, 2023. `construction pipeline/method` · modalities: T
- **Text2KGBench: A Benchmark for Ontology-Driven Knowledge Graph Generation from Text** — Mihindukulasooriya et al., *Proc. ISWC*, 2023. `dataset/benchmark/resource` · modalities: T
- **SAC-KG: Exploiting Large Language Models as Skilled Automatic Constructors for Domain Knowledge Graph** — Chen et al., *Proc. ACL*, 2024. `construction pipeline/method` · modalities: T
- **KAG: Boosting LLMs in Professional Domains via Knowledge Augmented Generation** — Liang et al., *arXiv preprint arXiv:2409.13731*, 2024. `construction pipeline/method` · modalities: T [[arXiv]](https://arxiv.org/abs/2409.13731)
- **AutoSchemaKG: Autonomous Knowledge Graph Construction through Dynamic Schema Induction from Web-Scale Corpora** — Bai et al., *arXiv preprint arXiv:2505.23628*, 2025. `construction pipeline/method` · modalities: T [[arXiv]](https://arxiv.org/abs/2505.23628)
- **NLP-AKG: Few-Shot Construction of NLP Academic Knowledge Graph Based on LLM** — Lan et al., *arXiv preprint arXiv:2502.14192*, 2025. `construction pipeline/method` · modalities: T [[arXiv]](https://arxiv.org/abs/2502.14192)
- **Beyond Predefined Schemas: TRACE-KG for Context-Enriched Knowledge Graphs from Complex Documents** — Abolhasani et al., *arXiv preprint arXiv:2604.03496*, 2026. `construction pipeline/method` · modalities: T [[arXiv]](https://arxiv.org/abs/2604.03496)

### 2. Document-centric understanding

- **LayoutLM: Pre-training of Text and Layout for Document Image Understanding** — Xu et al., *Proc. ACM SIGKDD*, 2020. `extraction/parsing component` · modalities: T,I,B
- **DocVQA: A Dataset for VQA on Document Images** — Mathew et al., *Proc. IEEE/CVF WACV*, 2021. `dataset/benchmark/resource` · modalities: T,I,B
- **LayoutLMv2: Multi-modal Pre-training for Visually-Rich Document Understanding** — Xu et al., *Proc. ACL*, 2021. `extraction/parsing component` · modalities: T,I,B
- **LayoutLMv3: Pre-training for Document AI with Unified Text and Image Masking** — Huang et al., *Proc. ACM Multimedia*, 2022. `extraction/parsing component` · modalities: T,I,B
- **OCR-Free Document Understanding Transformer (Donut)** — Kim et al., *Proc. ECCV*, 2022. `extraction/parsing component` · modalities: T,I,B
- **LiLT: A Simple yet Effective Language-Independent Layout Transformer for Structured Document Understanding** — Wang et al., *Proc. ACL*, 2022. `extraction/parsing component` · modalities: T,I,B
- **mPLUG-DocOwl 1.5: Unified Structure Learning for OCR-free Document Understanding** — Hu et al., *arXiv preprint arXiv:2403.12895*, 2024. `extraction/parsing component` · modalities: T,I,B [[arXiv]](https://arxiv.org/abs/2403.12895)
- **LayoutLLM: Layout Instruction Tuning with Large Language Models for Document Understanding** — Luo et al., *Proc. IEEE/CVF CVPR*, 2024. `extraction/parsing component` · modalities: T,I,B
- **Nougat: Neural Optical Understanding for Academic Documents** — Blecher et al., *Proc. ICLR*, 2024. `extraction/parsing component` · modalities: T,I,B
- **Docs2KG: A Human-LLM Collaborative Approach to Unified Knowledge Graph Construction from Heterogeneous Documents** — Sun et al., *Companion Proc. ACM Web Conference (WWW)*, 2025. `construction pipeline/method` · modalities: T,I,B

### 3a. Text and image: extraction and grounding

- **Visual Attention Model for Name Tagging in Multimodal Social Media** — Lu et al., *Proc. ACL*, 2018. `extraction/parsing component` · modalities: T,I
- **Multimodal Named Entity Recognition for Short Social Media Posts** — Moon et al., *Proc. NAACL-HLT*, 2018. `extraction/parsing component` · modalities: T,I
- **Improving Multimodal Named Entity Recognition via Entity Span Detection with Unified Multimodal Transformer** — Yu et al., *Proc. ACL*, 2020. `extraction/parsing component` · modalities: T,I
- **MNRE: A Challenge Multimodal Dataset for Neural Relation Extraction with Visual Evidence in Social Media Posts** — Zheng et al., *Proc. IEEE ICME*, 2021. `dataset/benchmark/resource` · modalities: T,I
- **Multimodal Relation Extraction with Efficient Graph Alignment** — Zheng et al., *Proc. ACM Multimedia*, 2021. `extraction/parsing component` · modalities: T,I
- **Good Visual Guidance Makes A Better Extractor: Hierarchical Visual Prefix for Multimodal Entity and Relation Extraction** — Chen et al., *Findings of NAACL*, 2022. `extraction/parsing component` · modalities: T,I
- **Hybrid Transformer with Multi-level Fusion for Multimodal Knowledge Graph Completion (MKGformer)** — Chen et al., *Proc. ACM SIGIR*, 2022. `completion/representation/alignment` · modalities: T,I
- **ITA: Image-Text Alignments for Multi-Modal Named Entity Recognition** — Wang et al., *Proc. NAACL-HLT*, 2022. `extraction/parsing component` · modalities: T,I
- **MORE: A Multimodal Object-Entity Relation Extraction Dataset with a Benchmark Evaluation** — He et al., *Proc. ACM Multimedia*, 2023. `dataset/benchmark/resource` · modalities: T,I
- **Grounded Multimodal Named Entity Recognition on Social Media** — Yu et al., *Proc. ACL*, 2023. `dataset/benchmark/resource` · modalities: T,I
- **Continual Multimodal Knowledge Graph Construction** — Chen et al., *Proc. IJCAI*, 2024. `construction pipeline/method` · modalities: T,I
- **LLMs as Bridges: Reformulating Grounded Multimodal Named Entity Recognition** — Li et al., *IEEE Transactions on Multimedia*, 2025. `extraction/parsing component` · modalities: T,I
- **Aligning Vision to Language: Annotation-Free Multimodal Knowledge Graph Construction for Enhanced LLMs Reasoning (VaLiK)** — Liu et al., *Proc. IEEE/CVF ICCV*, 2025. `construction pipeline/method` · modalities: T,I
- **Collaborative Multi-LoRA Experts with Achievement-Based Multi-Tasks Loss for Unified Multimodal Information Extraction** — Yuan et al., *Proc. IJCAI*, 2025. `extraction/parsing component` · modalities: T,I
- **REMOTE: A Unified Multimodal Relation Extraction Framework with Multilevel Optimal Transport and Mixture-of-Experts** — Lin et al., *Proc. ACM Multimedia*, 2025. `extraction/parsing component` · modalities: T,I

### 3b. Text and image: representation, completion, and alignment

- **Image-Embodied Knowledge Representation Learning** — Xie et al., *Proc. IJCAI*, 2017. `completion/representation/alignment` · modalities: T,I
- **Multimodal Data Enhanced Representation Learning for Knowledge Graphs (TransAE)** — Wang et al., *Proc. IJCNN*, 2019. `completion/representation/alignment` · modalities: T,I
- **Visual Pivoting for (Unsupervised) Entity Alignment (EVA)** — Liu et al., *Proc. AAAI*, 2021. `completion/representation/alignment` · modalities: T,I
- **Is Visual Context Really Helpful for Knowledge Graph? A Representation Learning Perspective (RSME)** — Wang et al., *Proc. ACM Multimedia*, 2021. `completion/representation/alignment` · modalities: T,I
- **OTKGE: Multi-modal Knowledge Graph Embeddings via Optimal Transport** — Cao et al., *Proc. NeurIPS*, 2022. `completion/representation/alignment` · modalities: T,I
- **Multi-modal Contrastive Representation Learning for Entity Alignment (MCLEA)** — Lin et al., *Proc. COLING*, 2022. `completion/representation/alignment` · modalities: T,I
- **Relation-Enhanced Negative Sampling for Multimodal Knowledge Graph Completion** — Xu et al., *Proc. ACM Multimedia*, 2022. `completion/representation/alignment` · modalities: T,I
- **MoSE: Modality Split and Ensemble for Multimodal Knowledge Graph Completion** — Zhao et al., *Proc. EMNLP*, 2022. `completion/representation/alignment` · modalities: T,I
- **MEAformer: Multi-modal Entity Alignment Transformer for Meta Modality Hybrid** — Chen et al., *Proc. ACM Multimedia*, 2023. `completion/representation/alignment` · modalities: T,I
- **VISTA: Visual-Textual Knowledge Graph Representation Learning** — Lee et al., *Findings of EMNLP*, 2023. `completion/representation/alignment` · modalities: T,I
- **IMF: Interactive Multimodal Fusion Model for Link Prediction** — Li et al., *Proc. ACM Web Conference (WWW)*, 2023. `completion/representation/alignment` · modalities: T,I
- **Unleashing the Power of Imbalanced Modality Information for Multi-modal Knowledge Graph Completion (AdaMF-MAT)** — Zhang et al., *Proc. LREC-COLING*, 2024. `completion/representation/alignment` · modalities: T,I
- **NativE: Multi-modal Knowledge Graph Completion in the Wild** — Zhang et al., *Proc. ACM SIGIR*, 2024. `completion/representation/alignment` · modalities: T,I
- **DiffusionCom: Structure-Aware Multimodal Diffusion Model for Multimodal Knowledge Graph Completion** — Huang et al., *arXiv preprint arXiv:2504.06543*, 2025. `completion/representation/alignment` · modalities: T,I [[arXiv]](https://arxiv.org/abs/2504.06543)
- **Mixed-Curvature Multi-Modal Knowledge Graph Completion** — Gao et al., *Proc. AAAI*, 2025. `completion/representation/alignment` · modalities: T,I
- **HERGC: Heterogeneous Experts Representation and Generative Completion for Multimodal Knowledge Graphs** — Xiao et al., *arXiv preprint arXiv:2506.00826*, 2025. `completion/representation/alignment` · modalities: T,I [[arXiv]](https://arxiv.org/abs/2506.00826)
- **Noise-Powered Multi-Modal Knowledge Graph Representation Framework** — Chen et al., *Proc. COLING*, 2025. `completion/representation/alignment` · modalities: T,I
- **Multiple Heads Are Better Than One: Mixture of Modality Knowledge Experts for Entity Representation Learning (MoMoK)** — Zhang et al., *Proc. ICLR*, 2025. `completion/representation/alignment` · modalities: T,I
- **Tokenization, Fusion, and Augmentation: Towards Fine-Grained Multimodal Entity Representation (MyGO)** — Zhang et al., *Proc. AAAI*, 2025. `completion/representation/alignment` · modalities: T,I

### 4. Beyond the image: audio, video, tables (and clinical resources)

- **Compositional Semantic Parsing on Semi-Structured Tables** — Pasupat et al., *Proc. ACL*, 2015. `dataset/benchmark/resource` · modalities: T,B
- **Video Visual Relation Detection** — Shang et al., *Proc. ACM Multimedia*, 2017. `extraction/parsing component` · modalities: V
- **MIMIC-CXR, a De-identified Publicly Available Database of Chest Radiographs with Free-text Reports** — Johnson et al., *Scientific Data*, 2019. `dataset/benchmark/resource` · modalities: T,I
- **MMKG: Multi-Modal Knowledge Graphs** — Liu et al., *Proc. ESWC*, 2019. `dataset/benchmark/resource` · modalities: T,I
- **TabFact: A Large-scale Dataset for Table-based Fact Verification** — Chen et al., *Proc. ICLR*, 2020. `dataset/benchmark/resource` · modalities: T,B
- **TURL: Table Understanding through Representation Learning** — Deng et al., *Proc. VLDB Endowment*, 2020. `extraction/parsing component` · modalities: T,B
- **TaPas: Weakly Supervised Table Parsing via Pre-training** — Herzig et al., *Proc. ACL*, 2020. `extraction/parsing component` · modalities: T,B
- **Richpedia: A Large-Scale, Comprehensive Multi-Modal Knowledge Graph** — Wang et al., *Big Data Research*, 2020. `dataset/benchmark/resource` · modalities: T,I
- **TaBERT: Pretraining for Joint Understanding of Textual and Tabular Data** — Yin et al., *Proc. ACL*, 2020. `extraction/parsing component` · modalities: T,B
- **VisualSem: A High-Quality Knowledge Graph for Vision and Language** — Alberts et al., *Proc. Workshop on Multilingual Representation Learning (EMNLP)*, 2021. `dataset/benchmark/resource` · modalities: T,I
- **FinQA: A Dataset of Numerical Reasoning over Financial Data** — Chen et al., *Proc. EMNLP*, 2021. `dataset/benchmark/resource` · modalities: T,B
- **RadGraph: Extracting Clinical Entities and Relations from Radiology Reports** — Jain et al., *Proc. NeurIPS Datasets and Benchmarks Track*, 2021. `dataset/benchmark/resource` · modalities: T
- **MultiModalQA: Complex Question Answering over Text, Tables and Images** — Talmor et al., *Proc. ICLR*, 2021. `dataset/benchmark/resource` · modalities: T,I,B
- **TAT-QA: A Question Answering Benchmark on a Hybrid of Tabular and Textual Content in Finance** — Zhu et al., *Proc. ACL*, 2021. `dataset/benchmark/resource` · modalities: T,B
- **Building a Knowledge Graph to Enable Precision Medicine** — Chandak et al., *Scientific Data*, 2023. `dataset/benchmark/resource` · modalities: T
- **TIVA-KG: A Multimodal Knowledge Graph with Text, Image, Video and Audio** — Wang et al., *Proc. ACM Multimedia*, 2023. `dataset/benchmark/resource` · modalities: T,I,A,V
- **VAT-KG: Knowledge-Intensive Multimodal Knowledge Graph Dataset for Retrieval-Augmented Generation** — Park et al., *arXiv preprint arXiv:2506.21556*, 2025. `dataset/benchmark/resource` · modalities: T,I,A [[arXiv]](https://arxiv.org/abs/2506.21556)

### 5. Reasoning, KGQA, and GraphRAG

- **OK-VQA: A Visual Question Answering Benchmark Requiring External Knowledge** — Marino et al., *Proc. IEEE/CVF CVPR*, 2019. `dataset/benchmark/resource` · modalities: T,I
- **MuKEA: Multimodal Knowledge Extraction and Accumulation for Knowledge-based Visual Question Answering** — Ding et al., *Proc. IEEE/CVF CVPR*, 2022. `retrieval/reasoning system` · modalities: T,I
- **From Local to Global: A Graph RAG Approach to Query-Focused Summarization** — Edge et al., *arXiv preprint arXiv:2404.16130*, 2024. `retrieval/reasoning system` · modalities: T [[arXiv]](https://arxiv.org/abs/2404.16130)
- **LightRAG: Simple and Fast Retrieval-Augmented Generation** — Guo et al., *arXiv preprint arXiv:2410.05779*, 2024. `retrieval/reasoning system` · modalities: T [[arXiv]](https://arxiv.org/abs/2410.05779)
- **HippoRAG: Neurobiologically Inspired Long-Term Memory for Large Language Models** — Gutierrez et al., *Proc. NeurIPS*, 2024. `retrieval/reasoning system` · modalities: T
- **KnowGPT: Knowledge Graph Based Prompting for Large Language Models** — Zhang et al., *Proc. NeurIPS*, 2024. `retrieval/reasoning system` · modalities: T
- **MMGraphRAG: Bridging Vision and Language with Interpretable Multimodal Knowledge Graphs** — Wan et al., *arXiv preprint arXiv:2507.20804*, 2025. `retrieval/reasoning system` · modalities: T,I [[arXiv]](https://arxiv.org/abs/2507.20804)
- **MegaRAG: Multimodal Knowledge Graph-Based Retrieval Augmented Generation** — Hsiao et al., *arXiv preprint arXiv:2512.20626*, 2026. `retrieval/reasoning system` · modalities: T,I [[arXiv]](https://arxiv.org/abs/2512.20626)
- **MG\textsuperscript2-RAG: Multi-Granularity Graph for Multimodal Retrieval-Augmented Generation** — Dai et al., *arXiv preprint arXiv:2604.04969*, 2026. `retrieval/reasoning system` · modalities: T,I [[arXiv]](https://arxiv.org/abs/2604.04969)

### 6. Transfer and domain adaptation

- **Structure Pretraining and Prompt Tuning for Knowledge Graph Transfer** — Zhang et al., *Proc. ACM Web Conference (WWW)*, 2023. `transfer method` · modalities: S
- **LLM-based Multi-Level Knowledge Generation for Few-shot Knowledge Graph Completion** — Li et al., *Proc. IJCAI*, 2024. `transfer method` · modalities: T
- **Multi-Domain Graph Foundation Models: Robust Knowledge Transfer via Topology Alignment** — Wang et al., *Proc. ICML*, 2025. `transfer method` · modalities: S
- **MLDGG: Meta-Learning for Domain Generalization on Graphs** — Tian et al., *Proc. ACM SIGKDD*, 2025. `transfer method` · modalities: S

## Modality-coverage matrix

Each family is represented by its most modality-extensive member (rule R4 of the survey), so the matrix over-states rather than under-states coverage. Within the surveyed corpus, no dataset, method, or pipeline spans all five modalities.

| Work | Type | Text | Image | Audio | Video | Table |
|---|---|:-:|:-:|:-:|:-:|:-:|
| DocRED | text dataset | ✓ |  |  |  |  |
| REBEL | extraction method | ✓ |  |  |  |  |
| GraphRAG | retrieval system | ✓ |  |  |  |  |
| MNRE | multimodal dataset | ✓ | ✓ |  |  |  |
| GMNER / RiVEG | grounded MNER method | ✓ | ✓ |  |  |  |
| MyGO / MoMoK | completion method | ✓ | ✓ |  |  |  |
| MMKG / Richpedia | datasets | ✓ | ✓ |  |  |  |
| VTKG (VISTA) | visual-triple dataset | ✓ | ✓ |  |  |  |
| MMGraphRAG | multimodal RAG system | ✓ | ✓ |  |  |  |
| LayoutLMv3 | document-AI method | ✓ | ✓ |  |  | ✓ |
| Docs2KG | construction pipeline | ✓ | ✓ |  |  | ✓ |
| MultiModalQA | QA benchmark | ✓ | ✓ |  |  | ✓ |
| VAT-KG | pipeline + dataset | ✓ | ✓ | ✓ |  |  |
| ImageBind | cross-modal encoder (enabler) | ✓ | ✓ | ✓ |  |  |
| Video-LLaMA | audio-visual encoder (enabler) | ✓ |  | ✓ | ✓ |  |
| TIVA-KG | four-modality dataset | ✓ | ✓ | ✓ | ✓ |  |

## Datasets and their limitations

| Dataset / resource | Year | Modalities | Basis | Primary use | Limitations / remarks |
|---|---|---|---|---|---|
| DocRED / Re-DocRED | 2019/22 | T | Wikipedia documents | Document-level relation extraction | Text only; Wikipedia domain; distantly supervised labels with substantial false negatives, partly repaired by Re-DocRED; evidence at sentence level; no media. |
| MMKG (FB15k / DB15k / YAGO15k) | 2019 | T,I | Encyclopedic graphs + numeric literals, images | Completion; entity alignment | Entity-level images retrieved from the web for existing graph entities; built for completion and alignment, not construction; no source documents. |
| Richpedia | 2020 | T,I | Wikidata entities + web images | Large-scale image-entity association | Entity-level image links only; no relation-level grounding; web images of variable relevance to the entity. |
| VisualSem | 2021 | T,I | BabelNet-filtered concepts + curated images | Vision-language grounding | Concept nodes with curated images and glosses; entity-level; derived from existing lexical resources rather than documents. |
| MNRE | 2021 | T,I | Twitter posts | Multimodal relation extraction | Short posts; small closed relation set; social-media domain only; relations hold between text entities, with entity-level image use. |
| GMNER | 2023 | T,I | Twitter posts + boxes | Grounded multimodal NER | Twitter domain; boxes ground entities, not relations; some entities have no visual referent; short text. |
| MORE | 2023 | T,I | News articles + images | Object-entity relation extraction | News domain; relations between image objects and text entities; no persistent graph and no cross-document identity. |
| VTKG (VISTA) | 2023 | T,I | Entity- and triple-level images | Multimodal completion | Images attached to entities and triples of an existing graph; image only beyond text; built for completion. |
| TIVA-KG | 2023 | T,I,A,V | ConceptNet topology + retrieved media | Completion with triplet grounding | Topology inherited from ConceptNet; media retrieved for existing facts rather than extracted from documents; no tables; evaluated on completion only. |
| VAT-KG | 2025 | T,I,A | Curated audio-visual datasets, concept-aligned | Multimodal RAG | Concept-centric; built by filtering curated audio-visual datasets; no video or tables; preprint at the time of writing. |
| Text2KGBench | 2023 | T | Ontology-paired corpora | Construction benchmarking | Text only; sentence-level generation against a given ontology; no schema induction and no multimodal input. |
| MIMIC-CXR + RadGraph | 2019/21 | T,I | Chest radiographs + reports; clinical schema | Clinical graph construction | Text and image only (no audio, tables, or video released); no region-level grounding of report entities; single-institution images; negation and uncertainty must be modeled; credentialed access. |
| PrimeKG | 2023 | T | Integrated biomedical sources | Precision-medicine analysis | Integrates curated sources; no raw documents and no media; construction is source integration, not extraction. |
| TabFact / WTQ / TAT-QA / FinQA | 2015–21 | T,B | Web and financial tables | Table QA and verification | QA or verification labels rather than graphs; tables from Wikipedia and financial reports; many answers require arithmetic over cells; nothing is persisted. |
| MultiModalQA / DocVQA | 2021 | T,I,B | Joint text-table-image; document images | Multimodal document QA | QA labels only; no graph; DocVQA tables exist only as pixels; MultiModalQA composes Wikipedia tables, text, and images. |
| AudioSet | 2017 | A | Ontology of audio events | Audio perception (enabler) | Clip-level sound-event labels on ten-second web-video clips; an ontology of sounds, not of entities or relations; not linked to a graph. |
| Visual Genome | 2017 | T,I | Dense scene-graph annotations | Scene-graph grounding (enabler) | Scene graphs over single images with objects canonicalized to WordNet synsets; closed to image content; no cross-document entity identity. |

## Cross-task comparison criteria

The survey compares its six research areas under seven structural criteria rather than by performance numbers, because the areas report incomparable metrics on incomparable data.

| Research area | Input assumed | Output produced | Schema regime | Grounding granularity | Customary metric | Modalities | Transfer evidence |
|---|---|---|---|---|---|---|---|
| Text and LLM-based construction | Raw text (documents, corpora) | Triple set or persistent graph | Fixed (DocRED, Text2KGBench) or induced (AutoSchemaKG) | Text span, where reported | Triple P/R/F1; ontology conformance | T | Within-domain only |
| Document-centric understanding | Page images, PDFs | Fields, markup, answers; a graph in Docs2KG | Fixed per task; ad hoc in Docs2KG | Token and region level | Field F1; ANLS (DocVQA) | T,I,B | Layout transfer across languages (LiLT) |
| Text+image: extraction and grounding | Short text with an image | Typed spans, relations, boxes | Fixed label sets | Entity level (boxes) | Span and relation F1 | T,I | Single benchmark per method |
| Text+image: representation and completion | Existing graph with aligned media | Scores over candidate triples; embeddings | Inherited from the graph | Entity level; triple level in VTKG | MRR, Hits@k (filtered) | T,I | Not reported |
| Beyond image: audio, video, tables | Curated media, tables, or an existing graph | Graph resource; QA answers | Inherited (ConceptNet) or none (table QA) | Triple level (TIVA-KG); cell level (table QA) | MRR, Hits@k; QA accuracy | T,I,A,V,B across the area; no single work covers all five | Not reported |
| Reasoning, QA, and GraphRAG | Corpus and query | Answer, with an ephemeral graph | Open; induced by the LLM per corpus | Passage level at best | QA accuracy; LLM-judged quality | T, (I) | Per corpus; none across domains |
| Transfer and domain adaptation | Source and target graphs | Adapted model | Inherited | None | Gain on the target task | structure, T | Structure-only transfer |

## Reporting checklist for construction papers

Pending shared benchmarks, the survey proposes that construction papers report a minimal common set so that results become comparable:

- **P1. Input assumption and modalities.** Raw documents, semi-structured input, or an existing graph; the modalities consumed.
- **P2. Triple-level precision, recall, and F1** against a gold graph, stating the procedure used to align predicted and reference vocabularies when the schema is induced.
- **P3. Grounding accuracy per modality.** The fraction of emitted triples whose locators (text span, image region, audio/video interval, table cell) are judged to support them.
- **P4. Hallucination and omission rates**, with the sampling and adjudication procedure used to estimate them.
- **P5. Schema statistics.** Number of induced types, fraction merged as duplicates, and consistency across runs.
- **P6. Transfer.** Where transfer is claimed, paired results on at least two domains with a component-level transferability profile (each component frozen vs. re-tuned).

Standardized evaluation protocols and full-modality construction benchmarks are future work; this repository is intended to host them as they appear.

## Machine-readable classification

`corpus_classification.csv` lists every reference with its BibTeX key, title, year, venue, peer-review status, research area, contribution type, and modalities. `refs.bib` is the survey's bibliography.

## Citation

If you use this list, please cite the survey (full citation to be added upon publication).

## License

This repository (README, classification, and notes) is released under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0). The cited papers remain under their own licenses.
