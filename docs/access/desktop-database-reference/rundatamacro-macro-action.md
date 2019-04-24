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
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="8607a-102">RunDataMacro-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="8607a-102">RunDataMacro macro action</span></span>

<span data-ttu-id="8607a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8607a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8607a-104">Mit der **AusführenDatenmakro**-Aktion können Sie ein benanntes Datenmakro ausführen.</span><span class="sxs-lookup"><span data-stu-id="8607a-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="8607a-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="8607a-105">Setting</span></span>

<span data-ttu-id="8607a-106">Die **AusführenDatenmakro**-Aktion kann mit dem folgenden Argument verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8607a-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8607a-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="8607a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8607a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8607a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8607a-109">Name</span><span class="sxs-lookup"><span data-stu-id="8607a-109">Name</span></span></p></td>
<td><p><span data-ttu-id="8607a-110">Der Name des Datenmakros, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8607a-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8607a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8607a-111">Remarks</span></span>

<span data-ttu-id="8607a-112">Sie können die **ausführendatenmakro** -Aktion in Makros, benannten datenmakros und den folgenden Makro Ereignissen verwenden: **[nach DELETE-Makro](after-delete-macro-event.md)** Ereignis, **[nach INSERT-Makro](after-insert-macro-event.md)** Ereignis und makroereignis **[nach Aktualisierung](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="8607a-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete macro event](after-delete-macro-event.md)**, **[After Insert macro event](after-insert-macro-event.md)** and **[After Update macro event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="8607a-113">Der Name des datenmakros muss die Tabelle, an die er angefügt ist, aufweisen (beispielsweise **comments. AddComment**, nicht nur **AddComment**).</span><span class="sxs-lookup"><span data-stu-id="8607a-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="8607a-114">Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert.</span><span class="sxs-lookup"><span data-stu-id="8607a-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="8607a-115">Wenn das datenmakro Parameter erfordert, werden Textfelder angezeigt, in denen Sie die Argumente eingeben können.</span><span class="sxs-lookup"><span data-stu-id="8607a-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="8607a-p102">Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8607a-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="8607a-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8607a-118">Example</span></span>

<span data-ttu-id="8607a-119">Das folgende Beispiel zeigt, wie Sie einen Parameter an ein benanntes datenmakro übergeben.</span><span class="sxs-lookup"><span data-stu-id="8607a-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="8607a-120">Das dmGetCurrentServiceRequest-datenmakro der tblServiceRequests-Tabelle wird mithilfe der Ausführendatenmakro-Aktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8607a-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="8607a-121">Wenn die dmGetCurrentServiceRequest abgeschlossen ist, wird die CurrentServiceRequest-Variable zurückgegeben Formular das datenmakro in das Textfeld txtCurrentSR geschrieben.</span><span class="sxs-lookup"><span data-stu-id="8607a-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="8607a-122">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="8607a-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
