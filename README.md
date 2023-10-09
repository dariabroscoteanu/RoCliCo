# A Novel Contrastive Learning Method for Clickbait Detection on RoCliCo: A Romanian Clickbait Corpus of News Articles
## 1. Description 
### General Information
The RoCliCo dataset contains 8,313 news samples which are manually annotated with clickbait and non-clickbait labels. The dataset is divided into two subsets, as presented in the following table:
| Subset      | Clickbait      | Non-clickbait  | Total  |
|-------------|----------------|-----------------|--------|
| Train       | 3,279          | 3,527           | 6,806  |
| Test        | 441            | 1,066           | 1,507  |
| **Total**   | **3,720**      | **4,593**       | **8,313** |

We conduct experiments with four machine learning methods:

- Random Forest and SVM based on handcrafted features
- BiLSTM
- Fine-tuned Ro-BERT
- Contrastive Ro-BERT

We also carry out experiments with a weighted voting ensemble. Among the considered baselines, we propose a novel BERT-based contrastive learning model that learns to encode news titles and contents into a deep metric space such that titles and contents of non-clickbait news have high cosine similarity. In contrast, titles and contents of clickbait news have low cosine similarity. 

Our contribution is twofold:

- We introduce the first publicly available corpus of Romanian news articles comprising manually annotated clickbait and non-clickbait samples.
- We propose a novel clickbait detection model based on learning a deep metric space where news titles and contents are jointly represented. In the shared embedding space, titles and contents of non-clickbait news are supposed to be neighbors, while titles and contents of clickbait news should be

### Data Organization
The data set is divided into two archives, corresponding to the two subsets for training and testing, keeping source separation between training and test. In each archive, there are three JSON files. Each file contains articles collected from only one website. 

A sample in any of the JSON files contains these three elements:
- title - the title of the article
- Content - the body of the article
- category - clickbait/nonclickbait

## 2. Citation

## 3. License 
