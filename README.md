# Machine-Learning-Final-Project

This project, titled "Divide, Conquer and Classify," focuses on developing a hierarchical classification framework designed to automatically organize the vast amount of scientific literature in repositories like arXiv.


Instead of using a traditional "flat" classification approach—which struggles with the high dimensionality and semantic overlap of over 150 subcategories—this system employs a "Divide and Conquer" architecture powered by Deep Learning.


Key Components of the Project:
Two-Phase Architecture:
Phase 1 (General Model): A global "router" (a Multi-Layer Perceptron) that assigns documents to one of seven macro-areas, such as Physics, Computer Science, or Mathematics.


Phase 2 (Specialist Models): A modular set of independent neural networks. Each "specialist" is trained specifically for one macro-area to determine the final fine-grained subcategory.


SPECTER Embeddings: Unlike traditional word-frequency methods (like TF-IDF), the system uses SPECTER, a Transformer-based architecture trained on citation graphs
. This allows the model to group documents based on deep semantic relationships even if they don't share the same vocabulary.


Data Engineering: The project involved rigorous preprocessing, including taxonomy normalization to map obsolete tags and class fusion (merging Economics and Finance) to reduce ambiguity and improve model robustness.


Results and Conclusions:
The system proved highly effective, achieving a Top-3 accuracy of 78.2%
. This gap between strict accuracy (60.9%) and Top-3 accuracy suggests that most errors occur between semantically related sub-disciplines, confirming that the model successfully captures the underlying scientific context
. Ultimately, the hierarchical approach reduces computational complexity and effectively "unravels" the complex web of modern science.
