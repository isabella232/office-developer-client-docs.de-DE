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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708158"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="0faf0-102">SetReturnVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="0faf0-102">SetReturnVar macro action</span></span>

<span data-ttu-id="0faf0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0faf0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0faf0-104">Die **SetReturnVar** -Aktion erstellt eine Variable zurückgegebene und platziert es in einem bestimmten Wert.</span><span class="sxs-lookup"><span data-stu-id="0faf0-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="0faf0-105">Die **SetReturnVar** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0faf0-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="0faf0-106">Setting</span><span class="sxs-lookup"><span data-stu-id="0faf0-106">Setting</span></span>

<span data-ttu-id="0faf0-107">Die **SetReturnVar** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="0faf0-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0faf0-108">Argument</span><span class="sxs-lookup"><span data-stu-id="0faf0-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0faf0-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="0faf0-109">Required</span></span></p></th>
<th><p><span data-ttu-id="0faf0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0faf0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0faf0-111">Name</span><span class="sxs-lookup"><span data-stu-id="0faf0-111">Name</span></span></p></td>
<td><p><span data-ttu-id="0faf0-112">Ja</span><span class="sxs-lookup"><span data-stu-id="0faf0-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="0faf0-113">Eine Zeichenfolge, die den Namen der Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="0faf0-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0faf0-114">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="0faf0-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="0faf0-115">Ja</span><span class="sxs-lookup"><span data-stu-id="0faf0-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="0faf0-116">Ein Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0faf0-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="0faf0-117">Setzen Sie den Ausdruck mit dem Gleichheitszeichen (=).</span><span class="sxs-lookup"><span data-stu-id="0faf0-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="0faf0-118">Sie können klicken Sie auf die Schaltfläche <strong>Erstellen</strong> , um den <strong>Ausdrucks-Generator</strong> verwenden, um dieses Argument festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0faf0-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0faf0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0faf0-119">Remarks</span></span>

<span data-ttu-id="0faf0-120">Die Aktion **SetReturnVar** dient zum Erstellen einer **ReturnVar**die Variable, die von Makros kann, die ein Datenmakro Aufrufen verwendet werden, indem Sie mit der **AusführenDatenmakro** -Aktion ist.</span><span class="sxs-lookup"><span data-stu-id="0faf0-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="0faf0-121">Sobald ein **ReturnVar** durch die **SetReturnVar** -Aktion erstellt wurde, kann das aufrufende Makro in einem Ausdruck verwenden.</span><span class="sxs-lookup"><span data-stu-id="0faf0-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="0faf0-122">Angenommen, wenn Sie eine **ReturnVar** mit dem Namen **UpdateSuccess**erstellt, können die Variable Sie mithilfe der folgenden Syntax:</span><span class="sxs-lookup"><span data-stu-id="0faf0-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="0faf0-123">Die **SetReturnVar** -Aktion kann nur in benannten Datenmakros verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0faf0-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="0faf0-124">Es ist nicht verfügbar in Datenmakros, die ein Ereignis eines Makro zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0faf0-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="0faf0-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0faf0-125">Example</span></span>

<span data-ttu-id="0faf0-126">Das folgende Beispiel veranschaulicht die SetReturnVar-Aktion verwenden, um einen Wert aus ein benanntes Datenmakro zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="0faf0-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="0faf0-127">Eine mit dem Namen **CurrentServiceRequest** ReturnVar wird an das Makro oder Visual Basic für Applikationen (VBA) Unterroutine zurückgegeben, die das benanntes Datenmakro aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0faf0-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="0faf0-128">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="0faf0-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
