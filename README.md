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
|     1200:12 24:1204     |                          |
      1201:34                    68:1205
      1202:12                    00:1206
      1203:34                    c4:1207


#### Manual Calculations


![WhatsApp Image 2025-09-22 at 08 32 38_2f8a9d99](https://github.com/user-attachments/assets/4351e268-cf49-4acd-80ff-1f90a6a93ea8)



## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="646" height="408" alt="Screenshot 2025-09-22 080859" src="https://github.com/user-attachments/assets/9d0d7c69-6096-4acd-88f9-a55891891bbf" />
<img width="633" height="442" alt="Screenshot 2025-08-18 113653" src="https://github.com/user-attachments/assets/33f52101-aa6a-48f1-839a-191e6ca813b1" />


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
|     1200:12 24:1204     |                          |
      1201:34                    68:1205
      1202:12                    00:1206
      1203:34                    c4:1207

#### Manual Calculations
![WhatsApp Image 2025-09-22 at 08 36 44_9a356cd3](https://github.com/user-attachments/assets/9f007a87-ee79-4f55-bd72-dd52b1c772e9)





## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-22 at 08 23 05_971dc4fa](https://github.com/user-attachments/assets/5cb0c424-f13f-40fc-9bf8-1942cdc60764)

<img width="645" height="445" alt="Screenshot 2025-08-18 113509" src="https://github.com/user-attachments/assets/f13b2831-88b4-4d68-bd1c-c1a897191057" />

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
|     1200:12 24:1204     |                          |
      1201:34                    68:1205
      1202:12                    00:1206
      1203:34                    c4:1207
#### Manual Calculations
![WhatsApp Image 2025-09-22 at 08 43 11_36f250bf](https://github.com/user-attachments/assets/49c3fd71-1b96-465d-aa0a-ea821ceb272b)


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-22 at 08 23 05_1c5e6c5a](https://github.com/user-attachments/assets/35f60e27-a8a0-41dd-95a7-00d557f882ff)
<img width="638" height="445" alt="Screenshot 2025-08-18 112949" src="https://github.com/user-attachments/assets/08dbe47a-672b-4511-97ba-616c3d39732d" />

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
|     1200:12 24:1204     |                          |
      1201:34                    68:1205
      1202:12                    00:1206
      1203:34                    c4:1207

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 47 03_de7b40a3](https://github.com/user-attachments/assets/00fc162c-5038-427c-b8ef-e8362620782c)

## OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-09-22 at 08 23 05_2b809010](https://github.com/user-attachments/assets/90514fb2-3e4c-4475-ae0b-b4fd775e5090)
<img width="638" height="434" alt="Screenshot 2025-08-18 112739" src="https://github.com/user-attachments/assets/6e433a14-888f-4673-9bc5-2a164e6dcdc4" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

