Best Practise:
1. Use API in SLF4j instead of the one in Log4j, Logback.
Separate the 
2. Use stackholder instead of appending the string for trace/debug/info.
3. The exception information should include both details on exception & stacktrace.

Exception:
1. make sure the log existed when exception caught. 
2. The key attributes in logging should include:
	 who did the call
	 what the Context is
	 what action has been performed
	 what attributes can do help on trouble-shooting.
3. Data to exclude:
	Source code
	User Credentials(password, TEA token)
	Connection details

Logging Location:
	Network: access log

	Process:
	Input Validation failures e.g. illegal Query String or URI 
	Excessive use
	Authentication success& failures
	Authorization failures
	Session Management failures
	Backend Micro-Service failures
	Request details(uri, headers)
	Response details(status code, headers)

	System Call:
	Schedule Job start-ups & shut-downs
	Data changes on Routing & ContentProviders.

