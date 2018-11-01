---
title: Recordset2.NoMatch Property (DAO)
TOCTitle: NoMatch Property
ms:assetid: 2d7a02ff-a2bf-5f0e-bd71-a6d42c25b13a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192114(v=office.15)
ms:contentKeyID: 48543972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbc35b696f74aa0da64ec24ce38c2f8ad8cfab4d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879091"
---
# <a name="recordset2nomatch-property-dao"></a>Recordset2.NoMatch Property (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt an, ob ein bestimmter Datensatz mithilfe der **[Seek](recordset2-seek-method-dao.md)** -Methode oder einer der **[Find](recordset2-findfirst-method-dao.md)** -Methoden gefunden wurde (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . NoMatch

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein **[Recordset](recordset-object-dao.md)** -Objekt öffnen oder erstellen, hat seine **NoMatch**-Eigenschaft den Wert **False**.

Verwenden Sie für die Suche nach einem Datensatz die **Seek** -Methode für ein **Recordset** -Objekt vom Tabellentyp oder die **Find** -Methoden für ein **Recordset** -Objekt vom Dynaset- oder Momentaufnahmentyp. Überprüfen Sie die **NoMatch** -Eigenschaftseinstellung, um festzustellen, ob der Datensatz gefunden wurde.

Wenn die Methoden **Seek** und **Find** nicht erfolgreich sind und die **NoMatch**-Eigenschaft den Wert **True** hat, ist der aktuelle Datensatz nicht mehr gültig. Rufen Sie das Lesezeichen des aktuellen Datensatzes ab, bevor Sie die **Seek**-Methode oder eine **Find**-Methode verwenden, falls Sie zu diesem Datensatz zurückkehren müssen.


> [!NOTE]
> <P>[!HINWEIS] Das Verwenden einer der <STRONG><A href="recordset-movefirst-method-dao.md">Move</A></STRONG> -Methoden für ein <STRONG>Recordset</STRONG>-Objekt hat keinen Einfluss auf die Einstellung seiner <STRONG>NoMatch</STRONG>-Eigenschaft.</P>



## <a name="example"></a>Beispiel

In diesem Beispiel wird anhand der NoMatch-Eigenschaft ermittelt, ob Seek und FindFirst erfolgreich waren. Wenn nicht, wird entsprechendes Feedback zurückgegeben. Damit dieser Vorgang ausgeführt werden kann, sind die SeekMatch- und FindMatch-Prozeduren erforderlich.

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset2, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
