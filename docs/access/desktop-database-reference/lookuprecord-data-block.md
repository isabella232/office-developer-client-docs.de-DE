---
title: Nachschlagendatensatz-Datenblock
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734210"
---
# <a name="lookuprecord-data-block"></a>Nachschlagendatensatz-Datenblock

**Gilt für**: Access 2013, Office 2013

Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.

> [!NOTE]
> Der **NachschlagenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Setting

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
<td><p>Eine Zeichenfolge, die den Datensatz bezeichnet, für den eine Aktion ausgeführt werden soll. Das <em>in</em> -Argument kann den Namen der Tabelle, eine SELECT-Abfrage oder eine SQL-Anweisung enthalten.</p><p><strong>Hinweis</strong>: der angegebene Datensatz darf keine Daten enthalten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.</p></td>
</tr>
<tr class="even">
<td><p>Bedingung</p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, der verwendet wird, um den Datenbereich einzuschränken, für den der <strong>nachschlagendatensatz</strong> -Datenblock ausgeführt wird. Beispielsweise entsprechen Kriterien häufig der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort WHERE. Wenn Kriterien ausgelassen werden, funktioniert der <strong>nachschlagendatensatz</strong> -Datenblock für die gesamte Domäne, die durch das Argument <em>in</em> angegeben wird. Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in <em>in</em>sein.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge, die einen alternativen Namen für den durch das <em>in</em> -Argument angegebenen Datensatz bereitstellt. Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden. Wenn <em>Alias</em> nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn die durch die Argumente *in* und *WHERE Bedingung* angegebenen Kriterien mehr als einen Datensatz zurückgeben, wird der **nachschlagendatensatz** -Datenblock nur für den ersten Datensatz ausgeführt.  Wenn keine Datensätze mit den angegebenen Kriterien übereinstimmen, springt Access über die Gruppe von Aktionen, die im **nachschlagendatensatz** -Block enthalten sind, als ob es sich um einen **[if](if-then-else-macro-block.md)** -Makroblock Ausdruck handelt, der als false ausgewertet wird.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird gezeigt, wie Sie mit der SetReturnVar-Aktion einen Wert aus einem benannten datenmakro zurückgeben. Ein ReturnVar mit dem Namen **CurrentServiceRequest** wird an das Makro oder Visual Basic for Applications (VBA) Unterroutine zurückgegeben, die das benannte datenmakro aufgerufen hat.

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

Im folgenden Beispiel wird gezeigt, wie Sie mit der auslösenfehler-Aktion das makroereignis vor Änderungsdaten abbrechen. Wenn das Feld AssignedTo aktualisiert wird, wird ein nachschlagendatensatz-Datenblock verwendet, um zu bestimmen, ob der zugewiesene Techniker derzeit einer offenen Dienstanforderung zugewiesen ist. Wenn dies der Fall ist, wird das Before Change-Ereignis abgebrochen, und der Datensatz wird nicht aktualisiert.

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
