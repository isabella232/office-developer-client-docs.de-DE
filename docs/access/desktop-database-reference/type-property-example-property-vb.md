---
<<<<<<< HEAD-Titel: Type-Eigenschaft (Beispiel) (VB) TOCTitle: Type-Eigenschaft (Beispiel) (VB) === Titel: Type-Eigenschaft (Beispiel) (VB) TOCTitle: Type-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: b3fecd24-e15a-3216-e2c8-0f4ce5655b9c Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249858(v=office.15) Ms:contentKeyID: 48547209 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="type-property-example-property-vb"></a>Type-Eigenschaft (Beispiel) (VB)
=======
# <a name="type-property-example-property-vb"></a>Type-Eigenschaft (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Dieses Beispiel veranschaulicht die [Type](type-property-ado.md)-Eigenschaft. Dabei handelt es sich um ein Modell eines Hilfsprogramms, mit dem die Namen und Typen einer Auflistung aufgeführt werden, wie z. B. [Properties](properties-collection-ado.md), [Fields](fields-collection-ado.md) usw.

Ein [Recordset](recordset-object-ado.md) muss nicht geöffnet werden, um auf seine **Properties** -Auflistung zugreifen zu können. Die Eigenschaften sind vorhanden, sobald das **Recordset** -Objekt instanziiert wurde. Wenn jedoch die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt wird, werden der **Properties** -Auflistung des **Recordset** -Objekts verschiedene dynamische Eigenschaften hinzugefügt, wodurch das Beispiel etwas interessanter wird. Zur besseren Veranschaulichung wird speziell die [Item](item-property-ado.md)-Eigenschaft für den Zugriff auf jedes einzelne [Property](property-object-ado.md)-Objekt verwendet.

```vb 
 
'BeginTypePropertyVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rst As ADODB.Recordset 
 Dim prop As ADODB.Property 
 ' property variables 
 Dim ix As Integer 
 Dim strMsg As String 
 
 ' create client-side recordset 
 Set rst = New ADODB.Recordset 
 rst.CursorLocation = adUseClient 
 ' enumerate property types 
 For ix = 0 To rst.Properties.Count - 1 
 Set prop = rst.Properties.Item(ix) 
 Select Case prop.Type 
 Case adBigInt 
 strMsg = "adBigInt" 
 Case adBinary 
 strMsg = "adBinary" 
 Case adBoolean 
 strMsg = "adBoolean" 
 Case adBSTR 
 strMsg = "adBSTR" 
 Case adChapter 
 strMsg = "adChapter" 
 Case adChar 
 strMsg = "adChar" 
 Case adCurrency 
 strMsg = "adCurrency" 
 Case adDate 
 strMsg = "adDate" 
 Case adDBDate 
 strMsg = "adDBDate" 
 Case adDBTime 
 strMsg = "adDBTime" 
 Case adDBTimeStamp 
 strMsg = "adDBTimeStamp" 
 Case adDecimal 
 strMsg = "adDecimal" 
 Case adDouble 
 strMsg = "adDouble" 
 Case adEmpty 
 strMsg = "adEmpty" 
 Case adError 
 strMsg = "adError" 
 Case adFileTime 
 strMsg = "adFileTime" 
 Case adGUID 
 strMsg = "adGUID" 
 Case adIDispatch 
 strMsg = "adIDispatch" 
 Case adInteger 
 strMsg = "adInteger" 
 Case adIUnknown 
 strMsg = "adIUnknown" 
 Case adLongVarBinary 
 strMsg = "adLongVarBinary" 
 Case adLongVarChar 
 strMsg = "adLongVarChar" 
 Case adLongVarWChar 
 strMsg = "adLongVarWChar" 
 Case adNumeric 
 strMsg = "adNumeric" 
 Case adPropVariant 
 strMsg = "adPropVariant" 
 Case adSingle 
 strMsg = "adSingle" 
 Case adSmallInt 
 strMsg = "adSmallInt" 
 Case adTinyInt 
 strMsg = "adTinyInt" 
 Case adUnsignedBigInt 
 strMsg = "adUnsignedBigInt" 
 Case adUnsignedInt 
 strMsg = "adUnsignedInt" 
 Case adUnsignedSmallInt 
 strMsg = "adUnsignedSmallInt" 
 Case adUnsignedTinyInt 
 strMsg = "adUnsignedTinyInt" 
 Case adUserDefined 
 strMsg = "adUserDefined" 
 Case adVarBinary 
 strMsg = "adVarBinary" 
 Case adVarChar 
 strMsg = "adVarChar" 
 Case adVariant 
 strMsg = "adVariant" 
 Case adVarNumeric 
 strMsg = "adVarNumeric" 
 Case adVarWChar 
 strMsg = "adVarWChar" 
 Case adWChar 
 strMsg = "adWChar" 
 Case Else 
 strMsg = "*UNKNOWN*" 
 End Select 
 'show results 
 Debug.Print "Property " & ix & ": " & prop.Name & _ 
 ", Type = " & strMsg 
 Next ix 
 
 ' clean up 
 Set rst = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 Set rst = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndTypePropertyVB 
```

