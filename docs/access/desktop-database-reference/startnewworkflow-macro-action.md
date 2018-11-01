---
title: StartenNeuerWorkflow-Makroaktion
TOCTitle: StartNewWorkflow Macro Action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6ba9d38caaa85ab9dd582abdbeb37aff5c7b340e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886494"
---
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="72058-102">StartenNeuerWorkflow-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="72058-102">StartNewWorkflow Macro Action</span></span>


<span data-ttu-id="72058-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72058-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72058-104">Sie können die **StartenNeuerWorkflow** -Aktion verwenden, um einen neuen Workflow für ein Element in einer verknüpften Microsoft SharePoint Foundation-Liste zu starten.</span><span class="sxs-lookup"><span data-stu-id="72058-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="72058-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="72058-105">Setting</span></span>

<span data-ttu-id="72058-106">Die **StartenNeuerWorkflow** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="72058-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72058-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="72058-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="72058-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72058-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72058-109"><strong>Datensatznummer</strong></span><span class="sxs-lookup"><span data-stu-id="72058-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="72058-110">Die Position des Elements in der SharePoint Foundation-Liste, beginnend mit <strong>1</strong> für das erste Element in der Liste, <strong>2</strong> für das zweite Element, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="72058-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="72058-111">Sie können auch einen Ausdruck für dieses Argument eingeben.</span><span class="sxs-lookup"><span data-stu-id="72058-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="72058-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72058-112">Remarks</span></span>

  - <span data-ttu-id="72058-p102">Die **StartenNeuerWorkflow** -Aktion öffnet das Dialogfeld **Neuen Workflow starten**, in dem alle Workflows angezeigt werden, die für das angegebene Element zur Verfügung stehen. Ein Workflow muss für die Liste in SharePoint Foundation definiert sein, bevor Sie diese Methode verwenden können.</span><span class="sxs-lookup"><span data-stu-id="72058-p102">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box. This dialog box displays all workflows that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="72058-p103">Die **StartenNeuerWorkflow** -Aktion kann nur verwendet werden, nachdem eine verknüpfte SharePoint-Liste geöffnet und ausgewählt wurde. Wenn Sie die verknüpfte Liste öffnen und auswählen möchten, verwenden Sie die **ÖffnenTabelle** -Aktion. Falls die Liste bereits geöffnet wurde, verwenden Sie die **AuswählenObjekt** -Aktion, um sie zu auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="72058-p103">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="72058-119">Die **StartenNeuerWorkflow** -Aktion hat dieselbe Auswirkung wie das Klicken mit der rechten Maustaste auf eine beliebige Zelle in einer verknüpften SharePoint-Liste, während diese in der Datenblattansicht geöffnet ist, das Zeigen auf **Workflow** und das anschließende Klicken auf **Neuen Workflow starten**.</span><span class="sxs-lookup"><span data-stu-id="72058-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="72058-120">Verwenden Sie zum Ausführen der **StartenNeuerWorkflow** -Aktion in einem VBA-Modul die **LockNavigationPane** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="72058-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

