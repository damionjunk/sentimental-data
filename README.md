# sentimental-data

Data to use with various sentiment analysis tools. SNAPSHOT versions
are not considered stable.

The reason we're storing a CSV file this way is to provide an extreme
audit trail for modifications and versions of the various data sets
contained within this repository.

## Usage

Usable as a Maven or Leiningen dependency:
```clojure
["sentimental-data" "0.1.0"]
```

Data sets are located in the *resources/* directory and will be
accessible on the classpath of a JVM process. In Clojure, they can be
accessed with something similar to the following code:

```clojure
(ns foo
  (:require [clojure.java.io :as io]))

(with-open [rdr (io/reader (io/resource "filename.csv"))]
  (doseq [line (line-seq rdr)]
    ;; Do somehting with the lines perhaps!
    ))
```

## License

License for each data set belongs to the original data creator. Some
of the data sets in this repository may be derivative works.

