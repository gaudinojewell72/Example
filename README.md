# Example
Func _ScreenToClient($hWindow, ByRef $aCoord) ; convert screen coords to $hWindow client coords (i.e mouse to listview, or listview to GUI, or mouse to header...)     Local $tPoint = DllStructCreate("int X;int Y")     DllStructSetData($tPoint, "X", $aCoord[0])     DllStructSetData($tPoint, "Y", $aCoord[1])     _WinAPI_ScreenToClient($hWindow, $tPoint)     $aCoord[0] = DllStructGetData($tPoint, "X")     $aCoord[1] = DllStructGetData($tPoint, "Y")     ; ByRef modified the Array in the calling function (+++) include &lt;GUIConstantsEx.au3> #include &lt;GuiListView.au3> #include &lt;MsgBoxConstants.au3> Example()
