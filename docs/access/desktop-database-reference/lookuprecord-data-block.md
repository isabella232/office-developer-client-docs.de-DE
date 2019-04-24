---
title: LookupRecord-Datenblock
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 920f0830a310452962eb5dd1c21be63215bf0f03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289791"
---
# <a name="lookuprecord-data-block"></a>LookupRecord-Datenblock

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
<td><p>Eine Zeichenfolge, die den Datensatz bezeichnet, für den eine Aktion ausgeführt werden soll. Das Argument <em>in</em> kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL-Anweisung enthalten.</p><p><strong>Hinweis</strong>: der angegebene Datensatz kann keine Daten aufnehmen, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.</p></td>
</tr>
<tr class="even">
<td><p>Bedingung</p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, mit dem der Datenumfang eingeschränkt wird, auf dem der <strong>LookupRecord</strong> -Datenblock ausgeführt wird. Kriterien sind beispielsweise oft Äquivalent zur WHERE-Klausel in einem SQL-Ausdruck ohne das Wort WHERE. Wenn Kriterien ausgelassen werden, wird der <strong>LookupRecord</strong> -Datenblock auf die gesamte Domäne angewendet, die durch das <em>in</em> -Argument angegeben wird. Jedes Feld, das in Criteria enthalten ist, muss auch ein Feld in <em>in</em>sein.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge, die einen alternativen Namen für den <em>im</em> Argument angegebenen Datensatz bereitstellt. Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden. Wenn <em>Alias</em> nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn die durch die *in* -und *Where* -Bedingungs Argumente angegebenen Kriterien mehrere Datensätze angeben, wird der **LookupRecord** -Datenblock nur für den ersten Datensatz ausgeführt.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie die SetReturnVar-Aktion verwenden, um einen Wert aus einem benannten datenmakro zurückzugeben. Ein ReturnVar mit dem Namen **CurrentServiceRequest** wird an das Makro oder die VBA-Unterroutine (Visual Basic für Applikationen) zurückgegeben, die das benannte datenmakro aufgerufen hat.

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

Das folgende Beispiel zeigt, wie Sie die Auslösenfehler-Aktion verwenden, um das makroereignis Before Change Data abzubrechen. Wenn das Feld ZugewiesenAn aktualisiert wird, wird ein LookupRecord-Datenblock verwendet, um zu bestimmen, ob der zugewiesene Techniker derzeit einer offenen Serviceanforderung zugeordnet ist. Wenn dies der Fall ist, wird das Before Change-Ereignis abgebrochen, und der Datensatz wird nicht aktualisiert.

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
