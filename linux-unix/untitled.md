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

Extract all hyperlinks from all `<a href=""></a>` in an HTML file and store them in a file:

```text
grep -Eoi '<a [^>]+>' source.html |
grep -Eo 'href="[^\"]+"' |
grep -Eo '(http|https)://[^"]+' | 
sort | uniq > links_unique.txt
```



