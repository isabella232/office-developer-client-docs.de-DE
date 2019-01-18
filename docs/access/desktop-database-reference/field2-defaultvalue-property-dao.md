---
title: Field2.DefaultValue-Eigenschaft (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845a2e0c7ffa5d54d73c4fcec1a6c785468d734e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717342"
---
# <a name="field2defaultvalue-property-dao"></a>Field2.DefaultValue-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Legt den Standardwert eines **Field2**-Objekts fest oder gibt den Wert zurück. Bei einem **Field2**-Objekt, das der **[Fields](fields-collection-dao.md)** -Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . DefaultValue

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung oder der Rückgabewert ist vom Datentyp **String** und kann maximal 255 Zeichen enthalten. Es kann sich um einen Text oder einen Ausdruck handeln. Ist die Eigenschafteneinstellung ein Ausdruck, kann er benutzerdefinierte Funktionen, SQL-Aggregatfunktionen des Microsoft Access-Datenbankmoduls oder Verweise auf Abfragen, Formulare oder andere **Field2**-Objekte enthalten.

> [!NOTE]
> [!HINWEIS] Sie können die **DefaultValue**-Eigenschaft eines **Field2**-Objekts für ein **TableDef**-Objekt auch auf einen speziellen Wert, "GenUniqueID( )" genannt, festlegen. Dabei wird diesem Feld eine Zufallszahl zugewiesen, sobald ein neuer Datensatz hinzugefügt oder erstellt wird, wodurch jeder Datensatz einen eindeutigen Bezeichner erhält. Die **Type**-Eigenschaft des Felds muss ein **Long**-Wert sein.

Die Verfügbarkeit der **DefaultValue**-Eigenschaft hängt vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist (siehe folgende Tabelle).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit der Fields-Auflistung</p></th>
<th><p>Verfügbarkeit von DefaultValue</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Index-Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p>QueryDef-Objekt</p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="odd">
<td><p>Recordset-Objekt</p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p>Relation-Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p>TableDef-Objekt</p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
</tbody>
</table>


Beim Erstellen eines neuen Datensatzes wird die Einstellung der **DefaultValue**-Eigenschaft automatisch als Wert für das Feld eingegeben. Sie können den Feldwert ändern, indem Sie seine **Value**-Eigenschaft festlegen.

Die **DefaultValue**-Eigenschaft wird nicht auf Felder vom Datentyp **AutoNumber** oder **Long Binary** angewendet.

## <a name="example"></a>Beispiel

Dieses Beispiel verwendet die DefaultValue-Eigenschaft, um den Benutzer auf den üblichen Wert eines Felds hinzuweisen und ihn zur Eingabe eines Werts aufzufordern. Es zeigt außerdem, wie neue Datensätze bei fehlender Eingabe mithilfe der DefaultValue-Eigenschaft gefüllt werden. Zum Ausführen dieser Prozedur ist die DefaultPrompt-Funktion erforderlich.

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
