# Linked List
- Setiap node memiliki setidaknya 1 nilai dan pointer ke node selanjutnya; Double linked list jika mengandung pointer ke node sebelum dan selanjut
- Memiliki pointer HEAD untuk menunjuk ke node pertama; pointer TAIL opsional
- Metode:
	- `Insert(val, n)`, menginsert nilai `val` ke posisi `n`
	- `Print()`, meng-print keseluruhan node
	- `Peek(n)`, melihat nilai pada node ke `n`
	- `Del(n)`, menghapus node ke `n`
- Kode:
```Python
class Node:
	def __init__(self, name, severity, next = None):
	self.name = name
	self.severity = severity
	self.next = next

class LinkedList:
	def __init__(self):
	self.ROOT = None

	def AppendNode(self, name, severity):
	newNode = Node(name, severity)
	if self.ROOT is None:
		self.ROOT = newNode
	else:
		currentNode = self.ROOT
		while currentNode.next is not None:
			currentNode = currentNode.next
			currentNode.next = newNode

	def PrintList(self):
	if self.ROOT is None:
		print("List is empty!")
		return -1
	currentNode = self.ROOT
	while currentNode is not None:
		print(f"[{currentNode.name} is {currentNode.severity}] -> ")
		currentNode = currentNode.next

	def RemoveNode(self, index):
	if self.ROOT is None:
		print("List is empty!")
		return -1
	currentNode = self.ROOT
	i = 0
	if index == 0:
		self.ROOT = currentNode.next
		return 0
# Stop 1 node before, then set next 2 nodes ahead, "skipping" the deleted node
	while i < index:
		currentNode = currentNode.next
		i += 1
	currentNode.next = currentNode.next.next
```

# Queue
- Sebuah antrian, biasa diimplementasi dengan list.
- Mengikuti prinsip First in, First out (FIFO)
- Metode:
	- `Shift(); Javascript / Pop(0); Python`, menghapus dan mengembalikan nilai paling pertama / selanjutnya
	- `Print()`, meng-print keseluruhan list
	- `Append(n)`, menambahkan nilai `n` ke queue
- Kode:
```Python
class Queue:
	def __init__(self):
	self.array = []

	def isEmpty(self):
	return len(self.array) == 0

	def long(self):
	return len(self.array)

	def queFront(self):
	if self.isEmpty():
		return None
	return self.array[0]

	def addQue(self,data):
	self.array.append(data)

	def remQue(self):
	if(self.isEmpty):
		print("QUEUE IS EMPTY")
	self.array.pop

	def __str__(self):
	ans = '['
	for i in range(self.long()):
	if len(ans)>1:
		ans += ", "
		ans = ans + self.array[i]
	ans += ']'
	return ans
```

# Stack
- Sebuah antrian, biasa diimplementasikan dengan list.
- Mengikuti prinsip Last in, First out (LIFO)
- Metode:
	- `Pop()`, menghapus dan mengembalikan nilai paling terakhir
	- `Print()`, meng-print keseluruhan list
	- `Append(n)`, menambahkan nilai `n` ke stack
- Kode:
```Python
class Stack:
	def __init__(self):
	self.items = []

	def push(self,item):
	self.items.append(item)

	def pop(self):
	return self.items.pop()

	def isEmpty(self):
	return (self.items == [])

	def peek(self):
	return self.items[-1]

	def __str__(self):
	return str(self.items)
```