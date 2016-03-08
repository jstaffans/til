# AOT-compiling a shell namespace

To get a proper main() method, AOT compiling is needed. But you really don't want to AOT-compile
anything unnecessarily.

One way to handle this is to just AOT-compile a small shell namespace:

```clojure
(ns my.shell (:gen-class))

(defn -main [& args]
   (require 'my.real.ns)
   (apply (resolve 'my.real.ns/-main) args))
```

* one (harmless) namespace is AOT-compiled
* jsvc knows how to launch it


