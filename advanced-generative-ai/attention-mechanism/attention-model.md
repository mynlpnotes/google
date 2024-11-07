# Attention Model

* Differs from traditional seq2seq models in 2 ways

1. Encoder passes lot more data to decoder&#x20;
   1.

       <figure><img src="../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>
   2. Instead of just passing final hidden state, the encoder passes all the hidden state from each time step
   3. This gives decoder more context,&#x20;
   4. Decoder uses all the hidden state to translate the sentence
2.  Takes extra step before producing output:

    1.

        <figure><img src="../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>
    2. To focus only on the most relevant parts of the input
    3. Looks at the set of encoder hidden states that it has received, each encoder hidden state that it received is associated with a certain word in the input sentence
    4. Gives each hidden state a score
    5. Multiplies each hidden state by its softmax score, this amplifying hidden score with high scores and downsizing hidden scores with low scores

