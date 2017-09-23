glog
====

Forked from https://github.com/golang/glog

Installation
------------

```
    go get github.com/sudersen/glog
```    


Feature flags
-------------

```
    -logflushinterval
        Log content would be flushed to the file every mentioned
        duration. Caveat: First flushing would honor the default
        flushing duration
```


Usage
-----

```
    ./gobinary -log_dir=path/to/log_dir -logflushinterval=flushDuration
    For eg: ./gobinary -log_dir=logs -logflushinterval=1s
```


Samples
-------

```
	Package glog implements logging analogous to the Google-internal
	C++ INFO/ERROR/V setup.  It provides functions Info, Warning,
	Error, Fatal, plus formatting variants such as Infof. It
	also provides V-style logging controlled by the -v and
	-vmodule=file=2 flags.
	
	Basic examples:
	
		glog.Info("Prepare to repel boarders")
	
		glog.Fatalf("Initialization failed: %s", err)
	
	See the documentation for the V function for an explanation
	of these examples:
	
		if glog.V(2) {
			glog.Info("Starting transaction...")
		}
	
		glog.V(2).Infoln("Processed", nItems, "elements")
```