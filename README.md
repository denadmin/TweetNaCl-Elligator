# TweetNaCl-Elligator
Elligator 2 based on tweetnacl

#### ! Warning !
#### This is toy software. It has not received formal security review and should not be entrusted with sensitive data. Use at your own risk.


### description

Implementation of Elligator 2 algorithm based on TweetNaCl library.
Heavily based on libelligator.

Example usage:

        int valid = 0;
        u8 repr[32] = {0};
        u8 pub[32] = {0};
        u8 priv[32] = {0};
        u8 pub_decode[32] = {0};
        //encode
        while (!valid){
                randombytes(priv,sizeof(priv));
                valid = crypto_box_keypair_elligator(pub, repr, priv);
        }
        //decode
        decode_repr(pub_decode,repr);

## links:
* https://elligator.cr.yp.to/
* https://github.com/Yawning/libelligator
* http://tweetnacl.cr.yp.to/
