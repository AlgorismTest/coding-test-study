## ๐ 1์ฃผ์ฐจ ๊ฐ๋ ์ ๋ฆฌ

## ์๋ฃ๊ตฌ์กฐ
### ๊ฐ๋ 
๋๋์ ๋ฐ์ดํฐ๋ฅผ ํจ์จ์ ์ผ๋ก ๊ด๋ฆฌํ  ์ ์๋ ๋ฐ์ดํฐ์ ๊ตฌ์กฐ
<Br>
์ด๋ค ๋ฐ์ดํฐ ๊ตฌ์กฐ๋ฅผ ์ฌ์ฉํ๋๋์ ๋ฐ๋ผ ์ฝ๋์ ํจ์จ์ด ๋ฌ๋ผ์ง ์ ์์ผ๋ฏ๋ก ์ ์ ํ ์๋ฃ๊ตฌ์กฐ๋ฅผ ์ ์ ํ๋ ๊ฒ์ด ๋งค์ฐ ์ค์ํ๋ค.

### ์๋ฃ๊ตฌ์กฐ์ ๋ถ๋ฅ
์ ํ๊ตฌ์กฐ
- ๋ฐฐ์ด
- ์ฐ๊ฒฐ๋ฆฌ์คํธ
- ์คํ
- ํ

๋น์ ํ๊ตฌ์กฐ
- ํธ๋ฆฌ
- ๊ทธ๋ํ

## Stack
### ๊ฐ๋
๋ฐ์ดํฐ๋ฅผ ์์๋๋ก ์๋ ์๋ฃ๊ตฌ์กฐ

### ํน์ง
- ํ์ ์ ์ถ(LIFO) ๊ตฌ์กฐ
    - ๋ง์ง๋ง์ ๋ค์ด์จ ๋ฐ์ดํฐ๊ฐ ๋จผ์  ๋๊ฐ๋ ๋ฐ์ดํฐ ๊ตฌ์กฐ
- ๋ฐ์ดํฐ ์์ ์๊ด์์ด ๋ฌด์กฐ๊ฑด ํ๋์ฉ๋ง ๋ฃ๊ฑฐ๋ ๋บ ์ ์๋ค
- ํ๋์ ์์ถ๋ ฅ ๋ฐฉํฅ์ ๊ฐ์ง๋ค.
- ์ ํํ๊ณ  ์ ์ ์ธ ๋ฐ์ดํฐ๋ง ์ ์ฅํ  ์ ์๋ค.
- ์คํ์ ํฌ๊ธฐ๋ ์ ํ๋์ด ์๋ค.

### Stack ํด๋์ค ๋ฉ์๋
```java
import java.util.Stack;

public class StackExample {

  public static void main(String[] args) {
      
    // ์ ์ธํ๊ธฐ  
      
    // String ํ์ ์ ์ธ  
    Stack<String> stack = new Stack<>();
    // Char ํ์ ์ ์ธ
    Stack<Character> chStack = new Stack<Character>();
    // Integer ํ์ ์ ์ธ
    Stack<Integer> iStack = new Stack<Integer>();
    // ๋ค ํ์ ์๋ต ๊ฐ๋ฅ
    Stack<Integer> iStack2 = new Stack<>();
    
    // ๋ฉ์๋
    
    // Stack์ ๋ฐ์ดํฐ ์ถ๊ฐ
    stack.push("Data1");
    stack.push("Data2");
    stack.push("Data3");

    // Stack์์ ๋ฐ์ดํฐ ๊บผ๋ด๊ธฐ
    System.out.println(stack.pop());

    // Stack์ ์ต์๋จ ๊ฐ ์ถ๋ ฅ(์ ๊ฑฐํ์ง ์์)
    System.out.println(stack.peek());

    // Stack์์ ๋ฐ์ดํฐ ๊บผ๋ด๊ธฐ
    System.out.println(stack.pop());
    
    // Stack ์ฌ์ด์ฆ ํ์ธํ๊ธฐ
    System.out.println(stack.size());
    
    // Stack ์ด๊ธฐํํ๊ธฐ 
    System.out.println(stack.clear());
    
    // Stack ๋น์ด์๋์ง ์ฌ๋ถ ํ๋จ
    // Boolean true or false ๋ฆฌํด
    System.out.println(stack.empty());
    
    // Stack์ ํน์  ๋ฐ์ดํฐ๊ฐ ํฌํจ๋์ด ์๋์ง ํ์ธ
    // Boolean true or false ๋ฆฌํด
    System.out.println(stack.contains("Data1"));
  }
}
```
<br>

