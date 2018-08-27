# Java集合Queue的使用

## 1. add/offer/put

使用这三个方法都可以向队列的尾部插入一个元素

- add

添加成功，返回true，但当队列已满时，会抛出IllegalStateException异常

- offer

添加成功，返回true，当队列已满添加失败时，返回false
可以也可以传入一个尝试等待时间，尝试一段时间后若队列仍然已满无法添加，再返回false

- put

无返回值，可保证添加成功，若队列已满，则阻塞直至添加成功

## 2. remove/poll/take

使用这三个方法可以删除队头并返回该对象

- remove

若为空集合，抛出NoSuchElementException异常，若不是，则删除队头并返回

- poll

若为空集合，返回null，若不是，则删除队头并返回
可以也可以传入一个尝试等待时间，尝试一段时间后若队列仍然为空，再返回null

- take

若为空集合，则一直阻塞直至队列不为空集合时，删除队头并返回

## 3. peek/element

- peek

获取队头对象，若为空队列，则返回null

- element

获取队头对象，若为空队列，则抛出NoSuchElementException异常