![Image Description](https://i.imgur.com/JvSydqn.jpg)
### Multi-Label Convolutional Neural Network (CNN)

**Author:** Tyler Gustafson
*Summer 2024*

#### ``Objectives``

**Overview:** This project utilizes a Multi-Label Convolutional Neural Network (CNN) to identify and classify Pokémon based on images. The model is trained on a diverse dataset of Pokémon images, allowing it to predict multiple labels such as type and evolutionary stage. The goal is to achieve high accuracy in multi-label classification, showcasing the potential of CNNs in image recognition tasks.

#### ``Motivations``
**Why is it important?**
- **Technical Insight & Improvement**
    - *Evaluating Accuracy:* Assess the performance of machine learning models in identifying specific characters.
    - *Educational Value:* Practice principles of machine learning and deep learning, particularly CNNs
- **Practical Applications and Broader Impact**
    - *Environmental Monitoring:* Use image recognition to track and identify animals for habitat preservation.
    - *Autonomous Vehicles:* Improve self-driving cars' ability to recognize and respond to road objects for enhanced safety and efficiency.

- **Or for the everyday trainer: Pokédex Upgrade**
    - *Gotta Catch 'Em All… Correctly:* Finally make Professor Oak proud with a supercharged Pokedex that never gets a single entry wrong.
 
#### ``Classes (Targets)``
We understand there are several ways to identify pokemon beyond their actual name and in this analysis we have implemented multiple approaches to account for this along with using these to understand how different classes can enhance a models performance. Below are a list of classes that we have modeled that you will see referenced in the later stages of the notebook
- **Model 1**
    - *Class Targets:* All 151 pokemon
    - *Example:* Bulbasaur, Charmeleon, Dragonite
    - *Dataset:* Full dataset
- **Model 2**
    - *Class Targets:* By Poketype
    - *Example:* Grass, Fire, Dragon
    - *Dataset:* Full dataset
- **Model 3**
    - *Class Targets:* By Evolution Type
    - *Example:* Bulbasaur_Family, Charmander_Family, Dratini_Family
    - *Dataset:* Full dataset
- **Model 4**
    - *Class Targets:* By Legendary Status
    - *Example:* Non_Legendary, Non_Legendary, Legendary
    - *Dataset:* Full dataset

We started with a small data set from:
- Kaggle. (KVPRATAMA). Pokémon Images Dataset. Retrieved from
https://www.kaggle.com/datasets/kvpratama/pokemon-images-dataset

Then we grew the dataset to get more training data to be required this included:
- Kaggle. (LANCE ZHANG). Pokémon Classification. Retrieved from
https://www.kaggle.com/datasets/lantian773030/pokemonclassification
- Kaggle. (MIKOŁAJ KOLMAN). Pokemon Images, First Generation. Retrieved from
https://www.kaggle.com/datasets/mikoajkolman/pokemon-images-first-generation17000-files

- Google API Scraping
- Pokemon Website Database: Veekun. (n.d.). Pokémon Image Dataset. Retrieved from https://veekun.com/dex/downloads

From there we have reviewed and processed the images to ensure they are optimal for model training and evaluation. For example:
- Removed files that are from a unsupported format
- Removed images with poor image quality
- Removed images with numerous Pokemon
- Structured and organized images into to proper class subdirectories based on scenario and optimized for tensorflow and keras packages
 
  Link to final data: https://drive.google.com/drive/u/1/folders/1YE-8-DWiKzseB433Xep20aRRfi3eGdeN

#### ``Example Classes Data``
![Image Description](https://github.com/Tyler-Gustafson/Multi_label_convolutional_neural_network_CNN/blob/main/01_background_info/data_sample_images_pokemon.jpg?raw=true)


#### ``Overview of Results``
![Image Description](https://github.com/Tyler-Gustafson/Multi_label_convolutional_neural_network_CNN/blob/main/01_background_info/preliminary_generalization_performance.jpg?raw=true)

  #### ``Notebook Structure``
1. Imports
2. Initial Exploratory Data Analysis (EDA)
3. Data Ingestion and Initial Preprocessing
4. Data Augmentation & Return to EDA
5. Baseline "Naive" Model
6. Building & Compiling Model
7. Training
8. Hyperparameter Tuning (TBD)
9. Evaluation / Confusion Matrix
10. Understanding Model Performance Under Various Scenarios
    - **Model 1: Class Target** - Individual Pokemon
    - **Model 2: Class Target** - By Pokemon Type
    - **Model 3: Class Target** - By Evolution Group
    - **Model 4: Class Target** - By Legendary Pokemon
11. Generalization
