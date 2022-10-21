We tried to build BIRNN encoder and decoder with anttention to get seq2seq2 translations.
# *build encoder - decoder model :BiRNN + Attention
#BiRNN：The encoder will receive a sequence of words, a LongTensor of size (max_len x batch_size), and output an encoding for each word, a FloatTensor of size (max_len x batch_size x hidden_size).

  Given Sentence :X = (x1,x2,..,xt) Set ht=f(xt,ht-1) and c=q(h1,

Each decoder output is conditioned on the previous outputs and some  𝐱 , where  𝐱  consists of the current hidden state and the attention "context",
    p(y_i |m{y_1,...,y_{i-1}, 𝐱) = g(y_{i-1}, s_i, c_i)
    s_i = f(s_{i-1}, y_{i-1}, c_i)
   where ci is context vector,where each weight a_{ij}is a normalized  attention "energy"

Training:
we use max_size = 25 and max_size= 40 to train the data

### Reference
https://zhuanlan.zhihu.com/p/57155059

