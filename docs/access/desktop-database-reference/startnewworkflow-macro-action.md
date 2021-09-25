---
title: StartNewWorkflow-Makroaktion
TOCTitle: StartNewWorkflow macro action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3752d0455d51d17108475e767380d2b1f0c2ef5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589078"
---
# <a name="startnewworkflow-macro-action"></a>StartNewWorkflow-Makroaktion


**Gilt für**: Access 2013, Office 2013

Sie können die **StartenNeuerWorkflow** -Aktion verwenden, um einen neuen Workflow für ein Element in einer verknüpften Microsoft SharePoint Foundation-Liste zu starten.

## <a name="setting"></a>Einstellung

Die **StartenNeuerWorkflow**-Aktion hat das folgende Argument.

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
<td><p>Die Position des Elements in der SharePoint Foundation-Liste, beginnend mit <strong>1</strong> für das erste Element in der Liste, <strong>2</strong> für das zweite Element usw. Sie können für dieses Argument auch einen Ausdruck eingeben.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

  - Die **StartenNeuerWorkflow** -Aktion öffnet das Dialogfeld **Neuen Workflow starten**, in dem alle Workflows angezeigt werden, die für das angegebene Element zur Verfügung stehen. Ein Workflow muss für die Liste in SharePoint Foundation definiert sein, bevor Sie diese Methode verwenden können.

  - Die **StartenNeuerWorkflow** -Aktion kann nur verwendet werden, nachdem eine verknüpfte SharePoint-Liste geöffnet und ausgewählt wurde. Wenn Sie die verknüpfte Liste öffnen und auswählen möchten, verwenden Sie die **ÖffnenTabelle** -Aktion. Falls die Liste bereits geöffnet wurde, verwenden Sie die **AuswählenObjekt** -Aktion, um sie zu auszuwählen.

  - Die **StartenNeuerWorkflow** -Aktion hat dieselbe Auswirkung wie das Klicken mit der rechten Maustaste auf eine beliebige Zelle in einer verknüpften SharePoint-Liste, während diese in der Datenblattansicht geöffnet ist, das Zeigen auf **Workflow** und das anschließende Klicken auf **Neuen Workflow starten**.

  - Verwenden Sie zum Ausführen der **StartenNeuerWorkflow** -Aktion in einem VBA-Modul die **LockNavigationPane** -Methode des **DoCmd** -Objekts.

