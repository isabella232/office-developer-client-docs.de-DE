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
# <a name="workflowtasks-macro-action"></a><span data-ttu-id="20d96-102">WorkflowTasks-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="20d96-102">WorkflowTasks macro action</span></span>


<span data-ttu-id="20d96-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20d96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20d96-104">Verwenden Sie die **WorkflowAufgaben** -Aktion, um das Dialogfeld **Workflowtask** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="20d96-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="20d96-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="20d96-105">Setting</span></span>

<span data-ttu-id="20d96-106">Die **WorkflowAufgaben** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="20d96-106">The **WorkflowTasks** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20d96-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="20d96-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="20d96-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20d96-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20d96-109"><strong>Datensatznummer</strong></span><span class="sxs-lookup"><span data-stu-id="20d96-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="20d96-110">Die Position des Elements in der Microsoft SharePoint Foundation-Liste, beginnend mit <strong>1</strong> für das erste Element in der Liste, <strong>2</strong> für das zweite Element, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="20d96-110">The position of the item in the Microsoft SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="20d96-111">Sie können auch einen Ausdruck für dieses Argument eingeben.</span><span class="sxs-lookup"><span data-stu-id="20d96-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="20d96-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20d96-112">Remarks</span></span>

  - <span data-ttu-id="20d96-p102">Die **WorkflowAufgaben** -Aktion öffnet das Dialogfeld **Workflow-Tasks**. In diesem Dialogfeld werden alle Tasks angezeigt, die für das angegebene Element zur Verfügung stehen. Ein Workflow muss für die Liste in SharePoint Foundation definiert sein.</span><span class="sxs-lookup"><span data-stu-id="20d96-p102">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box. This dialog box displays all tasks that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation.</span></span>

  - <span data-ttu-id="20d96-p103">Die **WorkflowAufgaben** -Aktion kann nur verwendet werden, nachdem eine verknüpfte SharePoint Foundation-Liste geöffnet und ausgewählt wurde. Wenn Sie die verknüpfte Liste öffnen und auswählen möchten, verwenden Sie die **ÖffnenTabelle** -Aktion. Falls die Liste bereits geöffnet wurde, verwenden Sie die **AuswählenObjekt** -Aktion, um sie zu auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="20d96-p103">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="20d96-119">Die **WorkflowAufgaben** -Aktion hat dieselbe Auswirkung wie das Klicken mit der rechten Maustaste auf eine beliebige Zelle in einer verknüpften SharePoint Foundation-Liste, während diese in der Datenblattansicht geöffnet ist, das Zeigen auf **Workflow** und das anschließende Klicken auf **Workflowtask**.</span><span class="sxs-lookup"><span data-stu-id="20d96-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span></span>

  - <span data-ttu-id="20d96-120">Verwenden Sie zum Ausführen der **WorkflowAufgaben** -Aktion in einem VBA-Modul die **WorkflowTasks** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="20d96-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span></span>

