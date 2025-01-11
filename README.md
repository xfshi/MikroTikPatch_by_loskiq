# Notice

I have already generated the keys for you. You can use them to generate a license key and sign packages:

```
export MIKRO_NPK_SIGN_PUBLIC_KEY="C293CED638A2A33C681FC8DE98EE26C54EADC5390C2DFCE197D35C83C416CF59"
export MIKRO_LICENSE_PUBLIC_KEY="8E1067E4305FCDC0CFBF95C10F96E5DFE8C49AEF486BD1A4E2E96C27F01E3E32"
export CUSTOM_NPK_SIGN_PRIVATE_KEY="7D008D9B80B036FB0205601FEE79D550927EBCA937B7008CC877281F2F8AC640"
export CUSTOM_NPK_SIGN_PUBLIC_KEY="28F886E32C141123126CFBCAD56766E99D1720CEB1F12BE2468BEBE7662FBEDB"
export CUSTOM_LICENSE_PRIVATE_KEY="9DBC845E9018537810FDAE62824322EEE1B12BAD81FCA28EC295FB397C61CE0B"
export CUSTOM_LICENSE_PUBLIC_KEY="723A34A6E3300F23E4BAA06156B9327514AEC170732655F16E04C17928DD770F"
```

You can generate your own keys yourself, but in this case you will have to manually create a MikroTik image.  
It is easier to use previously generated keys. Here is the command to generate your own keys:

```
python3 license.py genkey
```

# How to generate license key

- Install Python 3.x
- Clone this repository

## RouterOS

### Let's assume that your software_id is: 4JZ2-H049

```
loskiq@debian12:~# python3 license.py licgenros 4JZ2-H049 9DBC845E9018537810FDAE62824322EEE1B12BAD81FCA28EC295FB397C61CE0B
-----BEGIN MIKROTIK SOFTWARE KEY------------
50eNy667HxTQwmCtCpT15YaVx6lpPHQoy2w/KIsjoOHs
Eq/cU24G3/aIjHVeXXqjPRTubErxzaqjHD3aWIi1KA==
-----END MIKROTIK SOFTWARE KEY--------------
loskiq@debian12:~#
```

## Cloud Hosted Router

### Let's assume that your system_id is: pjLQ21gHzfI

```
loskiq@debian12:~# python3 license.py licgenchr pjLQ21gHzfI 9DBC845E9018537810FDAE62824322EEE1B12BAD81FCA28EC295FB397C61CE0B
-----BEGIN MIKROTIK SOFTWARE KEY------------
hdMf+/8rDWLOCOuNt8qP82NgHbN8YdQfJcZNRyWzBerz
BfwOQF1ehUjNubOGkCf4zkPQrK7U+2hbM/uh7gJWGA==
-----END MIKROTIK SOFTWARE KEY--------------
loskiq@debian12:~#
```
