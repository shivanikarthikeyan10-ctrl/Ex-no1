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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200🔢       01         12

|         1200                    |

#### Manual Calculations

(Add your calculation here)

---
<img width="1307" height="1086" alt="image" src="https://github.com/user-attachments/assets/ff580416-da52-4d64-a70f-cd99af225599" />

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="650" height="452" alt="WhatsApp Image 2026-05-14 at 9 47 00 AM" src="https://github.com/user-attachments/assets/a29c7475-0568-40e4-92cf-26966bdc8ac3" />


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
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---
<img width="1600" height="868" alt="WhatsApp Image 2026-05-14 at 10 13 46 AM" src="https://github.com/user-attachments/assets/eeb12323-630a-4132-87f0-60582c58b389" />
<img width="1430" height="453" alt="WhatsApp Image 2026-05-14 at 10 13 58 AM" src="https://github.com/user-attachments/assets/5aa641c8-a45c-4a82-a906-74d1b9771ef9" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="648" height="433" alt="WhatsApp Image 2026-05-14 at 10 14 22 AM" src="https://github.com/user-attachments/assets/7b391781-b7db-4761-b438-73040ed9dfaa" />


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
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---
<img width="1600" height="1139" alt="WhatsApp Image 2026-05-14 at 10 14 59 AM" src="https://github.com/user-attachments/assets/c416fdde-9a4e-483c-8fa9-eec9aea59f8d" />

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="641" height="426" alt="image" src="https://github.com/user-attachments/assets/761062c9-4fb2-4ca8-95c4-0cd82c232108" />


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
|                         |                          |

#### Manual Calculations

(Add your calculation here)

-<img width="1600" height="1338" alt="image" src="https://github.com/user-attachments/assets/51c54b2a-a2ab-4f51-8a38-1f66b05965a2" />
--

## OUTPUT FROM MASM SOFTWARE
<img width="643" height="430" alt="image" src="https://github.com/user-attachments/assets/5a361d3e-e01f-4ed2-aaa9-0b27528dac2a" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

