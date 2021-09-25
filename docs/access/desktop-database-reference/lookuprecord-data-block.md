---
title: NachschlagenDatensatz-Datenblock
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9ce133ef046ab5093f717c4512b647843ff8dbe9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602248"
---
# <a name="lookuprecord-data-block"></a>NachschlagenDatensatz-Datenblock

**Gilt für**: Access 2013, Office 2013

Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.

> [!NOTE]
> Der **NachschlagenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **NachschlagenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Erforderlich</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>In</p></td>
<td><p>Ja</p></td>
<td><p>Eine Zeichenfolge, die den Datensatz bezeichnet, für den eine Aktion ausgeführt werden soll. Das Argument <em>"In"</em> kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL Anweisung enthalten.</p><p><strong>HINWEIS:</strong>Der angegebene Datensatz kann keine Daten enthalten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.</p></td>
</tr>
<tr class="even">
<td><p>Bedingung</p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, der zum Einschränken des Datenbereichs verwendet wird, für den der <strong>Nachschlagedatenblock</strong> ausgeführt wird. Kriterien entsprechen beispielsweise häufig der WHERE-Klausel in einem SQL Ausdruck, ohne das Wort WHERE. Wenn Kriterien nicht angegeben werden, wird der <strong>Datenblock "LookupRecord"</strong> für die gesamte durch das Argument <em>"In"</em> angegebene Domäne ausgeführt. Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in <em>In</em>sein.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge, die einen alternativen Namen für den durch das <em>Argument "In"</em> angegebenen Datensatz bereitstellt. Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden. Wenn <em>Alias</em> nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Wenn die durch die Argumente *"In"* und *"Where Condition"* angegebenen Kriterien mehr als einen Datensatz zurückgeben, wird der **Datenblock "LookupRecord"** nur für den ersten Datensatz ausgeführt.  Für den Fall, dass keine Datensätze mit den angegebenen Kriterien übereinstimmen, überspringt Access den Im **LookupRecord-Block** enthaltenen Aktionssatz, als ob es sich um einen If-Makroblockausdruck handeln würde, der als "false" ausgewertet wurde. **[](if-then-else-macro-block.md)**

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie die SetReturnVar-Aktion verwenden, um einen Wert aus einem benannten Datenmakro zurückzugeben. Ein ReturnVar mit dem Namen **CurrentServiceRequest** wird an das Makro oder die Visual Basic for Applications (VBA)-Unterroutine zurückgegeben, die das benannte Datenmakro aufgerufen hat.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```

<br/>

Das folgende Beispiel zeigt, wie die RaiseError-Aktion verwendet wird, um das Makroereignis "Vor Änderung" abzubrechen. Wenn das Feld AssignedTo aktualisiert wird, wird ein Nachschlagedatenblock verwendet, um zu bestimmen, ob der zugewiesene Techniker derzeit einer geöffneten Serviceanfrage zugewiesen ist. Wenn dies der Fall ist, wird das Before Change-Ereignis abgebrochen, und der Datensatz wird nicht aktualisiert.

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
