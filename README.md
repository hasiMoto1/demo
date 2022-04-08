[default]
host -WinServer2012
[ignore_comments]
REGEX = ^# .*
DEST_KEY =queue
FORMAT =nullQueue
[iis2]
DELIMS =” ”
FIELDS = date time s-ip cs-method cs-uri-stem cs-uri-query s-port cs-username c-ip cs(User-Agent) cs(Cookie) cs(Referer) cs-host sc-status sc-substatus sc-win32-status sc-bytes cs-bytes time-taken 
