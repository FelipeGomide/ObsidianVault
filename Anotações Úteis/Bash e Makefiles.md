## Tips for writing shell scripts within makefiles:

1. Escape the script's use of `$` by replacing with `$$`
2. Convert the script to work as a single line by inserting `;` between commands
3. If you want to write the script on multiple lines, escape end-of-line with `\`
4. Optionally start with `set -e` to match make's provision to abort on sub-command failure. You can also use `set -e -o pipefail` to make sure errors in pipe commands cause the script to abort (note: this is a bashism, so requires `SHELL := /bin/bash` or similar)
5. This is totally optional, but you could bracket the script with `()` or `{}` to emphasize the cohesiveness of a multiple line sequence -- that this is not a typical makefile command sequence

Here's an example inspired by the OP:

```bash
mytarget:
    { \
    set -e ;\
    msg="header:" ;\
    for i in $$(seq 1 3) ; do msg="$$msg pre_$${i}_post" ; done ;\
    msg="$$msg :footer" ;\
    echo msg=$$msg ;\
    }
```


## Comandos Úteis

### Loop:
```bash
for file in folder/* : do \
	(comandos do loop);\
done
```

### Remover caminho do nome do arquivo
`$$(basename "$$string") ` 
`$${var%.ext}`
