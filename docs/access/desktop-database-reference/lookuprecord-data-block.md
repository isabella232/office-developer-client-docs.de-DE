---
title: NachschlagenDatensatz-Datenblock
TOCTitle: LookupRecord Data Block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bd9a687d7f74b99dc20ee079f970c37ba627f31
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877688"
---
# <a name="lookuprecord-data-block"></a>NachschlagenDatensatz-Datenblock

**Betrifft**: Access 2013, Office 2013

Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.

> [!NOTE]
> [!HINWEIS] Der **NachschlagenDatensatz** -Datenblock ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **NachschlagenDatensatz** -Aktion kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Eingabe erforderlich</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>In</p></td>
<td><p>Ja</p></td>
<td><p>Eine Zeichenfolge, die den Datensatz für den Betrieb identifiziert. Das <em>im</em> Argument kann der Name der Tabelle, einer select-Abfrage oder eine SQL-Anweisung enthalten.</p>

> [!NOTE]
> Der angegebene Datensatz darf keine Daten enthalten, die in einer verknüpften Tabelle oder einer ODBC-Datenquelle gespeichert sind.


<p></p></td>
</tr>
<tr class="even">
<td><p>Bedingung</p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, der zum Einschränken des Bereichs der Daten auf dem des <strong>NachschlagenDatensatz</strong> -Datenblocks wird ausgeführt. Häufig sind beispielsweise Kriterien entspricht der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort, in dem. Wenn Kriterien Length angegeben werden, wirkt sich auf die gesamte Domäne, die durch das Argument <em>im</em> angegebenen <strong>NachschlagenDatensatz</strong> -Datenblock. Jedes Feld, das im Argument Kriterien enthalten ist, muss auch ein Feld in <em>In</em>sein.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge, die einen alternativen Namen für den durch das Argument <em>im</em> angegebenen Datensatz enthält. Häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu verhindern, dass mögliche mehrdeutige Verweise zu verkürzen. Wenn <em>Alias</em> nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Wenn die durch die Argumente *In* und *Bedingung* angegebenen Kriterien mehrere Datensätze angegeben ist, wird das **NachschlagenDatensatz** -Datenblock nur für den ersten Datensatz ausgeführt.

## <a name="example"></a>Beispiel

Das folgende Beispiel veranschaulicht die SetReturnVar-Aktion verwenden, um einen Wert aus ein benanntes Datenmakro zurückzugeben. Eine mit dem Namen **CurrentServiceRequest** ReturnVar wird an das Makro oder Visual Basic für Applikationen (VBA) Unterroutine zurückgegeben, die das benanntes Datenmakro aufgerufen.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

Das folgende Beispiel veranschaulicht die Auslösenfehler-Aktion verwenden, um das Ereignis vor Änderung Daten Makro abzubrechen. Wenn das Feld AssignedTo aktualisiert wird, wird mit einem NachschlagenDatensatz-Datenblock verwendet, um festzustellen, ob der zugewiesene Techniker eine open Service-Anforderung derzeit zugewiesen ist. Wenn dies der Fall ist, wird das Ereignis vor Änderung abgebrochen, und der Datensatz nicht aktualisiert.

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
