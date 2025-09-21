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
|  2000                   |   79                     | 
|  2001                   |   88                     |
|  2002                   |   23                     |
|  2003                   |   02                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   9C                     | 
|  2005                   |   8A                     |
|  2006                   |   00                     |

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 23 09 24_7ac05946](https://github.com/user-attachments/assets/6b7a412c-d2a4-47c2-8ffe-b20acfcc38af)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="643" height="434" alt="Screenshot 2025-09-21 231044" src="https://github.com/user-attachments/assets/3cad3d5c-6aa6-4d44-b9b9-6d6c5b087f55" />

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
|  2000                   |   79                     | 
|  2001                   |   88                     |
|  2002                   |   23                     |
|  2003                   |   02                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   56                     | 
|  2005                   |   86                     |
|  2006                   |   00                     |
#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 23 09 23_64c51d28](https://github.com/user-attachments/assets/03670e5c-ab76-49a7-8bbe-7407ed6b29f1)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="652" height="441" alt="Screenshot 2025-09-21 231519" src="https://github.com/user-attachments/assets/d888c4b0-4cfe-42b9-ac74-dad534815863" />

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
|  2000                   |   02                     | 
|  2001                   |   00                     |
|  2002                   |   03                     |
|  2003                   |   00                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   06                     | 
|  2005                   |   00                     |
|  2006                   |   00                     |

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 23 09 22_8727a9aa](https://github.com/user-attachments/assets/de720330-b880-4166-94b5-c370f4682a10)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="641" height="442" alt="Screenshot 2025-09-21 232339" src="https://github.com/user-attachments/assets/7595efac-d329-4125-9666-0b597143faf1" />

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
|  2000                   |   69                     | 
|  2001                   |   24                     |
|  2002                   |   34                     |
|  2003                   |   12                     |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2004                   |   02                     | 
|  2005                   |   00                     |
|  2006                   |   01                     |
#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 23 09 23_50eb9298](https://github.com/user-attachments/assets/9c761a05-8b80-4750-ac33-3046acb2cad0)

---
## OUTPUT FROM MASM SOFTWARE
<img width="646" height="436" alt="Screenshot 2025-09-21 232832" src="https://github.com/user-attachments/assets/1b64b3ca-d3d7-4130-9b21-acb23afe0968" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

