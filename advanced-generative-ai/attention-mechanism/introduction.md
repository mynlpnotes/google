# Introduction

* Core of the LLM
* To translate an English sentence to French
*

    <figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
* We could use an encoder decoder model for this
* But sometimes the translated sentence might not perfectly align with the translated sentence at each time stamp
*

    <figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>
* When we translate this, the 1st word in English is The, but in French the 1st word will be chat
* How can we train the model so that it focuses more on cat rather than black
* To improve translation, we can add Attention mechanism to Encoder Decoder
* Attention mechanism is a technique that allows a NN to focus on specific parts of an input sequence
* This is done by assigning weights to different parts of the input sequence with the most important parts receiving the highest weights
* The weighted sum of the input sequence is then used as the input to the next layer of NN
*
