# Bash Scripting

Iterate through files and print each line:

```bash
#!/bin/bash

file=$1

if [ -f "$file" ]; then
	echo "Reading from $file"
else
	echo "Cannot find $file"
	exit 1
fi

while IFS="" read -r line || [ -n "$line"  ]
do
	printf 'Scanning %s\n' "$line"
done < ${file}

echo "Done."
```

