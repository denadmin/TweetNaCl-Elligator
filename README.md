# TweetNaCl-Elligator
Elligator 2 based on tweetnacl

#### ! Warning !
#### This is toy software. It has not received formal security review and should not be entrusted with sensitive data. Use at your own risk.


### description

Implementation of Elligator 2 algorithm based on TweetNaCl library.
Heavily based on libelligator.

Example usage:

        int vaild = 0;
        u8 repr[32] = {0};
        u8 pub[32] = {0};
        u8 priv[32] = {0};
        u8 pub_decode[32] = {0};
        // encode
        while (!vaild){
          randombytes(priv,sizeof(priv));
          valid = elligator(pub, repr, priv);
        }
        // decode
        decode_repr(pub_decode,repr);
        // now pub_decode eq pub

## links:
* https://elligator.cr.yp.to/
* https://github.com/Yawning/libelligator
* http://tweetnacl.cr.yp.to/
