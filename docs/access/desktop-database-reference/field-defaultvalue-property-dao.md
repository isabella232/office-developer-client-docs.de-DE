---
title: Field.DefaultValue-Eigenschaft (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 8a1c558b-c8f6-757d-c595-4e50b9b6ae3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197092(v=office.15)
ms:contentKeyID: 48546185
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ec9469e2e3d10e9f24def7dbc15e3cecf545328d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626673"
---
# <a name="fielddefaultvalue-property-dao"></a>Field.DefaultValue-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013


Legt den Standardwert eines **[Field](field-object-dao.md)** -Objekts fest oder gibt den Wert zurück. Bei einem **Field**-Objekt, das der **[Fields](fields-collection-dao.md)** -Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Defaultvalue

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung oder der Rückgabewert ist vom Datentyp **String** und kann maximal 255 Zeichen enthalten. Es kann sich um einen Text oder einen Ausdruck handeln. Ist die Eigenschafteneinstellung ein Ausdruck, kann er benutzerdefinierte Funktionen, SQL-Aggregatfunktionen des Microsoft Access-Datenbankmoduls oder Verweise auf Abfragen, Formulare oder andere **Field**-Objekte enthalten.


> [!NOTE]
> [!HINWEIS] Sie können die **DefaultValue**-Eigenschaft eines **Field**-Objekts für ein [TableDef](tabledef-object-dao.md) -Objekt auch auf einen speziellen Wert, "GenUniqueID( )" genannt, festlegen. Dabei wird diesem Feld eine Zufallszahl zugewiesen, sobald ein neuer Datensatz hinzugefügt oder erstellt wird, wodurch jeder Datensatz einen eindeutigen Bezeichner erhält. Die [Type](field-type-property-dao.md) -Eigenschaft des Felds muss ein **Long**-Wert sein.


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
<td><p>Lesen/Schreiben</p></td>
</tr>
</tbody>
</table>


Beim Erstellen eines neuen Datensatzes wird die Einstellung der **DefaultValue**-Eigenschaft automatisch als Wert für das Feld eingegeben. Sie können den Feldwert ändern, indem Sie seine **[Value](field-value-property-dao.md)** -Eigenschaft festlegen.

Die **DefaultValue**-Eigenschaft wird nicht auf Felder vom Datentyp **AutoNumber** oder **Long Binary** angewendet.

## <a name="example"></a>Beispiel

This example uses the **DefaultValue** property to alert the user of a field's normal value while prompting for input. In addition, it demonstrates how new records will be filled using **DefaultValue** in the absence of any other input. The DefaultPrompt function is required for this procedure to run.

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
     fldTemp As Field) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
