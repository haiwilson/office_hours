


frmMain()
centerScreen()

Sub centerScreen
  ' This will get the user's system screen width & height divided by 2
  ' and subtract it from the Form's width & height dived by 2
  ' to center the form on app load
  gw = GraphicsWindow.Width
  gh = GraphicsWindow.Height
  dw = Desktop.Width
  dh = Desktop.Height
  GraphicsWindow.Left = (dw / 2) - (gw / 2)
  GraphicsWindow.Top = (dh / 2) - (gh / 2)
EndSub

' Build Frame
Sub frmMain
  GraphicsWindow.CanResize = 0
  GraphicsWindow.Width = 400
  GraphicsWindow.Height = 350
  GraphicsWindow.Title = "Office Hours"
  GraphicsWindow.BackgroundColor = GraphicsWindow.GetColorFromRGB(240, 240, 240)
  GraphicsWindow.FontBold = "False"
  GraphicsWindow.BrushColor = "Black"
  GraphicsWindow.Show()

  ' Enable the listener for Button Events
  Controls.ButtonClicked = buttonClicked

  ' Buttons:
  closeButton = Controls.AddButton("Close",290,290)
  Controls.SetSize(closeButton,100,50)

' Labels & textBoxes:
  GraphicsWindow.BrushColor = "black"
  GraphicsWindow.FillRectangle(10,70,380,50)
  GraphicsWindow.BrushColor = "#c9fffb"
  GraphicsWindow.FillRectangle(11,71,378,48)
  
  centerText()

  GraphicsWindow.BrushColor = "Black"
  GraphicsWindow.FontBold = "True"
  GraphicsWindow.DrawBoundText(10,30,100, "Current Time:")
  GraphicsWindow.FontBold = "False"
  
  GraphicsWindow.BrushColor = "Black"
  GraphicsWindow.FontBold = "True"
  GraphicsWindow.DrawBoundText(10,150,130, "Portland Office:")
  GraphicsWindow.FontBold = "False"
  
  GraphicsWindow.BrushColor = "Black"
  GraphicsWindow.FontBold = "True"
  GraphicsWindow.DrawBoundText(10,200,130, "New York Office:")
  GraphicsWindow.FontBold = "False"
  
  GraphicsWindow.BrushColor = "Black"
  GraphicsWindow.FontBold = "True"
  GraphicsWindow.DrawBoundText(10,250,130, "London Office:")
  GraphicsWindow.FontBold = "False"
  
  GraphicsWindow.BrushColor = "darkblue"
  GraphicsWindow.FontBold = "True"
  GraphicsWindow.DrawBoundText(300,30,100, "17:28:32 PST")
  GraphicsWindow.FontBold = "False"
  
  port_hour = Clock.Hour
  port_min = Clock.Minute
  
  GraphicsWindow.FontBold = "True"
  getPortTime()
  GraphicsWindow.DrawBoundText(150,150,250, port_time + " " + port_amPm + " - The Oregon branch is " + port_open + ".")
  
  getNyTime()
  GraphicsWindow.DrawBoundText(150,200,250, ny_time + " " + ny_amPm + " - The NY City branch is " + ny_open + ".")
  
  getLonTime()
  GraphicsWindow.DrawBoundText(150,250,250, lon_time + " " + lon_amPm + " - The London branch is " + lon_open + ".")
  GraphicsWindow.FontBold = "False"
  GraphicsWindow.BrushColor = "black"
EndSub

Sub centerText
  ' Character return + Line-feed
  CR = Text.GetCharacter(13) + Text.GetCharacter(10)
  
  'GraphicsWindow.FontName = "Tahoma"
  'GraphicsWindow.FontSize = 12
  GraphicsWindow.BrushColor = "Black"
  GraphicsWindow.FontBold = "True"
  text1 = "All office hours are from:"
  text2 = "9:00 am to 9:00 pm, or (0900) to (2100)."
  
  'Text.GetLength(caption) means the number of characters in the caption.  Default font size (height) is 
  '12 pixels and gross average width of the default font (Tahoma) assumed to be 7 pixels 
  'in this program.  If the window width is gw, centering x position of the caption will be as follows.
  wCaption1 = (Text.GetLength(text1) + 2) * 12 * .4
  wCaption2 = (Text.GetLength(text2) + 2) * 12 * .48
  x1 = Math.Floor((378 - wCaption1) / 2)
  x2 = Math.Floor((378 - wCaption2) / 2)
  GraphicsWindow.DrawBoundText(x1,75,378, text1)
  GraphicsWindow.DrawBoundText(x2,100,378, text2)
 
  'Or, if you use "Courier New" font, the font width is 0.6 times the font height.  So, if the font size (height) 
  'is 12, you can calculate caption width as follows.  
  ' wCaption = (Text.GetLength(caption) + 2) * 12 * 0.6
