When multiple columns are returned from a target table, these can be concatenated into a single column. This makes retrieval more straightforward, because it requires identification of only a single varchar field in the original query.

Oracle: SELECT table_name||':'||column_name FROM all_tab_columns

MS-SQL: SELECT table_name+':'+coumn_name FROM information_schema.columns

MySQL: SELECT CONCAT(table_name,':',column_name) FROM information_schema.column