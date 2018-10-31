---
title: Field.DefaultValue Property (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 8a1c558b-c8f6-757d-c595-4e50b9b6ae3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197092(v=office.15)
ms:contentKeyID: 48546185
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d23e088ca93474ac928875730580a693abe9648c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862226"
---
# <a name="fielddefaultvalue-property-dao"></a>Field.DefaultValue Property (DAO)


**Betrifft**: Access 2013 | Office 2013


Legt den Standardwert eines **[Field](field-object-dao.md)** -Objekts fest oder gibt den Wert zurück. Bei einem **Field**-Objekt, das der **[Fields](fields-collection-dao.md)** -Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . DefaultValue

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

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
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
</tbody>
</table>


Beim Erstellen eines neuen Datensatzes wird die Einstellung der **DefaultValue**-Eigenschaft automatisch als Wert für das Feld eingegeben. Sie können den Feldwert ändern, indem Sie seine **[Value](field-value-property-dao.md)** -Eigenschaft festlegen.

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
