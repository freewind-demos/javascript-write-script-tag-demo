JavaScript Write Script Tag Demo
================================

直接:

```
<script>
document.write('<script src=...></script>')
</script>
```

是不行的。因为字符串里的`</script>`会被错认为普通的`</script>`导致提前关闭，所以要对它进行转义。

两种做法：

```
document.write('\x3Cscript type="text/javascript" src="foo.js">\x3C/script>');
```

```
document.write('<script type="text/javascript" src="foo.js"></script>');
```

前者清晰，后者更通用。

```
open index.html
```

Resources
--------

- https://stackoverflow.com/questions/236073/why-split-the-script-tag-when-writing-it-with-document-write
