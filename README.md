# SquadPy Library

------------

![Python Versions](https://img.shields.io/badge/python-3.9|3.10|3.11|3.12-blue)

SquadPy eases interacting with the Squad (HabariPay) payment gateway in Python. 
It offers wrappers for various functionalities, streamlining payment processing 
for your projects.

Squad (owned by **HabariPay | GTBank**) is a Nigerian payment gateway that allows 
businesses to accept payments easily and securely.


> 📝: Read more on Monnify api documentation: [Monnify API DOCUMENTATION](https://developers.monnify.com/api/)

> 📝: Read more on monnifyease api documentation: [MonnifyEase DOCUMENTATION](https://monnifyease.readthedocs.io/en/latest/)


## Getting Started

You should create a Squad sandbox account to generate: 

1. **Squad Test Secret Key**
2. **Squad Test Api Key**

You can see this in the *Merchant Settings page >> API keys and Webhooks section*.

> ⚠️: **Warning:** Do not expose your secret key, api key or 
>commit your any to git, or use them in client-side code.

> 💡: **Take Note:**  The Squad SDK is to be used from your front-end when integrating using Monnify.

> ✅: **Good**: Set your secret key, api key, in environment variables as seen: 
> 1. *SQUAD_SECRET_KEY=your-secret-key*
> 2. *SQUAD_API_KEY=your-api-key*


## Create a Virtual Environment

1. For Windows:

    * Create virtual environment

        ```
            py -m venv <environment_name>
       ```
    * Activate the virtual environment

        ```
            <environment_name>\Scripts\activate
       ```

2. For Unix/macOS

    * Create virtual environment

        ```
            python3 -m venv <environment_name>
       ```
    * Activate the virtual environment

        ```
            <environment_name>/bin/activate
       ```

----------------------------------------------------------------------

## Install squadpy library:


* #### Install squadpy using pip.

> pip install squadpy

* #### Install squadpy using pipx.

> pipx install squadpy

* #### Install squadpy using poetry.

> poetry add squadpy


## If you want to download the sdist packages directly:

Download the wheel distribution file and install using pip

>  pip install squadpy-0.i.0-py3-none-any.whl 

Download the source distribution file, and install using pip

> pip install squad-0.i.0.tar.gz 


## To get a development version of squadpy

Clone from the ``dev`` branch GitHub repository, unzip and install:

> git clone -b dev https://github.com/cla-bit/MonnifyEase.git

> cd squad

> pip install squad

----------------------------------------------------------------------

## API usage

-------------------------------------------------------

### Making a Transaction [Synchronous]

If after setting your secret key in environment variables, for a synchronous transaction process 
all you need to do is use the transaction API to make a transaction. 

To create a transaction or initialize a transaction:

* import the Monnify API wrapper.

```python

from monnifyease import Monnify, Currency, MERCHANT_CODE

client = Monnify()

create_transaction = client.transactions.initialize_transaction(
    amount=1000.00,
    customer_name="Test Customer",
    customer_email="test@gmal.com",
    payment_reference="test123prod",
    payment_description="Testing payment",
    currency=Currency.NGN.value,
    merchant_contract_code=MERCHANT_CODE,
   # add other parameters here
)

print(f"Transaction Created: {create_transaction}")

```

> ✅: **Good**: You can check your Monnify account, go to the Transaction page, and you will see the transaction just created.


# Other Tools
Similar to calling the Monnify, you can also call other tools to make your work easy. For example:

* ### Currency Type
```python

from monnifyease import Currency

val1 = Currency.NGN.value
print(val1)

```
> "NGN"

See documentation for more: https://monnifyease.readthedocs.io/en/latest/
