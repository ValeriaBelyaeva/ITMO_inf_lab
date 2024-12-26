Файл result.txt получается после выполнения команды  
`grep -h "Error" log1 log2 log3 | sort | uniq > result.txt`

Здесь:  
• -h отключает вывод имени файла в результатах  
• sort упорядочивает строки  
• uniq удаляет дубликаты  
• результат записывается в result.txt  