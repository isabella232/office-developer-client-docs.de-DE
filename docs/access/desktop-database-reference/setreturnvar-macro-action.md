---
title: SetReturnVar-Makroaktion
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308673"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="bad8c-102">SetReturnVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="bad8c-102">SetReturnVar macro action</span></span>

<span data-ttu-id="bad8c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bad8c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bad8c-104">Mit der **SetReturnVar** -Aktion wird eine Rückgabevariable erstellt und auf einen bestimmten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bad8c-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="bad8c-105">Die **SetReturnVar** -Aktion ist nur in datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bad8c-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="bad8c-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="bad8c-106">Setting</span></span>

<span data-ttu-id="bad8c-107">Die **SetReturnVar** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="bad8c-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bad8c-108">Argument</span><span class="sxs-lookup"><span data-stu-id="bad8c-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="bad8c-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="bad8c-109">Required</span></span></p></th>
<th><p><span data-ttu-id="bad8c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bad8c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bad8c-111">Name</span><span class="sxs-lookup"><span data-stu-id="bad8c-111">Name</span></span></p></td>
<td><p><span data-ttu-id="bad8c-112">Ja</span><span class="sxs-lookup"><span data-stu-id="bad8c-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="bad8c-113">Eine Zeichenfolge, die den Namen der Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="bad8c-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bad8c-114">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="bad8c-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="bad8c-115">Ja</span><span class="sxs-lookup"><span data-stu-id="bad8c-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="bad8c-116">Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bad8c-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="bad8c-117">Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran.</span><span class="sxs-lookup"><span data-stu-id="bad8c-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="bad8c-118">Sie können auf die <strong>Generator</strong> -Schaltfläche klicken, um den <strong>Ausdrucks-Generator</strong> zum Festlegen dieses Arguments zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bad8c-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bad8c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bad8c-119">Remarks</span></span>

<span data-ttu-id="bad8c-120">Die **SetReturnVar** -Aktion wird verwendet, um eine **ReturnVar**zu erstellen, die von Makros verwendet werden kann, die ein datenmakro mithilfe der **ausführendatenmakro** -Aktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bad8c-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="bad8c-121">Nachdem ein **ReturnVar** durch die **SetReturnVar** -Aktion erstellt wurde, kann es in einem Ausdruck vom aufrufenden Makro verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bad8c-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="bad8c-122">Wenn Sie beispielsweise einen **ReturnVar** mit dem Namen **UpdateSuccess**erstellt haben, können Sie die Variable mithilfe der folgenden Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="bad8c-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="bad8c-123">Die **SetReturnVar** -Aktion kann nur in benannten datenmakros verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bad8c-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="bad8c-124">Sie ist in datenmakros, die an ein datenmakro Ereignis angefügt sind, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bad8c-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="bad8c-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bad8c-125">Example</span></span>

<span data-ttu-id="bad8c-126">Das folgende Beispiel zeigt, wie Sie die SetReturnVar-Aktion verwenden, um einen Wert aus einem benannten datenmakro zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="bad8c-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="bad8c-127">Ein ReturnVar mit dem Namen **CurrentServiceRequest** wird an das Makro oder die VBA-Unterroutine (Visual Basic für Applikationen) zurückgegeben, die das benannte datenmakro aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="bad8c-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="bad8c-128">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="bad8c-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
