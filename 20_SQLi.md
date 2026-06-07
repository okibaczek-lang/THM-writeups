# THM ROOM - SQLi

## SQL keywords
- -- everything after this is ignored
- UNION combines two SELECT results
- LIKE pattern matching
- % different sequences of letters and numbers
- LIMIT row limit returned
- SELECT retrieve data from tables

## Key payloads
- ' OR 1=1;--	                                                        Authentication bypass payload
- ' UNION SELECT 1,2	                                                UNION payload
- ' UNION SELECT 1,2,3 where database() like '%';--                   Boolean payload
- ' UNION SELECT SLEEP(5);--	                                        Time-delay payload

## Error-Based SQLi
- Uses database error messages
- Errors reveal information about database

## Union-Based SQLi
- Uses UNION SELECT
- Retrieves additional data from database

## Boolean-Based Blind SQLi
- No errors returned
- Observe differences between TRUE and FALSE conditions

## Time-Based Blind SQLi
- No errors and no visible differences
- Uses delays such as SLEEP() to extract information

## Key lesson
I learned how and when to use these types of SQLi
