---
title: WorkflowTasks-Makroaktion
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721857"
---
# <a name="workflowtasks-macro-action"></a>WorkflowTasks-Makroaktion


**Betrifft**: Access 2013, Office 2013

Verwenden Sie die **WorkflowAufgaben** -Aktion, um das Dialogfeld **Workflowtask** zu öffnen.

## <a name="setting"></a>Einstellung

Die **WorkflowAufgaben** -Aktion hat das folgende Argument.

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
<td><p><strong>Datensatznummer</strong></p></td>
<td><p>Die Position des Elements in der Microsoft SharePoint Foundation-Liste, beginnend mit <strong>1</strong> für das erste Element in der Liste, <strong>2</strong> für das zweite Element, und so weiter. Sie können auch einen Ausdruck für dieses Argument eingeben.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

  - Die **WorkflowAufgaben** -Aktion öffnet das Dialogfeld **Workflow-Tasks**. In diesem Dialogfeld werden alle Tasks angezeigt, die für das angegebene Element zur Verfügung stehen. Ein Workflow muss für die Liste in SharePoint Foundation definiert sein.

  - Die **WorkflowAufgaben** -Aktion kann nur verwendet werden, nachdem eine verknüpfte SharePoint Foundation-Liste geöffnet und ausgewählt wurde. Wenn Sie die verknüpfte Liste öffnen und auswählen möchten, verwenden Sie die **ÖffnenTabelle** -Aktion. Falls die Liste bereits geöffnet wurde, verwenden Sie die **AuswählenObjekt** -Aktion, um sie zu auszuwählen.

  - Die **WorkflowAufgaben** -Aktion hat dieselbe Auswirkung wie das Klicken mit der rechten Maustaste auf eine beliebige Zelle in einer verknüpften SharePoint Foundation-Liste, während diese in der Datenblattansicht geöffnet ist, das Zeigen auf **Workflow** und das anschließende Klicken auf **Workflowtask**.

  - Verwenden Sie zum Ausführen der **WorkflowAufgaben** -Aktion in einem VBA-Modul die **WorkflowTasks** -Methode des **DoCmd** -Objekts.

