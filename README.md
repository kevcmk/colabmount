# Drive Secrets

Quick mount a Google Drive file in a notebook if it's running in Colab, otherwise do nothing.

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
!pip install colabmount

from colabmount import mount_file

load_dotenv(mount_file(".env", create=True) or ".env")

secret = os.environ['SECRET']
```

## Important

The files created are in plaintext in your Google Drive. Anyone with access to your Google Drive can read them as a text file.