EndSub
  
' Define the Event functions
Sub buttonClicked
  lastButton = Controls.LastClickedButton
  If lastButton = closeButton Then
      Program.End() 
  EndIf
EndSub
  
Sub getPortTime
  If port_hour = 1 Then
    port_time = 1
    port_amPm = "Am"
    port_open = "false"
  ElseIf port_hour = 2 Then
    port_time = 2
    port_amPm = "Am"
    port_open = "false"
  ElseIf port_hour = 3 Then
    port_time = 3
    port_amPm = "Am"
    port_open = "false"
  ElseIf port_hour = 4 Then
    port_time = 4
    port_amPm = "Am"
    port_open = "false"
  ElseIf port_hour = 5 Then
    port_time = 5
    port_amPm = "Am"
    port_open = "false"
  ElseIf port_hour = 6 Then
    port_time = 6
    port_amPm = "Am"
    port_open = "false"
  ElseIf port_hour = 7 Then
    port_time = 7
    port_amPm = "Am"
    port_open = "false"
  ElseIf port_hour = 8 Then
    port_time = 8
    port_amPm = "Am"
    port_open = "false"
  ElseIf port_hour = 9 Then
    port_time = 9
    port_amPm = "Am"
    port_open = "true"
  ElseIf port_hour = 10 Then
    port_time = 10
    port_amPm = "Am"
    port_open = "true"
  ElseIf port_hour = 11 Then
    port_time = 11
    port_amPm = "Am"
    port_open = "true"
  ElseIf port_hour = 12 Then
    port_time = 12
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 13 Then
    port_time = 1
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 14 Then
    port_time = 2
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 15 Then
    port_time = 3
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 16 Then
    port_time = 4
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 17 Then
    port_time = 5
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 18 Then
    port_time = 6
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 19 Then
    port_time = 7
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 20 Then
    port_time = 8
    port_amPm = "Pm"
    port_open = "true"
  ElseIf port_hour = 21 Then
    port_time = 9
    port_amPm = "Pm"
    port_open = "false"
  ElseIf port_hour = 22 Then
    port_time = 10
    port_amPm = "Pm"
    port_open = "false"
  ElseIf port_hour = 23 Then
    port_time = 11
    port_amPm = "Pm"
    port_open = "false"
  ElseIf port_hour = 0 Then
    port_time = 12
    port_amPm = "Am"
    port_open = "false"
  EndIf
  
  If  port_open = "true" Then
    port_open = "Open"
    GraphicsWindow.BrushColor = "green"
  Else  
    port_open = "Closed"
    GraphicsWindow.BrushColor = "red"
  EndIf
EndSub
  
