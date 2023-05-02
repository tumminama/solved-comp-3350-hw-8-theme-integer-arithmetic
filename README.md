Download Link: https://assignmentchef.com/product/solved-comp-3350-hw-8-theme-integer-arithmetic
<br>
<ol>

 <li>In the following code sequence, show the value of AL after each shift or rotate instruction has executed. This question is to be done by hand, not programmatically. mov cl, 3</li>

</ol>

mov al, 45h

<table width="146">

 <tbody>

  <tr>

   <td width="73"><strong>01000101 </strong></td>

   <td width="73"><strong> </strong></td>

  </tr>

  <tr>

   <td width="73"><strong>10001010 </strong></td>

   <td width="73"><strong>CF = 0 </strong></td>

  </tr>

  <tr>

   <td width="73"><strong>00010101 </strong></td>

   <td width="73"><strong>CF = 1 </strong></td>

  </tr>

  <tr>

   <td width="73"><strong>00101010 </strong></td>

   <td width="73"><strong>CF = 0 </strong></td>

  </tr>

 </tbody>

</table>

rol al, cl           ;       al = 2Ah













mov al, 7Ah

mov cl, 1

<table width="146">

 <tbody>

  <tr>

   <td width="73"><strong>01111010           </strong></td>

   <td width="73"><strong> </strong></td>

  </tr>

  <tr>

   <td width="73"><strong>00111101 </strong></td>

   <td width="73"><strong>CF = 0 </strong></td>

  </tr>

 </tbody>

</table>

ror al, Cl           ;       al = 3Dh

<strong> </strong>




stc

mov al, 64h         mov cl, 2

<table width="146">

 <tbody>

  <tr>

   <td width="73"><strong>01100100 </strong></td>

   <td width="73"><strong>CF = 1 </strong></td>

  </tr>

  <tr>

   <td width="73"><strong>11001001 </strong></td>

   <td width="73"><strong>CF = 0 </strong></td>

  </tr>

  <tr>

   <td width="73"><strong>10010010 </strong></td>

   <td width="73"><strong>CF = 1 </strong></td>

  </tr>

 </tbody>

</table>

rcl al, cl           ;       al = 92h

<strong><em> </em></strong>







stc

mov al, 3Dh         mov cl, 1

<table width="151">

 <tbody>

  <tr>

   <td width="78"><strong>00111101 </strong></td>

   <td width="73"><strong>CF = 1 </strong></td>

  </tr>

  <tr>

   <td width="78"><strong>10011110 </strong></td>

   <td width="73"><strong>CF = 0 </strong></td>

  </tr>

 </tbody>

</table>

rcr al, cl           ;       al =







<ol start="2">

 <li>(a) Write a program that calculates EAX*<em>17<sub>10</sub></em> using binary multiplication.</li>

</ol>







<ul>

 <li>Consider the following value: A24E6C8D. Let this value be stored in register EAX.  Write a program that will extract the decimal digits from this value using shifts and logical instructions.</li>

</ul>

Place the first two <strong>decimal numeric</strong> digits in DH and the other two into DL.  Submit a print out of the run of the program and the list file.




<strong> </strong>

<ol start="3">

 <li>(a) What will be the contents of AX and DX after the following operation? You must work this problem by hand, not by a program run.  What may happen if you do not set dx to 0 in the beginning?  mov dx, 0  mov ax, 1234h  mov cx, 4213h  mul cx</li>

</ol>







<strong>DX = 04B2 </strong>

<strong>AX = C1DC </strong>

<strong> </strong>

<strong>DX may be different value. </strong>




<ul>

 <li>When does an IDIV instruction cause an overflow? Provide an example.</li>

</ul>




<strong>Mov ax, 4000h </strong>

<strong>Mov dx, 500h </strong>

<strong>Mov bx, 10h </strong>

<strong>Idiv bx </strong>

<strong> </strong>

<strong>OF = 1 </strong>




<ul>

 <li>What will be the values of DX:AX after the following instructions execute? What might be the use of such a sequence of instructions in a 16-bit computer?</li>

</ul>

mov ax, 0h  mov dx, 0h  sub ax, 1h

sbb dx, 0




<strong>DX:AX = FFFF:FFFF </strong>

<strong>       To subtract numbers larger than 16 bits. </strong>




<ol start="4">

 <li>Implement the following two expressions in assembly language, using 32-bit signed operands. Demonstrate the equivalence of the two using some test values for X and Y.  Show the runs of the programs using both positive and negative test values.  Which of the two implementations is preferable?</li>

</ol>

<em>Z = X<sup>2</sup> + 2XY + Y<sup>2</sup> </em>

<em>Z = (X+Y)<sup>2</sup>   </em>










<strong>The second one is preferable because of less code. </strong>

<strong> </strong>

<ol start="5">

 <li>Write a program that performs C = A – B using extended subtraction. See textbook pg. 270-271.  <em> </em></li>

</ol>

Use the following:

Apple       WORD  1214h, 3423h, 6578h, 5699h, 2005h

Berry       WORD  4125h, 2345h, 12BCh, 0CDF1h, 1009h

Cherry      WORD  5dup(0)

Submit the list file and a display of the contents of all the arrays after the run.

<em> </em>