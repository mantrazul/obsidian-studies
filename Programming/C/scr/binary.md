
#### About binary

Computers today count using a system called *binary*. It's from the term *binary digit* that we get a familiar term called *bit*. A *bit* is a zero or one.

Computers only speak in terms of zeros and ones. 

- Zero represent *off*.
- One represent *on*.

Computers are millions, and perhaps billions, of transistors that are being turned on and off.

If you imagine using a light bulb, a single bulb can only count from zero to one.

- Using three light bulbs, the following could represent zero:
    
    ```
      0 0 0
    ```
    
- Similarly, the following would represent one:
    
    ```
      0 0 1
    ```
    
- By this logic, we could propose that the following equals two:
    
    ```
      0 1 0
    ```
    
- Extending this logic further, the following represents three:
    
    ```
      0 1 1
    ```
    
- Four would appear as:
    
    ```
      1 0 0
    ```
    
- We could, in fact, using only three light bulbs count as high as seven!
    
    ```
      1 1 1
    ```
    
- As a heuristic, we could imagine that the following values represent each possible place in our _binary digit_:
    
    ```
      4 2 1
    ```
    
- Computers use ‘base-2’ to count. This can be pictured as follows:
    
    ```
      2^2  2^1  2^0
      4    2    1
    ```
    

Therefore, you could say that it would require three bits (the four’s place, the two’s place, and the one’s place) to represent a number as high as seven.

Computers generally use eight bits to represent a number. For example, `00000101` is the number 5 in _binary_.