> ์คํ ์ค๋ฒํ๋ก์ฐ
> <br>
> ๊ฝ ์ฐฌ ์คํ์ ๋ฐ์ดํฐ ์์๋ฅผ ๋ฃ์ผ๋ ค ํ  ๋ ๋ฐ์
> <br>
> <br>
> ์คํ ์ธ๋ํ๋ก์ฐ
> <br>
> ๋น์ด์๋ ์คํ์์ ๋ฐ์ดํฐ ์์๋ฅผ ๊บผ๋ด๋ คํ  ๋ ๋ฐ์

### ์คํ ํ์ฉ ์์
- ์น ๋ธ๋ผ์ฐ์  ๋ค๋ก ๊ฐ๊ธฐ : ๊ฐ์ฅ ๋์ค์ ์ด๋ฆฐ ํ์ด์ง๋ถํฐ ๋ค๋ก ๊ฐ๊ธฐ ์คํ
- ๋ฌธ์์์์์ Ctrl+Z : ๊ฐ์ฅ ๋์ค ์์ ํ ๋ด์ญ๋ถํฐ ๋๋๋ฆฐ๋ค
- ์ญ์ ๋ฌธ์์ด ๋ง๋ค๊ธฐ : ๋งจ ๋์ ๋ฌธ์์ด๋ถํฐ ์ฐจ๋ก๋๋ก ๋ง๋ค์ด์ง๋ค
- ํ์ ํ๊ธฐ๋ฒ ๊ณ์ฐ
- ์ฌ๊ท์  ์๊ณ ๋ฆฌ์ฆ

## Queue
### ๊ฐ๋
๋จผ์  ์ง์ด๋ฃ์ ๋ฐ์ดํฐ๊ฐ ๋จผ์  ๋์ค๋ ๊ตฌ์กฐ

### ํน์ง
- Rear ๋ถ๋ถ์์ ์๋ฃ ์ฝ์
- Front ๋ถ๋ถ์์ ์๋ฃ ์ญ์ 
- ์ ์์ ์ถ ์๋ฃ๊ตฌ์กฐ

### Queue ํด๋์ค ๋ฉ์๋
```java
import java.util.LinkedList;

public class QueueExample {

  public static void main(String[] args) {

    // ์ ์ธํ๊ธฐ  

    // Queue ํด๋์ค ์ ์ธ
    Queue queue = new LinkedList();

    // Integerํ์์ผ๋ก ์ ์ธ
    Queue<Integer> i = new LinkedList<Integer>();
    // new๋ถ๋ถ ํ์ ์๋ต ๊ฐ๋ฅ
    Queue<Integer> i2 = new LinkedList<>();
    // ์ ์ธ๊ณผ ๋์์ ์ด๊ธฐ๊ฐ ์ธํ
    Queue<Integer> i3 = new LinkedList<Integer>(Arrays.asList(1, 2, 3));
    // Stringํ์ ์ ์ธ
    Queue<String> str = new LinkedList<String>();
    // Characterํ์ ์ ์ธ    
    Queue<Character> ch = new LinkedList<Character>();

    // ๋ฉ์๋

    // Queue์ ๊ฐ ์ถ๊ฐ
    que.add("Hello");
    que.add("World");
    queue.offer("hi");

    // ๋งจ ์์ ๊ฐ ์ญ์ 
    que.poll();
    // ๋งจ ์์ ๊ฐ ์ญ์ 
    que.remove();
    // ํด๋นํ๋ ๊ฐ ์ญ์ 
    que.remove("Hello");

    // Queue ํค๋ ์์ ํ์ธ ๋ฐ ๋ฐํ
    System.out.println(que.peek());
    
    // Queue ๋น์๋์ง ํ์ธ
    // true false ๋ฆฌํด
    System.out.println(que.isEmpty());
    
    // Queue ๊ฐ ํฌํจ ์ฌ๋ถ
    // true false ๋ฆฌํด
    System.out.println(que.continas("Hello"));
    
    // Queue ์ฌ์ด์ฆ ํ์ธํ๊ธฐ
    System.out.println(que.size());

    // Queue ์ด๊ธฐํํ๊ธฐ
    System.out.println(que.clear());
    
  }
}
  
  
```

### ํ์ ํ์ฉ ์์
- ์ํ์ฐฝ๊ตฌ ๋ฒํธํ ๋๊ธฐ : ๋น ๋ฅธ ๋ฒํธํ๋ฅผ ๊ฐ์ง ์ฌ๋์ด ๋จผ์  ์๋ฌด๋ฅผ ๋ณธ๋ค
- ์ปดํจํฐ ์ด์์ฒด์  ์ค์ผ์ค๋ง : ๊ฐ์ฅ ๊ฐ๋จํ ํํ์ ์ ์์  ์ฒ๋ฆฌ ์ค์ผ์ค๋ง ์ ์ฑ
- ๋๋น ์ฐ์  ํ์ ์๊ณ ๋ฆฌ์ฆ 
