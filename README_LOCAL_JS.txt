ИНСТРУКЦИЯ: локальная библиотека Extensions API (без tableau.github.io)

Файлы в наборе:
- index.html — расширение (календарь)
- tableau.extensions.1.latest.js — ЗАГЛУШКА! Замените её на реальную библиотеку.
- manifest.trex — манифест, указывает на https://voronka-test1.netlify.app/index.html

Шаги:
1) Скачайте официальный файл библиотеки:
   - GitHub: https://github.com/tableau/extensions-api (папка lib/)
   - Или с https://tableau.github.io/extensions-api/lib/tableau.extensions.1.latest.js
2) Переименуйте скачанный файл в tableau.extensions.1.latest.js
3) Замените им файл-ЗАГЛУШКУ рядом с index.html на Netlify (тот же каталог).
4) В Tableau Server:
   - Добавьте в Allow list: https://voronka-test1.netlify.app
   - (tableau.github.io уже не нужен, т.к. библиотека грузится локально)
5) В книге проверьте точные имена параметров (тип Date):
   «Начало периода», «Конец периода».
6) Добавьте расширение на дашборд, выбрав manifest.trex.

Проверка:
- При открытии диапазон подсветится по значениям параметров.
- Клики обновляют параметры (видно в панели Parameters/фильтре).
