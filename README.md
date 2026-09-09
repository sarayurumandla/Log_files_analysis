# Log_files_analysis
import re

def analyze_log(filepath, pattern):
    """Parse a log file and count how often each unique pattern occurs."""
    counts = {}

    with open(filepath, "r") as f:
        for line in f:
            match = re.search(pattern, line)
            if match:
                key = match.group()
                if key in counts:
                    counts[key] += 1
                else:
                    counts[key] = 1

    return counts

# Example: count occurrences of error codes like "ERR404", "ERR500"
results = analyze_log("network.log", r"ERR\d{3}")

# Sort by count, highest first
for pattern, count in sorted(results.items(), key=lambda x: x[1], reverse=True):
    print(f"{pattern}: {count} occurrences")
