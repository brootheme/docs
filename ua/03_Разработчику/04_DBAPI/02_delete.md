### Видалення данних з бази

bool delete(string $from [, string $where [, string $fields]])

**$from** - таблиця, в якій необхідно видалити дані
**$where** - умова, за яким необхідно видалити дані
**$fields** - список полів, які потрібно видалити. Якщо не вказано, то віддаляється весь ряд

***

#### Приклад

	//Видалення користувача з бази за ідентифікатором  
	global $modx, $table_prefix;  
	$id = $modx->db->escape($id);  
	$modx->db->delete($table_prefix.".modx_web_users", "id = $id");