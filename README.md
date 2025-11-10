# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="321" height="750" alt="image" src="https://github.com/user-attachments/assets/29ba5374-3a53-4fa6-b48e-4459cca19dd8" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 24          |
|       1201: 34          |        1205: 68          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: C4          |

#### Manual Calculations

<img width="312" height="640" alt="481343710-839c2e85-0554-4d1f-857e-93885be70898" src="https://github.com/user-attachments/assets/f0919bf2-cbb4-4e1f-af3b-8c8b9afef1e3" />



## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="638" height="439" alt="Screenshot 2025-08-20 204430" src="https://github.com/user-attachments/assets/1c08759d-375e-4d27-8a4c-9dcf455a5ba1" />



## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 00          |
|       1201: 34          |        1205: 00          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: C4          |

#### Manual Calculations

<img width="402" height="793" alt="image" src="https://github.com/user-attachments/assets/50d5e982-20f2-429d-85e6-5eee055b24fd" />




## OUTPUT SCREEN FROM MASM SOFTWARE


<img width="626" height="439" alt="Screenshot 2025-08-20 205606" src="https://github.com/user-attachments/assets/479bd444-d224-4b0a-adf7-da16ce400885" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="406" height="646" alt="image" src="https://github.com/user-attachments/assets/8d2420b2-febd-40f2-a482-b859c46f7c93" />




#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 44          |
|       1201: 34          |        1205: 51          |
|       1202: 12          |        1206: 97          |
|       1203: 34          |        1207: 0A          |

#### Manual Calculations
<img width="546" height="658" alt="image" src="https://github.com/user-attachments/assets/9d530dc5-f288-48e7-8c1a-51ec66ff7b6e" />



## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="447" alt="Screenshot 2025-08-20 210258" src="https://github.com/user-attachments/assets/4efff547-e29c-4626-9543-a299f67753cc" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="397" height="595" alt="image" src="https://github.com/user-attachments/assets/1876f31f-4394-4078-bd24-234d314c5eeb" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 01          |
|       1201: 34          |        1205: 00          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: 00          |

#### Manual Calculations
<img width="462" height="615" alt="image" src="https://github.com/user-attachments/assets/089e06eb-90fe-449b-8017-95e26290d323" />



## OUTPUT FROM MASM SOFTWARE

<img width="633" height="443" alt="Screenshot 2025-08-20 212117" src="https://github.com/user-attachments/assets/c224c62f-bfd9-4ced-848a-fa7faa16c25b" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
