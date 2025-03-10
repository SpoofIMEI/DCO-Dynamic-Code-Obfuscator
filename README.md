# DOC (Dynamic Code Obfuscator)
![rem_back-removebg-preview](https://user-images.githubusercontent.com/72181445/183062380-e6321c88-42e4-4f7a-877e-d39d7d019edb.png)

## Description
### DCO Takes in code (python,binary,bash), base64 encodes the payload, reverses the encoded text and generates a unique and obfuscated python program that when executed launches the payload.

## Installation
```
git clone https://github.com/SpoofIMEI/DCO-Dynamic-Code-Obfuscator
cd DCO-Dynamic-Code-Obfuscator
python3 -m pip install -r requirements.txt
python3 DCO.py -h
```


## Usage
```
  -h, --help            show this help message and exit
  -i INPUT_FILE, --input-file INPUT_FILE
                        File you want to obfuscate.
  -f FORMAT, --format FORMAT
                        What format the file is you want to obfuscate. (python, binary, bash)
  -o OUTPUT_FILE, --output-file OUTPUT_FILE
                        File where you want the obfuscated while to be written.
  -p PRE_SCRIPT, --pre-script PRE_SCRIPT
                        Python program to run before executing the main payload.
  --os OS               Operating system the obfuscated code will be ran in. (windows,linux)
```

## Example usage:
```
python3 DCO.py -i reverse_shell.sh -f bash --out reverse_obf.py --os linux
python3 DCO.py -i Document.exe -f binary --os windows --out Document.py
python3 DCO.py -i im_bad_at_naming.py --os windows -f python --out install_ram.py
python3 DCO.py -i Document.exe -f binary --os windows -p disable_av.py --out Document.py
```

## Supported formats:
* ### python (executed in memory)
* ### bash (executed in memory)
* ### binary (written to disk and executed)

#### Donate monero: 48ZrWwcf1gpG9VCe7agYru36SJhKwDDyGCgGw4TvkAG92Exd9pN7GBvL23SkwrMMbgdFa7BnFX2k6cD49SzV7pv42B4JDQE
