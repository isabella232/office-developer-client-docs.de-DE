---
title: AusführenDatenmakro-Makroaktion
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6777ae05d2ab7455016df834d17abb3406a2d710
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889924"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="02aae-102">AusführenDatenmakro-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="02aae-102">RunDataMacro Macro Action</span></span>

<span data-ttu-id="02aae-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02aae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02aae-104">Mit der **AusführenDatenmakro** -Aktion können Sie ein benanntes Datenmakro ausführen.</span><span class="sxs-lookup"><span data-stu-id="02aae-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="02aae-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="02aae-105">Setting</span></span>

<span data-ttu-id="02aae-106">Die **AusführenDatenmakro** -Aktion kann mit dem folgenden Argument verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02aae-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02aae-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="02aae-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="02aae-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02aae-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02aae-109">Name</span><span class="sxs-lookup"><span data-stu-id="02aae-109">Name</span></span></p></td>
<td><p><span data-ttu-id="02aae-110">Der Name des Datenmakros, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="02aae-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="02aae-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02aae-111">Remarks</span></span>

<span data-ttu-id="02aae-112">Die **AusführenDatenmakro** -Aktion können Sie in Makros, benannten Datenmakros und den folgenden Makroereignissen verwenden: **[Makroereignis "Nach Löschvorgang"](after-delete-macro-event.md)**, **[Makroereignis "Nach Eingabe"](after-insert-macro-event.md)** und **[Makroereignis "Nach Aktualisierung"](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="02aae-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete Macro Event](after-delete-macro-event.md)**, **[After Insert Macro Event](after-insert-macro-event.md)** and **[After Update Macro Event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="02aae-113">Der Name des Datenmakros muss die Tabelle enthalten, mit der sie (beispielsweise **Comments.AddComment**, nicht nur **AddComment**) verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="02aae-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="02aae-114">Wenn Sie das auszuführende Datenmakro im Makro-Designer auswählen, wird von Access ermittelt, ob das Datenmakro Parameter erfordert.</span><span class="sxs-lookup"><span data-stu-id="02aae-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="02aae-115">Wenn das Datenmakro Parameter erfordert, erscheinen Textfelder, in dem Sie die Argumente eingeben können.</span><span class="sxs-lookup"><span data-stu-id="02aae-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="02aae-p102">Wenn Sie ein Makro ausführen, das die **AusführenDatenmakro** -Aktion enthält, und dieses die **AusführenDatenmakro** -Aktion erreicht, wird das aufgerufene Datenmakro in Access ausgeführt. Sobald das aufgerufene Datenmakro beendet wurde, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="02aae-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="02aae-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="02aae-118">Example</span></span>

<span data-ttu-id="02aae-119">Im folgenden Beispiel wird veranschaulicht, wie einen Parameter an ein benanntes Datenmakro übergeben.</span><span class="sxs-lookup"><span data-stu-id="02aae-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="02aae-120">Das Datenmakro DmGetCurrentServiceRequest der Tabelle TblServiceRequests wird aufgerufen, mit der AusführenDatenmakro-Aktion.</span><span class="sxs-lookup"><span data-stu-id="02aae-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="02aae-121">Nach Abschluss der DmGetCurrentServiceRequest zurückgegeben, die Variable CurrentServiceRequest Formular, das das Datenmakro in das Textfeld TxtCurrentSR geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="02aae-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="02aae-122">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="02aae-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
