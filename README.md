<div align="center">

## How to dynamically create multiple controls?


</div>

### Description

Automatically add controls to the form at runtime, (by code, programmatically) and react to their events
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[SoTTo](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/sotto.md)
**Level**          |Beginner
**User Rating**    |5.0 (30 globes from 6 users)
**Compatibility**  |VB\.NET
**Category**       |[Controls/ Forms/ Dialogs/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-dialogs-menus__10-3.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/sotto-how-to-dynamically-create-multiple-controls__10-406/archive/master.zip)

### API Declarations

```
Copyrighted by SoTTo,
let me know if you use this code by writing something in my guestbook on http://www.sotto.tk
```


### Source Code

```
Dim chk() As CheckBox
 Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load
  Dim i As Integer
  For i = 0 To 5
   ReDim Preserve chk(i)
   chk(i) = New CheckBox()
   chk(i).Text = "check " & i
   chk(i).Top = chk(i).Height * i
   chk(i).Left = 0
   chk(i).Name = "chk" & i
   Me.Controls.Add(chk(i))
   AddHandler chk(i).CheckStateChanged, AddressOf chk_CheckedChanged
  Next
 End Sub
 Private Sub chk_CheckedChanged(ByVal sender As System.Object, ByVal e As
System.EventArgs)
  MsgBox("checkbox " & sender.name & "'s state changed to " & sender.Checked)
 End Sub
```

