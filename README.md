# Selenium
Урок - использование Selenium в PyTest
В данном уроке мы на очень простом примере рассматриваем использование Selenium для управления веб интерфейсом в браузере.

Файл test_selenium_simple.py содержит пример теста, который откроет окно браузера, в этом окне откроет адрес https://google.com, введет некоторую фразу в строку поиска и нажмет на кнопку поиска. После этих действий тест сделает скриншот страницы и завершится.

В этом простом тесте мы используем поиск элементов по ID и NAME, нажимаем на элемент и вводим текст в текстовое поле.

Как запустить
Для запуска этого теста вам потребуется скачать файл Geko-Driver для управления браузером Google Chrome. Скачать файл можно здесь:

https://chromedriver.storage.googleapis.com/index.html?path=2.43/

После того, как вы скачаете этот файл, вам нужно установить все зависимости:

pip install -r requirements.txt
И после всего этого уже можно запускать тесты:

python3 -m pytest -v --driver Chrome --driver-path /tests/chrome test_selenium_simple.p  

Обратите внимание, что в данном случае я положил скачанный на первом шаге дравер для браузера в папку /tests/ - (chrome - это имя бинарного файла). При запуске тестов вам нужно будет указать полный путь до этого драйвера.
