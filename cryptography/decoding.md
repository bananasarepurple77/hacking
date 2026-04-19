## Decoding HEX and base64 files

1. file {filename}
2. change filetype using mv or cp. Then extract file if zip
3. read file and sort if there is any partern
sort -t, -k1,1n enc
-t, — field separator set to a comma. This tells sort to treat commas as column delimiters instead of whitespace.
-k1,1n — sort key specification:
-k1,1 means sort using field 1 only (the first column).
n appended makes the sort numeric rather than lexicographic.

4. Can ask AI to create a one line command to decode the file.
Example:
mkdir -p decoded_lines
awk -F, '{gsub(/[^0-9A-Fa-f]/,"",$3); print $3}' hex_sorted | xxd -r -p > b64_lines.txt
n=1; while IFS= read -r line || [ -n "$line" ]; do printf '%s' "$line" | base64 -d > decoded_lines/line_$n.bin 2>/dev/null || echo "line $n: decode failed"; n=$((n+1)); done < b64_lines.txt
for f in decoded_lines/line_*.bin; do echo "---- $f ----"; file "$f"; hexdump -C "$f" | sed -n '1,2p'; done

5. cp line_1.bin file to keep original
6. then check file type. Rename as suits.
7. Unzip/read file.

Note: these steps vary depending on the encoding used

## Simple base64 decoding
echo 'asdkfuhasfdhuasdfh==' | base64 -d
