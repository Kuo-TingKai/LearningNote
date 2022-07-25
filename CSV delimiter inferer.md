# CSV delimiter inferer

>kevinkuo 2022/07/23

如果是單純的csv檔不管其他資料庫格式

```python=
#!/usr/bin/env python
import csv

def parse(filename):
    with open(filename, 'rb') as csvfile:
        dialect = csv.Sniffer().sniff(csvfile.read(), delimiters=';,\t\n ')
        csvfile.seek(0)
        reader = csv.reader(csvfile, dialect)

        for line in reader:
            print(line)

def main(): 
    parse('example.csv')

if __name__ == '__main__':
    main()
```

[solution stack](https://en.wikipedia.org/wiki/Solution_stack)
[stackmap](https://www.stackmap.io/demo-booking)
[crossmap(oracle)](https://docs.oracle.com/middleware/1213/osb/develop/GUID-F1DED2BC-B513-4637-9FAF-63F07FAB52A5.htm#OSBDV88848)

