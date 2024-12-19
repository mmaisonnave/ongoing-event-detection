# Detecting ongoing events using contextual word and sentence embeddings

![Contributors](https://img.shields.io/github/contributors/mmaisonnave/ongoing-event-detection?style=plastic)
![Forks](https://img.shields.io/github/forks/mmaisonnave/ongoing-event-detection)
![Stars](https://img.shields.io/github/stars/mmaisonnave/ongoing-event-detection)
![GitHub](https://img.shields.io/github/license/mmaisonnave/ongoing-event-detection?style=round-square)
![Issues](https://img.shields.io/github/issues/mmaisonnave/ongoing-event-detection)

This repository holds the source code for all the experiments conducted for the publication *"[Detecting ongoing events using contextual word and sentence embeddings](https://www.sciencedirect.com/science/article/abs/pii/S0957417422013975),"* featured in the journal *Expert Systems with Applications* in December 2022. The authors of the paper are Mariano Maisonnave, Fernando Delbianco, Fernando Tohmé, Ana Maguitman, and Evangelos Milios.

## Paper Abstract
This paper introduces the Ongoing Event Detection (OED) task, which is a specific Event Detection task where the goal is to detect ongoing event mentions only, as opposed to historical, future, hypothetical, or other forms or events that are neither fresh nor current. Any application that needs to extract structured information about ongoing events from unstructured texts can take advantage of an OED system. The main contribution of this paper are the following: (1) it introduces the OED task along with a dataset manually labeled for the task; (2) it presents the design and implementation of an RNN model for the task that uses BERT embeddings to define contextual word and contextual sentence embeddings as attributes, which to the best of our knowledge were never used before for detecting ongoing events in news; (3) it presents an extensive empirical evaluation that includes (i) the exploration of different architectures and hyperparameters, (ii) an ablation test to study the impact of each attribute, and (iii) a comparison with a replication of a state-of-the-art model. The results offer several insights into the importance of contextual embeddings and indicate that the proposed approach is effective in the OED task, outperforming the baseline models.

## Dataset
The dataset used in this work is based on the New York Times (NYT) archive from 1987 to 2007, as described by Sandhaus (2008).
 *Sandhaus, Evan. The New York Times Annotated Corpus LDC2008T19. Web Download. Philadelphia: Linguistic Data Consortium, 2008.

The dataset was built by tokenizing the full archive using the Spacy NLP library and extracting sentences. A subset of sentences was selected by searching for mentions of three financial crises: the Mexican peso crisis of 1994, the Russian financial crisis of 1998, and the Asian financial crisis of 1997. This selection was done using the Lucene search engine with keywords related to these crises, yielding 2,000 sentences for labeling, with an additional 200 sentences for testing. 

The dataset focuses on labeling sentences as either event triggers (representing ongoing events) or non-event triggers, in a binary classification task. This labeling was done through an active learning process. More details on the dataset can be found on its dedicated website: [https://cs.uns.edu.ar/~mmaisonnave/resources/ED_data/](https://cs.uns.edu.ar/~mmaisonnave/resources/ED_data/).

## License
The source code in this repository is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Contributing
We welcome contributions from the community. Please open an issue or submit a pull request for any improvements or suggestions.

## Acknowledgments
This work was enabled  by support provided by  CONICET, Universidad Nacional del Sur (PGI-UNS 24/N051 and PGI-UNS 24/E145), ANPCyT (PICT 2019-01640, PICT  2019-02302, and PICT 2019-03944), a LARA project (Google Research Award for Latin America 2019-2021), Compute Canada ([https://www.computecanada.ca](https://www.computecanada.ca)), a New Frontiers in Research Fund Exploration Grant, an ELAP scholarship by the Department of Foreign Affairs, Trade and Development Canada and ACENET ([https://www.ace-net.ca/](https://www.computecanada.ca)).
