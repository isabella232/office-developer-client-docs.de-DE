---
title: DbEngine. RegisterDatabase-Methode (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 632f6e10d79d74dfef295b34a52ce62f1690101b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294225"
---
# <a name="dbengineregisterdatabase-method-dao"></a>DbEngine. RegisterDatabase-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Gibt Verbindungsinformationen für eine ODBC-Datenquelle in die Windows-Registrierung ein. Der ODBC-Treiber benötigt Verbindungsinformationen, wenn die ODBC-Datenquelle während einer Sitzung geöffnet wird.

## <a name="syntax"></a>Syntax

*Ausdruck* . RegisterDatabase (***DSN***, ***Treiber***, ***Silent***, ***Attribute***)

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DSN</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>der Name, der in <strong><a href="dbengine-opendatabase-method-dao.md"></a></strong> der OpenDatabase-Methode verwendet wird. Er verweist auf einen Block mit beschreibenden Informationen zur Datenquelle. Ist die Datenquelle beispielsweise eine ODBC-Remote-Datenquelle, könnte diese der Name des Servers sein.</p></td>
</tr>
<tr class="even">
<td><p><em>Driver</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Name des ODBC-Treibers. Er entspricht nicht dem Namen der DLL-Datei des ODBC-Treibers.</p></td>
</tr>
<tr class="odd">
<td><p><em>Automatische</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p><strong>True</strong> , wenn Sie nicht möchten, dass die Dialogfelder ODBC-Treiber angezeigt werden, die für treiberspezifische Informationen aufgefordert werden; oder <strong>false</strong> , wenn die Dialogfelder ODBC-Treiber angezeigt werden sollen. Wenn Silent auf <strong>true</strong>festgelegt ist, müssen Attribute alle erforderlichen treiberspezifischen Informationen enthalten, oder die Dialogfelder werden trotzdem angezeigt.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Eine Liste der Schlüsselwörter, die zur Windows-Registrierung hinzugefügt werden sollen. Die Schlüsselwörter sind in Zeichenfolgen enthalten, die durch Wagenrücklaufzeichen getrennt sind.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Ist die Datenbank beim Verwenden der **RegisterDatabase**-Methode bereits in der Windows-Registrierung registriert (Verbindungsinformationen wurden eingegeben), werden die Verbindungsinformationen aktualisiert.

Wenn die **RegisterDatabase**-Methode fehlschlägt, werden keine Änderungen in der Windows-Registrierung vorgenommen, und es tritt ein Fehler auf.

Weitere Informationen zu ODBC-Treibern wie SQL Server finden Sie in der vom Treiber bereitgestellten Hilfedatei.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **RegisterDatabase**-Methode verwendet, um eine Microsoft SQL Server-Datenquelle namens Publishers in der Windows-Registrierung zu erfassen.

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

