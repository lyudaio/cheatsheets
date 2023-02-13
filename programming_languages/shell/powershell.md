# PowerShell (7.2.0)

PowerShell is a task-based command-line shell and scripting language built on .NET. It helps to automate administrative tasks and manage different components of Windows operating systems.

## Variables

Variables in PowerShell are declared using the `$` symbol.

```powershell
$x = 10
$y = 20
$z = $x + $y
Write-Output $z
```

## Loops

PowerShell has several ways to write loops.

### For Loop

A for loop can be written using the `For` keyword.

```powershell
For ($i = 0; $i -lt 10; $i++) {
  Write-Output $i
}
```

### Foreach Loop

A foreach loop can be written using the `Foreach` keyword.

```powershell
$numbers = 1,2,3,4,5
Foreach ($number in $numbers) {
  Write-Output $number
}
```

## Functions

Functions in PowerShell are declared using the `Function` keyword.

```powershell
Function Square($x) {
  return $x * $x
}
Write-Output (Square 10)
```
