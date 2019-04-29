---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fdance-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409048"
---
# <a name="fdance"></a><span data-ttu-id="75702-104">fDance</span><span class="sxs-lookup"><span data-stu-id="75702-104">fDance</span></span>

 <span data-ttu-id="75702-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75702-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="75702-106">Beispiel für einen benutzerdefinierten Befehl, mit dem die markierten Zellen des aktiven Arbeitsblatts geändert werden, bis der Benutzer **ESC**drückt.</span><span class="sxs-lookup"><span data-stu-id="75702-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="75702-107">Wenn GENERIC. XLL geladen wird, wird ein benutzerdefiniertes Menü generisch erstellt, über das auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="75702-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="75702-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="75702-108">Parameters</span></span>

<span data-ttu-id="75702-109">Die Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="75702-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="75702-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75702-110">Property value/Return value</span></span>

<span data-ttu-id="75702-111">Die Funktion gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="75702-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75702-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75702-112">Remarks</span></span>

<span data-ttu-id="75702-113">Dies ist ein Beispiel für einen langwierigen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="75702-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="75702-114">Die Funktion [XlAbort](xlabort.md) wird gelegentlich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="75702-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="75702-115">Dadurch wird der Prozessor (bei kooperativem Multitasking) und überprüft, ob der Benutzer **ESC** gedrückt hat, um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="75702-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="75702-116">Wenn dies der Fall ist, bietet er dem Benutzer die Möglichkeit, den Abbruch abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="75702-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="75702-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="75702-117">Example</span></span>

<span data-ttu-id="75702-118">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="75702-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75702-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75702-119">See also</span></span>



[<span data-ttu-id="75702-120">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="75702-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