Sub getNyTime
  ny_hour = port_hour + 3
  If ny_hour = 1 Then
    ny_time = 1
    ny_amPm = "Am"
    ny_open = "false"
  ElseIf ny_hour = 2 Then
    ny_time = 2
    ny_amPm = "Am"
    ny_open = "false"
  ElseIf ny_hour = 3 Then
    ny_time = 3
    ny_amPm = "Am"
    ny_open = "false"
  ElseIf ny_hour = 4 Then
    ny_time = 4
    ny_amPm = "Am"
    ny_open = "false"
  ElseIf ny_hour = 5 Then
    ny_time = 5
    ny_amPm = "Am"
    ny_open = "false"
  ElseIf ny_hour = 6 Then
    ny_time = 6
    ny_amPm = "Am"
    ny_open = "false"
  ElseIf ny_hour = 7 Then
    ny_time = 7
    ny_amPm = "Am"
    ny_open = "false"
  ElseIf ny_hour = 8 Then
    ny_time = 8
    ny_amPm = "Am"
    ny_open = "false"
  ElseIf ny_hour = 9 Then
    ny_time = 9
    ny_amPm = "Am"
    ny_open = "true"
  ElseIf ny_hour = 10 Then
    ny_time = 10
    ny_amPm = "Am"
    ny_open = "true"
  ElseIf ny_hour = 11 Then
    ny_time = 11
    ny_amPm = "Am"
    ny_open = "true"
  ElseIf ny_hour = 12 Then
    ny_time = 12
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 13 Then
    ny_time = 1
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 14 Then
    ny_time = 2
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 15 Then
    ny_time = 3
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 16 Then
    ny_time = 4
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 17 Then
    ny_time = 5
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 18 Then
    ny_time = 6
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 19 Then
    ny_time = 7
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 20 Then
    ny_time = 8
    ny_amPm = "Pm"
    ny_open = "true"
  ElseIf ny_hour = 21 Then
    ny_time = 9
    ny_amPm = "Pm"
    ny_open = "false"
  ElseIf ny_hour = 22 Then
    ny_time = 10
    ny_amPm = "Pm"
    ny_open = "false"
  ElseIf ny_hour = 23 Then
    ny_time = 11
    ny_amPm = "Pm"
    ny_open = "false"
  ElseIf ny_hour = 0 Then
    ny_time = 12
    ny_amPm = "Am"
    ny_open = "false"
  EndIf
  
  If  ny_open = "true" Then
    ny_open = "Open"
    GraphicsWindow.BrushColor = "green"
  Else  
    ny_open = "Closed"
    GraphicsWindow.BrushColor = "red"
  EndIf
EndSub
  
Sub getLonTime
  lon_hour = port_hour + 8
  If lon_hour = 1 Then
    lon_time = 1
    lon_amPm = "Am"
    lon_open = "false"
  ElseIf lon_hour = 2 Then
    lon_time = 2
    lon_amPm = "Am"
    lon_open = "false"
  ElseIf lon_hour = 3 Then
    lon_time = 3
    lon_amPm = "Am"
    lon_open = "false"
  ElseIf lon_hour = 4 Then
    lon_time = 4
    lon_amPm = "Am"
    lon_open = "false"
  ElseIf lon_hour = 5 Then
    lon_time = 5
    lon_amPm = "Am"
    lon_open = "false"
  ElseIf lon_hour = 6 Then
    lon_time = 6
    lon_amPm = "Am"
    lon_open = "false"
  ElseIf lon_hour = 7 Then
    lon_time = 7
    lon_amPm = "Am"
    lon_open = "false"
  ElseIf lon_hour = 8 Then
    lon_time = 8
    lon_amPm = "Am"
    lon_open = "false"
  ElseIf lon_hour = 9 Then
    lon_time = 9
    lon_amPm = "Am"
    lon_open = "true"
  ElseIf lon_hour = 10 Then
    lon_time = 10
    lon_amPm = "Am"
    lon_open = "true"
  ElseIf lon_hour = 11 Then
    lon_time = 11
    lon_amPm = "Am"
    lon_open = "true"
  ElseIf lon_hour = 12 Then
    lon_time = 12
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 13 Then
    lon_time = 1
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 14 Then
    lon_time = 2
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 15 Then
    lon_time = 3
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 16 Then
    lon_time = 4
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 17 Then
    lon_time = 5
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 18 Then
    lon_time = 6
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 19 Then
    lon_time = 7
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 20 Then
    lon_time = 8
    lon_amPm = "Pm"
    lon_open = "true"
  ElseIf lon_hour = 21 Then
    lon_time = 9
    lon_amPm = "Pm"
    lon_open = "false"
  ElseIf lon_hour = 22 Then
    lon_time = 10
    lon_amPm = "Pm"
    lon_open = "false"
  ElseIf lon_hour = 23 Then
    lon_time = 11
    lon_amPm = "Pm"
    lon_open = "false"
  ElseIf lon_hour = 0 Then
    lon_time = 12
    lon_amPm = "Am"
    lon_open = "false"
  EndIf
  
  If  lon_open = "true" Then
    lon_open = "Open"
    GraphicsWindow.BrushColor = "green"
  Else  
    lon_open = "Closed"
    GraphicsWindow.BrushColor = "red"
  EndIf
EndSub
