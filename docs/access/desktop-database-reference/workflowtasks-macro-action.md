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
ms.localizationpriority: medium
ms.openlocfilehash: 97c5c3bd337785e4222655538310a194ee45e8cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593284"
---
# <a name="workflowtasks-macro-action"></a>WorkflowTasks-Makroaktion


**Gilt für**: Access 2013, Office 2013

Verwenden Sie die **WorkflowAufgaben**-Aktion, um das Dialogfeld **Workflowtask** zu öffnen.

## <a name="setting"></a>Einstellung

Die **WorkflowAufgaben**-Aktion hat das folgende Argument.

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
<td><p>Die Position des Elements in der Microsoft SharePoint Foundation-Liste, beginnend mit <strong>1</strong> für das erste Element in der Liste, <strong>2</strong> für das zweite Element usw. Sie können für dieses Argument auch einen Ausdruck eingeben.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

  - Die **WorkflowAufgaben** -Aktion öffnet das Dialogfeld **Workflow-Tasks**. In diesem Dialogfeld werden alle Tasks angezeigt, die für das angegebene Element zur Verfügung stehen. Ein Workflow muss für die Liste in SharePoint Foundation definiert sein.

  - Die **WorkflowAufgaben** -Aktion kann nur verwendet werden, nachdem eine verknüpfte SharePoint Foundation-Liste geöffnet und ausgewählt wurde. Wenn Sie die verknüpfte Liste öffnen und auswählen möchten, verwenden Sie die **ÖffnenTabelle** -Aktion. Falls die Liste bereits geöffnet wurde, verwenden Sie die **AuswählenObjekt** -Aktion, um sie zu auszuwählen.

  - Die **WorkflowAufgaben** -Aktion hat dieselbe Auswirkung wie das Klicken mit der rechten Maustaste auf eine beliebige Zelle in einer verknüpften SharePoint Foundation-Liste, während diese in der Datenblattansicht geöffnet ist, das Zeigen auf **Workflow** und das anschließende Klicken auf **Workflowtask**.

  - Verwenden Sie zum Ausführen der **WorkflowAufgaben** -Aktion in einem VBA-Modul die **WorkflowTasks** -Methode des **DoCmd** -Objekts.

