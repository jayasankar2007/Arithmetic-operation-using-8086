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
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


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

<img width="624" height="1280" alt="image" src="https://github.com/user-attachments/assets/839c2e85-0554-4d1f-857e-93885be70898" />



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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200: 12          |        1204: 00          |
|       1201: 34          |        1205: 00          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: C4          |

#### Manual Calculations

![photo_2025-08-24_09-18-23](https://github.com/user-attachments/assets/f4a408b7-c3eb-4c2b-a9c3-b9d4ee9f8066)




## OUTPUT SCREEN FROM MASM SOFTWARE


<img width="626" height="439" alt="Screenshot 2025-08-20 205606" src="https://github.com/user-attachments/assets/479bd444-d224-4b0a-adf7-da16ce400885" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



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
<img width="1061" height="1280" alt="image" src="https://github.com/user-attachments/assets/bc65c34c-6a8d-4302-b6d9-cb222b478c4b" />


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="447" alt="Screenshot 2025-08-20 210258" src="https://github.com/user-attachments/assets/4efff547-e29c-4626-9543-a299f67753cc" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


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
![photo_2025-08-24_09-18-23 (2)](https://github.com/user-attachments/assets/05ab91c2-bf2b-4248-a539-bd3b9b533797)



## OUTPUT FROM MASM SOFTWARE

<img width="633" height="443" alt="Screenshot 2025-08-20 212117" src="https://github.com/user-attachments/assets/c224c62f-bfd9-4ced-848a-fa7faa16c25b" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
