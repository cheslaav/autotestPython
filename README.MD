# pythonAutoTest
automation test with python and selenium

## Первичная настройка окружения

### Для Мак

Для установки Python3 в macOS воспользуйтесь [инструкцией](https://wsvincent.com/install-python/#install-python-on-macos.) 

После установки откройте окно терминала и создайте папку, где будут храниться наши виртуальные окружения, затем перейдите в созданную папку:

```
mkdir environments
```

```
cd environments
```

Создадим виртуальное окружение с помощью команды python3:

```
python3 -m venv selenium_env
```

Активируем окружение:

```
source selenium_env/bin/activate
```

Если понадобится выйти из нашего окружения, достаточно ввести команду deactivate:

```
deactivate
```

Обратите внимание, что после перезапуска терминала нужно будет снова активировать нужное окружение.

### Установка драйвера для браузера: macOS

```
brew install wget
```

Для установки драйвера откройте сайт https://googlechromelabs.github.io/chrome-for-testing/#stable и скопируйте ссылку на ту версию ChromeDriver, которая соответствует версии вашего браузера.


```
cd ~/Downloads
```

```
wget https://edgedl.me.gvt1.com/edgedl/chrome/chrome-for-testing/117.0.5938.92/win64/chromedriver-win64.zip
```


Разархивируйте скачанный файл и переместите его в папку /usr/local/bin, чтобы он был глобально доступен в вашей системе.

```
unzip chromedriver_mac64.zip
```

```
sudo mv chromedriver /usr/local/bin
```

Проверим, что нужная версия chromedriver установлена.

```
chromedriver --version
```


## Для Windows

Для начала вам нужно [скачать](https://www.python.org/downloads/windows/) установочный файл для Python3. Для этого на официальной странице  Python выберите стабильную версию для Windows, и скачайте файл для вашей системы (64-разрядная или 32-разрядная).

Создадим папку, где будут храниться наши виртуальные окружения, и перейдем в неё:

```
mkdir environments
```

```
cd environments
```

Создадим виртуальное окружение:

```
python -m venv selenium_env
```

Запустим созданный для нас приложением venv файл activate.bat, чтобы активировать окружение:

```
selenium_env\Scripts\activate.bat
```

Если понадобится выйти из нашего окружения, достаточно выполнить команду 

```
deactivate
```

### Установка драйвера

1. Скачайте с сайта [драйвер](https://edgedl.me.gvt1.com/edgedl/chrome/chrome-for-testing/117.0.5938.92/win64/chromedriver-win64.zip) для вашей версии браузерa. Разархивируйте скачанный файл.
2. Создайте на диске C: папку chromedriver и положите разархивированный ранее файл chromedriver.exe в папку C:\chromedriver.
3. Добавьте в системную переменную PATH папку C:\chromedriver. Как это сделать в разных версиях Windows, описано [здесь](https://www.computerhope.com/issues/ch000549.htm). 
