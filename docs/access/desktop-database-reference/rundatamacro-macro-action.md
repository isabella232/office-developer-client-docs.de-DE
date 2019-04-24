---
title: RunDataMacro-Makroaktion
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306811"
---
# <a name="rundatamacro-macro-action"></a>RunDataMacro-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **AusführenDatenmakro**-Aktion können Sie ein benanntes Datenmakro ausführen.

## <a name="setting"></a>Einstellung

Die **AusführenDatenmakro**-Aktion kann mit dem folgenden Argument verwendet werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Der Name des Datenmakros, das ausgeführt werden soll.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können die **ausführendatenmakro** -Aktion in Makros, benannten datenmakros und den folgenden Makro Ereignissen verwenden: **[nach DELETE-Makro](after-delete-macro-event.md)** Ereignis, **[nach INSERT-Makro](after-insert-macro-event.md)** Ereignis und makroereignis **[nach Aktualisierung](after-update-macro-event.md)**.

Der Name des datenmakros muss die Tabelle, an die er angefügt ist, aufweisen (beispielsweise **comments. AddComment**, nicht nur **AddComment**).

Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert. Wenn das datenmakro Parameter erfordert, werden Textfelder angezeigt, in denen Sie die Argumente eingeben können.

Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie einen Parameter an ein benanntes datenmakro übergeben. Das dmGetCurrentServiceRequest-datenmakro der tblServiceRequests-Tabelle wird mithilfe der Ausführendatenmakro-Aktion aufgerufen. Wenn die dmGetCurrentServiceRequest abgeschlossen ist, wird die CurrentServiceRequest-Variable zurückgegeben Formular das datenmakro in das Textfeld txtCurrentSR geschrieben.

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
