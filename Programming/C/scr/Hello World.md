- Machine only understand binary. Where humans write **source code**, a list of instructions for the computer that is human readable, machines only understand what we can call **machine code**. This machine code is a pattern of ones and zeros that produces a desired effect.
- We can convert **source code** into `machine code` using a very special piece of software called a **compiler**.

##### Three Axis of Code

Code can be evaluated upon three axes:

1. **Correctness**: refers to "does the code run as intended?"
2. **Design**: refers to "how well is the code designed?"
3. **Style**: refers to "how aesthetically pleasing and consistent is the code?"

### Hello World

```C
#include <stdio.h>

int main(void)
{
	printf("hello, workd\n");
}
```


### Computational Thinking

Essentially, computer programming is about taking some input and creating some output. - thus solving a problem. What happens in between the input and output, what we could call a *black box*, is the focus of this course.

![[Pasted image 20231109200831.png]]

For example:

We could use a system called *unary* to count, one finger at a time. Computers today count using a system called *[[binary]]*.

### Text

Just as n numbers are binary patterns of ones and zeros, letters are represented using ones and zeros too!

Since there is an overlap between the ones and the zeros that represent numbers and letters, the *ASCII* standard was created to map specific letters to specific numbers,

For example, the letter `A` was decided to map to the number 65.

f you received a text message, the binary under that message might represent the numbers 72, 73, and 33. Mapping these out to ASCII, your message would look as follows:

```
  H   I   !
  72  73  33
```

![[Pasted image 20231109201630.png]]

### Emojis

As time has rolled on, there are more and more ways to communicate via text.

Computer scientists faced a challenge when wanting to assign various skin tones to each emoji to allow the communication to be further personalised. In this case, the creators and contributors of emojis decided that the initial bits would be the structure of the emoji itself, followed by skin tone.

## Algorithms

Problem-solving is central to computer science and computer programming.

Imagine the basic problem of trying to locate a single name in a phone book.

How might you go about this?

One approach could be to simply read from page one to the next to the next until reaching the last page.

Another approach could be to search two pages at a time.

A final and perhaps better approach could be to go to the middle of the phone book and ask, “Is the name I am looking for to the left or to the right?” Then, repeat this process, cutting the problem in half and half and half.

Each of these approaches could be called algorithms. The speed of each of these algorithms can be pictured as follows in what is called _big-O notation_:

![[Pasted image 20231109202025.png]]


> [!NOTE]
> Notice that the first algorithm, highlighted in red, has a big-O of `n` because if there are 100 names in the phone book, it could take up to 100 tries to find the correct name. The second algorithm, where two pages were searched at a time, has a big-O of ‘n/2’ because we searched twice as fast through the pages. The final algorithm has a big-O of log2n as doubling the problem would only result in one more step to solve the problem.
