# 잡기술(Job-Technology)

# 1. Read, Write, X

Changing read/write settings of a particular file.

r(read) = 4, w(write) = 2, x = 1

First place: Me
Second place: Group members
Third place: Others

```bash
chmod 751 hello.c
```

- The example above implies that I(me) can read&write, group members can only read, and others can do neither of those.

> 😬Example 😬

![%E1%84%8C%E1%85%A1%E1%86%B8%E1%84%80%E1%85%B5%E1%84%89%E1%85%AE%E1%86%AF(Job-Technology)%20dbddebef4a624271b538325efb985a4f/Untitled.png](%E1%84%8C%E1%85%A1%E1%86%B8%E1%84%80%E1%85%B5%E1%84%89%E1%85%AE%E1%86%AF(Job-Technology)%20dbddebef4a624271b538325efb985a4f/Untitled.png)

Current state of hello.c is                            -rw-r—r—
It is 644

![%E1%84%8C%E1%85%A1%E1%86%B8%E1%84%80%E1%85%B5%E1%84%89%E1%85%AE%E1%86%AF(Job-Technology)%20dbddebef4a624271b538325efb985a4f/Untitled%201.png](%E1%84%8C%E1%85%A1%E1%86%B8%E1%84%80%E1%85%B5%E1%84%89%E1%85%AE%E1%86%AF(Job-Technology)%20dbddebef4a624271b538325efb985a4f/Untitled%201.png)

After chmod 777 hello.c, the state of hello.c becomes                   -rwxrwxrwx

# 2. Touch, Cat, Move, Copy

## 2-1 Touch

Touch literally does nothing but changes lastly modified time of particular file.

```bash
touch hello.c
```

## 2-2 Cat, ls

Cat provides a brief overview of a file. 

```bash
cat hello.c
```

![%E1%84%8C%E1%85%A1%E1%86%B8%E1%84%80%E1%85%B5%E1%84%89%E1%85%AE%E1%86%AF(Job-Technology)%20dbddebef4a624271b538325efb985a4f/Untitled%202.png](%E1%84%8C%E1%85%A1%E1%86%B8%E1%84%80%E1%85%B5%E1%84%89%E1%85%AE%E1%86%AF(Job-Technology)%20dbddebef4a624271b538325efb985a4f/Untitled%202.png)

```bash
ls -al
```

## 2-3 Copy and Move

```bash
cp hello.c hello1.c
mv hello1.c hello2.c
```

cp duplicates hello.c and creates hello1.c
mv changes hello1.c's name into hello2.c

# 3. Search

## 3-1 S notation

```bash
:1,$s/^*[a-z][fuckfuckfuck]*$
```

- 위와 같은 명령어는 한 단어로만 이루어진 줄을 찾는다.
- 이러면 각각 따로 정리 안해도 돼서 좋다.