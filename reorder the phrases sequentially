# Load the file and reorder the phrases sequentially 1. 2. 3...
file_path = '/home/failas.txt' #your file destination/path

with open(file_path, 'r', encoding='utf-8') as file:
    content = file.readlines()

# Skip the first sentence
content = content[1:]

# Process each line, change numbering sequentially
output = []
number = 1

for line in content:
    if line.strip():  # Only process non-empty lines
        # Find where the number and period is, and replace it with the new number
        new_line = line.split(". ", 1)
        if len(new_line) > 1:  # To ensure it's a valid numbered phrase
            output.append(f"{number}. {new_line[1]}")
            number += 1
        else:
            output.append(line)

# Save the output to a new file
output_path = '/home/failas_reordered.txt' # generated and finished file
with open(output_path, 'w', encoding='utf-8') as file:
    file.writelines(output)

output_path
