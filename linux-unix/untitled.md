---
description: Mostly Bash script snippets.
---

# Bash Shell / Scripting

Add user `ftpuser`, add it to the group `ftpgroup`, no home directory, no shell:

```text
useradd -g ftpgroup -d /dev/null -s /usr/sbin/nologin ftpuser
```

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

```bash
grep -Eoi '<a [^>]+>' source.html |
grep -Eo 'href="[^\"]+"' |
grep -Eo '(http|https)://[^"]+' | 
sort | uniq > tlds_unique.txt
```

Extract all hyperlinks from all `<a href=""></a>` in an HTML \(source.html\) file, filter out the TLDs, and store them in a file:

```bash
grep -Eoi '<a [^>]+>' source.html |
grep -Eo 'href="[^\"]+"' |
grep -Eo '(http|https)://[^/"]+' | sort | uniq > tlds.txt
```

