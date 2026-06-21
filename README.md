# Projet de Fin de Module : Deep Learning (EMSI 2025-2026)

Ce projet présente la conception, l'implémentation, la comparaison et l'analyse critique de modèles de Deep Learning pour trois types de données :
1. **Données tabulaires** avec un MLP (Partie I) sur le dataset *Breast Cancer Wisconsin* (sain vs cancéreux).
2. **Données d'images** avec un CNN (Partie II) sur *MNIST*, y compris des opérations de convolution et pooling codées manuellement en Numpy vs PyTorch, et une étude d'ablation.
3. **Données séquentielles** avec des modèles RNN / LSTM / GRU / Seq2Seq (Partie III) sur un dataset de traduction *English-French* (Tatoeba).

Chaque partie a été restructurée selon une structure logique rigoureuse en 9 étapes pour garantir la reproductibilité et la clarté pédagogique.

---

## Structure Réelle du Projet

Le projet est organisé comme suit à la racine du dossier :

```
Projet_DL/
│
├── requirements.txt            # Dépendances Python nécessaires (dont PyTorch et SHAP)
├── README.md                   # Ce fichier d'introduction et guide du projet
│
├── Notebook_01_MLP.ipynb       # Partie I : MLP, initialisation des poids, learning rate scheduler, plots d'exploration et SHAP
├── Notebook_02_CNN.ipynb       # Partie II : Numpy vs PyTorch, CNN LeNet-5 configurable, ablation et feature maps
├── Notebook_03_RNN_Seq2Seq.ipynb # Partie III : Comparaison RNN/LSTM/GRU, gradient clipping et traducteur Seq2Seq (Greedy vs Beam Search)
│
├── data/                       # Dossier contenant les datasets téléchargés (MNIST, Tatoeba)
├── figures/                    # Dossier contenant tous les graphiques et courbes générés par les notebooks
├── models/                     # Dossier contenant le meilleur modèle MLP sauvegardé (.pth)
└── results/                    # Dossier contenant les paires de phrases traduites en sortie du Seq2Seq
```

---

## Installation et Configuration

Pour exécuter le projet, installez d'abord les dépendances nécessaires. Assurez-vous d'avoir Python 3.8+ d'installé, puis exécutez la commande suivante dans votre terminal :

```bash
pip install -r requirements.txt
```

*Note : Les jeux de données sont téléchargés et configurés automatiquement au lancement des notebooks dans le dossier `data/`.*

---

## Comment exécuter le projet ?

Chaque partie est complètement autonome et s'exécute directement via son notebook Jupyter :

1. **Partie I (MLP)** : Ouvrez et exécutez [Notebook_01_MLP.ipynb](Notebook_01_MLP.ipynb). 
   - *Génère : les courbes de validation d'initialisation, la matrice de confusion et l'explication SHAP (`figures/shap_summary_plot.png`).*
2. **Partie II (CNN)** : Ouvrez et exécutez [Notebook_02_CNN.ipynb](Notebook_02_CNN.ipynb).
   - *Génère : l'étude d'ablation (`figures/ablation_study.png`) et les cartes d'activation de la première couche de convolution (`figures/feature_maps.png`).*
3. **Partie III (RNN/Seq2Seq)** : Ouvrez et exécutez [Notebook_03_RNN_Seq2Seq.ipynb](Notebook_03_RNN_Seq2Seq.ipynb).
   - *Génère : la courbe de perte récurrente comparative (`figures/comparaison_cellules.png`) et la courbe de perte du Seq2Seq (`figures/seq2seq_loss.png`).*


