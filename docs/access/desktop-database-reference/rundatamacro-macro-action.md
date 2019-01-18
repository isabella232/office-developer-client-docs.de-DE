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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709978"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="52fbf-102">RunDataMacro-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="52fbf-102">RunDataMacro macro action</span></span>

<span data-ttu-id="52fbf-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52fbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52fbf-104">Mit der **AusführenDatenmakro** -Aktion können Sie ein benanntes Datenmakro ausführen.</span><span class="sxs-lookup"><span data-stu-id="52fbf-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="52fbf-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="52fbf-105">Setting</span></span>

<span data-ttu-id="52fbf-106">Die **AusführenDatenmakro** -Aktion kann mit dem folgenden Argument verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52fbf-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52fbf-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="52fbf-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="52fbf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52fbf-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52fbf-109">Name</span><span class="sxs-lookup"><span data-stu-id="52fbf-109">Name</span></span></p></td>
<td><p><span data-ttu-id="52fbf-110">Der Name des Datenmakros, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="52fbf-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="52fbf-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52fbf-111">Remarks</span></span>

<span data-ttu-id="52fbf-112">Sie können die **AusführenDatenmakro** -Aktion in Makros, benannten Datenmakros und den folgenden makroereignissen verwenden: **[makroereignis nach Löschvorgang](after-delete-macro-event.md)**, **[Makro-Ereignis nach Eingabe](after-insert-macro-event.md)** und **[Makro-Ereignis nach Aktualisierung](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="52fbf-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete macro event](after-delete-macro-event.md)**, **[After Insert macro event](after-insert-macro-event.md)** and **[After Update macro event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="52fbf-113">Der Name des Datenmakros muss die Tabelle enthalten, mit der sie (beispielsweise **Comments.AddComment**, nicht nur **AddComment**) verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="52fbf-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="52fbf-114">Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert.</span><span class="sxs-lookup"><span data-stu-id="52fbf-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="52fbf-115">Wenn das Datenmakro Parameter erfordert, erscheinen Textfelder, in dem Sie die Argumente eingeben können.</span><span class="sxs-lookup"><span data-stu-id="52fbf-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="52fbf-p102">Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="52fbf-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="52fbf-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52fbf-118">Example</span></span>

<span data-ttu-id="52fbf-119">Im folgenden Beispiel wird veranschaulicht, wie einen Parameter an ein benanntes Datenmakro übergeben.</span><span class="sxs-lookup"><span data-stu-id="52fbf-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="52fbf-120">Das Datenmakro DmGetCurrentServiceRequest der Tabelle TblServiceRequests wird aufgerufen, mit der AusführenDatenmakro-Aktion.</span><span class="sxs-lookup"><span data-stu-id="52fbf-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="52fbf-121">Nach Abschluss der DmGetCurrentServiceRequest zurückgegeben, die Variable CurrentServiceRequest Formular, das das Datenmakro in das Textfeld TxtCurrentSR geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="52fbf-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="52fbf-122">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="52fbf-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
