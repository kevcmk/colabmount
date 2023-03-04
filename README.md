# Drive Secrets

Quick mount a Google Drive file in a notebook if it's running in Colab, otherwise do nothing.

You might find this useful if you use the .ipynb files across both Colab and local environments.

## Quickstart

Add the following to your Colaboratory notebook.

### Simple Example

```
!pip install colabmount

from colabmount import mount_file

path = mount_file(".env", create=True)
```

### Dotenv Example
```
!pip install colabmount python-dotenv

from colabmount import mount_file
from dotenv import load_dotenv

load_dotenv(mount_file(".env", create=True) or ".env")
```

## Important

The files created are in plaintext in your Google Drive. Anyone with access to your Google Drive can read them as text files.
