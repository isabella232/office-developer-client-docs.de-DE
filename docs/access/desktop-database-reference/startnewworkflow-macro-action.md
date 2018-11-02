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
ms.openlocfilehash: ed3c508f4799b2ef1f9939de8ce212ab11833353
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925492"
---
# <a name="startnewworkflow-macro-action"></a>StartNewWorkflow-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **StartenNeuerWorkflow** -Aktion verwenden, um einen neuen Workflow für ein Element in einer verknüpften Microsoft SharePoint Foundation-Liste zu starten.

## <a name="setting"></a>Einstellung

Die **StartenNeuerWorkflow** -Aktion hat das folgende Argument.

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
<td><p>Die Position des Elements in der SharePoint Foundation-Liste, beginnend mit <strong>1</strong> für das erste Element in der Liste, <strong>2</strong> für das zweite Element, und so weiter. Sie können auch einen Ausdruck für dieses Argument eingeben.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

  - Die **StartenNeuerWorkflow** -Aktion öffnet das Dialogfeld **Neuen Workflow starten**, in dem alle Workflows angezeigt werden, die für das angegebene Element zur Verfügung stehen. Ein Workflow muss für die Liste in SharePoint Foundation definiert sein, bevor Sie diese Methode verwenden können.

  - Die **StartenNeuerWorkflow** -Aktion kann nur verwendet werden, nachdem eine verknüpfte SharePoint-Liste geöffnet und ausgewählt wurde. Wenn Sie die verknüpfte Liste öffnen und auswählen möchten, verwenden Sie die **ÖffnenTabelle** -Aktion. Falls die Liste bereits geöffnet wurde, verwenden Sie die **AuswählenObjekt** -Aktion, um sie zu auszuwählen.

  - Die **StartenNeuerWorkflow** -Aktion hat dieselbe Auswirkung wie das Klicken mit der rechten Maustaste auf eine beliebige Zelle in einer verknüpften SharePoint-Liste, während diese in der Datenblattansicht geöffnet ist, das Zeigen auf **Workflow** und das anschließende Klicken auf **Neuen Workflow starten**.

  - Verwenden Sie zum Ausführen der **StartenNeuerWorkflow** -Aktion in einem VBA-Modul die **LockNavigationPane** -Methode des **DoCmd** -Objekts.

