# COBOL Cheatsheet

## Data Division

The Data Division is where the record structure of a COBOL program is defined. It contains four sections:

- File Section
- Working-Storage Section
- Linkage Section
- Report Section

```COBOL
    IDENTIFICATION DIVISION.
    DATA DIVISION.
    FILE SECTION.
    WORKING-STORAGE SECTION.
    LINKAGE SECTION.
    REPORT SECTION.
```

## File Section

The File Section is where file descriptions are defined. A file description includes the name of the file, the organization of the file (Sequential, Indexed, etc.), the access mode (Sequential, Random, Dynamic), and the file's record description.

```COBOL
    FD <file-name>
        LABEL RECORDS ARE STANDARD.
        DATA RECORD IS <record-name>.
        <file description>.
```

## Working-Storage Section

The Working-Storage Section is used to define variables and intermediate results used by the program.

```COBOL
    01 <variable-name> PIC <picture clause >.
```

## Linkage Section

The Linkage Section is used to pass data between programs.

```COBOL
    01 <variable-name> PIC < picture clause >.
```

## Report Section

The Report Section is used to describe the layout of a report and its individual data items.

```COBOL
    REPORT SECTION.
    RD <report-name>
        <report description>.
    PAGE HEADING <report-name>
        <page heading description>.
```

## Procedure Division

The Procedure Division is where the logic of the program is written. It contains statements that perform specific operations, such as accepting input, performing calculations, and displaying output.

```COBOL
    IDENTIFICATION DIVISION.
    PROGRAM-ID. HELLO-WORLD.
    PROCEDURE DIVISION.
    DISPLAY "Hello, World!".
    STOP RUN.
```

## Arithmetic Operations

COBOL supports the following arithmetic operations:

- ADD
- SUBTRACT
- MULTIPLY
- DIVIDE
- COMPUTE

```COBOL
    ADD <operand-1> TO <operand-2> GIVING <result>.
    SUBTRACT <operand-1> FROM <operand-2> GIVING <result>.
    MULTIPLY <operand-1> BY <operand-2> GIVING <result>.
    DIVIDE <operand-1> BY <operand-2> GIVING <result>.
    COMPUTE <result> = <expression>.
```

## Conditional Statements

COBOL supports the following conditional statements:

- IF statement
- EVALUATE statement

```COBOL
    IF <condition>
        <statements>.
    END-IF.

    EVALUATE <expression>
        WHEN <value-1>
            <statements>
        WHEN <value-2>
            <statements>
        WHEN <value-3>
            <statements>
        WHEN OTHER
            <statements>
    END-EVALUATE.
```

## Looping Constructs

COBOL supports the following looping constructs:

- PERFORM statement
- DO statement
- GO TO statement

```COBOL
    PERFORM <paragraph-name> UNTIL <condition>.

    DO <counter> TIMES
        <statements>
    END-DO.

    GO TO <paragraph-name>.
```

## Input/Output Operations

COBOL supports the following input/output operations:

- ACCEPT statement
- DISPLAY statement

```COBOL
    ACCEPT <variable-name>.
    DISPLAY <expression>.
```
