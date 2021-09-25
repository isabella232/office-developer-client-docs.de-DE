---
title: RaiseError-Makroaktion
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7bfeae06c337dd8770e0d724e1b53f3be6ccf0cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615200"
---
# <a name="raiseerror-macro-action"></a>RaiseError-Makroaktion

**Gilt für**: Access 2013, Office 2013 

Mit der **AuslösenFehler** -Aktion wird eine Ausnahme ausgelöst, die von der **[BeiFehler](onerror-macro-action.md)** -Makroaktion behandelt werden kann.

> [!NOTE]
> [!HINWEIS] Die **AuslösenFehler** -Aktion ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **AuslösenFehler**-Aktion kann mit den folgenden Argumenten verwendet werden.

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
<td><p>Fehlernummer</p></td>
<td><p>Ja</p></td>
<td><p>Eine Zahl oder ein Ausdruck, die bzw. der zu einem Long-Datentyp aufgelöst wird.</p></td>
</tr>
<tr class="even">
<td><p>Fehlerbeschreibung</p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, der den Fehler beschreibt.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Bei einem Aufruf der **AuslösenFehler** -Aktion in einem Makroereignis des Typs **[Vor Änderung](before-change-macro-event.md)** oder **[Vor Löschung](before-delete-macro-event.md)** wird das Ereignis abgebrochen.

Wenn keine aktive **BeiFehler** -Anweisung zur Fehlerbehandlung vorhanden ist, wird der von der **AuslösenFehler** -Aktion ausgelöste Fehler der **USysApplicationLog** -Systemtabelle hinzugefügt. Wenn die **AuslösenFehler** -Aktion in der **USysApplicationLog** -Tabelle schreibt, wird die **Kategorie** -Spalte automatisch auf **Ausführung** festgelegt.

Zum Anzeigen der **USysApplicationLog** -Tabelle gehen Sie wie folgt vor:

1.  Klicken Sie auf das Menü **"Datei",** und klicken Sie dann auf **"Optionen".**

2.  Klicken Sie im Dialogfeld **Access-Optionen** auf die Registerkarte **Aktuelle Datenbank**.

3.  Klicken Sie im Bereich **Navigation** auf **Navigationsoptionen**.

4.  Klicken Sie im Dialogfeld **Navigationsoptionen** auf **Systemobjekte anzeigen** und dann auf **OK**.

5.  Klicken Sie auf **OK**, um das Dialogfeld **Access-Optionen** zu schließen.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie die RaiseError-Aktion verwendet wird, um das Makroereignis "Vor Änderung" abzubrechen. Wenn das Feld AssignedTo aktualisiert wird, wird ein Nachschlagedatenblock verwendet, um zu bestimmen, ob der zugewiesene Techniker derzeit einer geöffneten Serviceanfrage zugewiesen ist. Wenn dies der Fall ist, wird das Before Change-Ereignis abgebrochen, und der Datensatz wird nicht aktualisiert.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
