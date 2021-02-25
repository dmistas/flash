#### Класс для удобного вывода flash сообщений и работой с переменными в сессии
<hr>

Для работы класса должна быть запущена сессия session_start() в вызываемом файле

- Session::flash('key_name', 'message') - записать flash сообщение в сессию
- Session::flash('key_name') - вывести flash сообщение
<br><br>
Дополнительные методы:
<br>
- Session::put('key_name', 'message') - добавить строку в сессию с ключом key_name
- Session::get('key_name') - получить строку с ключом key_name из сессии
- Session::exist('key_name') - проверить наличие в сессии строки с ключем key_name
- Session::delete('key_name') - удалить строку с ключом key_name из сессии

Example:
<pre>
if (!$login) {
    Session::flash('danger', "Логин или пароль неверны");
    }
...

if (exist('danger')){
    echo Session::flash('danger');
    }
</pre>