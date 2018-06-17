# Syslog 
Provides access to a Unix system's system logger.

```Io
logger = Syslog clone do(
	identity("SyslogTest")
	facility(facilityMap at("LOG_USER"))
	options(List append(optionsMap at("LOG_PID"), optionsMap at("LOG_CONS")))
	priority(priorityMap at("LOG_INFO"))
	open(facility, options)
	mask(List append(maskMap at("LOG_PRIMASK")))
	log(priority, "*** Merely a test ***")
	close
)
```

> Note: This is partially tested. Please let me know of any problems you happen to stumble across, or if it could be better. --Jeremy Tregunna
