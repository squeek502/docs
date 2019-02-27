# Go-fuzz targets

To fuzz Go code, use the `setup` steps to install all the needed dependencies. Then, specify the package and method to fuzz in the `harness` field.

This is an example of the configuration of a target written in Go, with a fuzz method named `FuzzMe` in package `github.com/x/y/z/a/b/c`:

```yaml
# ---- base, global setup, and global environment omitted
language: go
version: "1.11"
# checkout specifies where in the Gopath to place your code
# this repository will be placed in the directory:
# ~/go/src/github.com/x/y
checkout: github.com/x/
targets:
    - name: my-target
      setup:
        - dep ensure # make sure all dependencies are installed
      corpus: ./my_target/corpus
      harness:
        # the name of your method
        function: FuzzMe
        # build tags are optional
        build_tags: tag1 tag2 tag3
        # package specifies the package to import the
        # desired function from 
        package: github.com/x/y/z/a/b/c
```

You're ready to go! [Push your project to Fuzzbuzz](../fuzzing-jobs.md) and it will detect your targets automatically.

