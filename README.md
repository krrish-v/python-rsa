# Pure Python RSA implementation

[![PyPI](https://img.shields.io/pypi/v/rsa.svg)](https://pypi.org/project/rsa/)
[![Build Status](https://travis-ci.org/sybrenstuvel/python-rsa.svg?branch=master)](https://travis-ci.org/sybrenstuvel/python-rsa)
[![Coverage Status](https://coveralls.io/repos/github/sybrenstuvel/python-rsa/badge.svg?branch=master)](https://coveralls.io/github/sybrenstuvel/python-rsa?branch=master)
[![Code Climate](https://api.codeclimate.com/v1/badges/a99a88d28ad37a79dbf6/maintainability)](https://codeclimate.com/github/codeclimate/codeclimate/maintainability)

It is forked from the pure-Python RSA library library, the changes in this library to is gonna make you to supply keys in the tuple form to functions.

[Python-RSA](https://stuvel.eu/rsa) is a pure-Python RSA implementation. It supports
encryption and decryption, signing and verifying signatures, and key
generation according to PKCS#1 version 1.5. It can be used as a Python
library as well as on the commandline. The code was mostly written by
Sybren A.  Stüvel.

Download and install using:

    git clone https://github.com/krrish-v/python-rsa

You will provide the keys something like-
       
        import rsa
        
        public, private = rsa.newkeys(2048)
        public_key = (public.n, public.e)
        private_key = (private.n, private.e, private.d, private.p, private.q)
        
        # encryption
        rsa.encrypt(b'message', public_key)
        #decryption
        rsa.decrypt(<encrypted_text>, private_key)
        
And now why it is?

-It is gonna make to collect the all the variables (n, e, d, p, q) if seperately also, so you can arrange them in a tuple and get it upload inside the function, it make easy to store the keys inside a file in int() format and the use it afterwards.
