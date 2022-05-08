# Fonts

# Generate unicode list

https://onlineunicodetools.com/generate-unicode-range
https://unix.stackexchange.com/questions/423345/generate-collating-order-of-a-list-of-individual-characters

xfd -fa "DejaVu Sans Mono"

fc-query font-file

fc-match --format='%{charset}\n' OpenSans

echo "\ue00e" | demenu -fn "-wuncon-siji-medium-r-normal--10-100-75-75-c-80-iso10646-1"

#!/bin/bash

x=(0 1 2 3 4 5 6 7 8 9 A B C D E F)
for a in {0..15}; do for b in {0..15}; do for c in {0..15}; do
[[$a -eq 0 && $b -eq 0 && $c -lt 2]] && continue
echo -en "\n${x[$a]}${x[$b]}${x[$c]}X: "
for d in {0..15}; do
echo -en "\u${x[$a]}${x[$b]}${x[$c]}${x[$d]}"
done
done; done; done
