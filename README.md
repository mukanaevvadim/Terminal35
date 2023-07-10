1. Посмотреть где я: pwd
2. Создать папку: mkdir folder
3. Зайти в папку: 
	3.1 cd folder - переход в папку folder
	3.2 cd .. - переход на уровень выше
	3.3 cd !$ - переход в только что созданную папку
4. Создать 3 папки: 
	4.1 mkdir folder1 folder2 folder3 - создание папок в текущей папке
	4.2 mkdir -p folder1/folder2/folder3 - последовательное создание папок 
5. Зайти в любоую папку: cd folder1
6. Создать 5 файлов (3 txt, 2 json): touch name.txt name1.txt name2.txt name3.json name4.json
7. Создать 3 папки: mkdir folder4 folder5 folder6
8. Вывести список содержимого папки: ls -la
9. + Открыть любой txt файл: cat > folder1/name.txt
10. + написать туда что-нибудь, любой текст: "Едиственный способ стать умнее - играть с более умным противником" - основа шахмат 1883г.
11. + сохранить и выйти: ctrl+c
12. Выйти из папки на уровень выше: cd ..
13. Переместить любые 2 файла, которые вы создали, в любую другую папку: 
	13.1 mv folder1/name.txt folder2/name.txt
	13.2 mv folder1/name3.json folder3/name3.json
14. Скопировать любые 2 файла, которые вы создали, в любую другую папку: 
	14.1 cp folder1/name2.txt folder2/name2.txt
	14.2 cp folder1/name4.json folder3/name4.json
15. Найти файл по имени: find -name "name2.txt"
16. Просмотреть содержимое в реальном времени (команда grep) изучите как она работает: tail -f folder2/name.txt | grep "основа"
17. Вывести несколько первых строк из текстового файла: head folder2/name.txt
18. Вывести несколько последних строк из текстового файла: tail folder2/name.txt
19. Просмотреть содержимое длинного файла (команда less) изучите как она работает:
	19.1 less -s folder2/name.txt - режим просмотра
	19.2 q либо ZZ - выход из режима просмотра 
20. вывести дату и время: date

Задание*

1. Отправить http запрос на сервер.
http://162.55.220.72:5006/terminal-hw-request

1.1 Отправка запроса в терминале с помощью команды curl: 

curl http://162.55.220.72:5006/terminal-hw-request

1.2 Результат: 

"Intro": "Hello!! This is your the first response from server",
  "Tasks": {
    "Task_1": "Send the next URL in terminal: http://162.55.220.72:5006/get_method?name=(set_your_String)&age=(set_your_number)",
    "result": [
      "Your_String",
      "Your_number"
1.3 Задание_1. Отправить следующий запрос в терминале:

curl "http://162.55.220.72:5006/get_method?name=vadim&age=28"

1.4 Результат: 
	[
	"vadim",
	"28"
	]

2. Написать скрипт, который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

2.1 Создание файла + пропись скрипта - cat > script.txt 
	
	#!/bin/bash
	cd ДЗ
	mkdir -p folder/folder1/folder2
	cd folder
	touch name.txt name2.txt name1.txt name3.json name4.json
	mkdir folder3 folder4 folder5
	ls -la
	mv name.txt folder3/name.txt
	mv name3.json folder4/name3.json

2.2 Сохранение файла и выход из меню редактирования - ctrl + C

2.3 Назначение файла исполняемым - chmod u+x ./script.txt

2.4 Запуск скрипта - ./script.txt
