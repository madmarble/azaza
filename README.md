Выполнено : <br>
добавление ключа в узел<br>
cплит<br>
Статус : отладка<br>
old_version_btree - б-дерево, в котором каждый узел представляется отдельным файлом, название файлов уникальные, реализованы те же функции
b_tree - актуальная версия<br>
Входные данные :<br>
Один файл, в котором начало отведено под конфигурацию б-дерева(chunk_size, db_size, t), далее идет массив занятости блоков, далее идут блоки памяти.<br>
Состав блока - количество детей - n, флаг листа, номера детей - блоков количества n + 1, размер ключа и ключ количества n, размер данных и данные количества n.<br>

block.h - функции работы с блоками памяти - read, write, create<br>
conf.h - функции работы с конфигурационным файлом - создание конфигурационного файла по умолчанию или создание из файла<br>
btree.h - описание структур б-дерева<br>
btree.c - insert, insert-non-full, split, freedom(для освобождения памяти DB)<br>
TODO:<br>
реализовать битовый массив занятости блоков вместо байтового<br>
функции delete, find<br>
освобождение памяти конфигурационного файла DBC<br>
чтобы все это заработало<br>
