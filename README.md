# راه‌اندازی امن سیگما-بی

## پیشنیاز ها

برای شرکت در این راه‌اندازی، لازم است نرم‌افزار `snarkjs` را نصب داشته باشید. این نرم‌افزار برای اجرا به NodeJS نیاز خواهد داشت، بنابراین لازم است که پکیج `npm` را توسط پکیج منیجر سیستم خود نصب نمایید.

```
sudo apt install npm
npm i g snarkjs
```

## نحوه مشارکت

1. ابتدا این مخزن را کلون کنید:
    ```bash
    git clone https://github.com/nobitex/sigmab-trusted-setup
    ```

2. یک فولدر `params` داخل فولدر مخزن ایجاد کرده و فایل های `zkey` دریافت شده از هماهنگ‌کننده را داخل آن کپی کنید.
    ```bash
    cd sigmab-trusted-setup
    mkdir params
    cp -r [PATH_TO_ZKEY_FILES]/*.zkey params/
    ```

3. دستور `make contribute > logs.txt` را اجرا کنید.
    این دستور از شما یوزرنیم گیتهاب دریافت خواهد کرد. مطمئن شوید که یوزرنیم درستی را وارد می‌کنید.
    لاگ های این دستور داخل فایل `logs.txt` ذخیره خواهند شد. از آن برای نوشتن گزارش خود استفاده کنید.

4. داخل فولدر خود یک فایل به اسم `report.md` ایجاد کنید و گزارش خود را بنویسید. می‌توانید از قالب `TEMPLATE.md` استفاده کنید.

5. با استفاده از نرم‌افزار `gpg`، گزارش خود را امضا کنید. لازم است که از کلیدعمومی که به گیتهاب شما وصل است استفاده کنید.
    ```bash
    gpg --detach-sign repord.md
    ```

6. یک Pull Request بسازید و تغییرات خود را سابمیت کنید.