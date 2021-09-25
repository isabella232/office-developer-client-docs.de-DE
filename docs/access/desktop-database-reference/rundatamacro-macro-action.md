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
ms.localizationpriority: medium
ms.openlocfilehash: d24cf33bd9b5ced31ec7a71ce67efc70b26b5e02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557792"
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


## <a name="remarks"></a>HinwBemerkungeneise

Sie können die **Aktion "RunDataMacro"** in Makros, benannten Datenmakros und den folgenden Makroereignissen verwenden: **[Makroereignis "Nach Löschvorgang",](after-delete-macro-event.md)** **[Makroereignis "Nach Einfügen"](after-insert-macro-event.md)** und **[Makroereignis "Nach Aktualisierung".](after-update-macro-event.md)**

Der Name des Datenmakros muss die Tabelle enthalten, der es angefügt ist (z. **B. Comments.AddComment**, nicht nur **AddComment**).

Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert. Wenn für das Datenmakro Parameter erforderlich sind, werden Textfelder angezeigt, in die Sie die Argumente eingeben können.

Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie einen Parameter an ein benanntes Datenmakro übergeben. Das dmGetCurrentServiceRequest-Datenmakro der tblServiceRequests-Tabelle wird mithilfe der RunDataMacro-Aktion aufgerufen. Wenn dmGetCurrentServiceRequest abgeschlossen ist, wird die CurrentServiceRequest-Variable zurückgegeben, aus der das Datenmakro in das Textfeld txtCurrentSR geschrieben wird.

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
