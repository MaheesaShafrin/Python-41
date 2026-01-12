# Python-41
Write a python program to find the most frequent words from a file
name = input('Enter file: ')
handle = open(name, 'r')

text = handle.read()
words = text.split()

counts = {}
for word in words:
    counts[word] = counts.get(word, 0) + 1

bigword = None
bigcount = None

for word, count in counts.items():
    if bigcount is None or count > bigcount:
        bigword = word
        bigcount = count

print(bigword, bigcount)


Output:
Enter file: data.txt
