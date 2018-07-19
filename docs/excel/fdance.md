---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- Fdance-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790506"
---
# <a name="fdance"></a><span data-ttu-id="139f1-104">fDance</span><span class="sxs-lookup"><span data-stu-id="139f1-104">fDance</span></span>

 <span data-ttu-id="139f1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="139f1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="139f1-106">Benutzerdefinierte Beispielbefehl, der die markierten Zellen im aktiven Arbeitsblatt um zurückführt, bis der Benutzer die **ESC-Taste**drückt.</span><span class="sxs-lookup"><span data-stu-id="139f1-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="139f1-107">Wenn GENERIC.xll geladen wird, erstellt es ein Menü benutzerdefinierte allgemeine, über die auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="139f1-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="139f1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="139f1-108">Parameters</span></span>

<span data-ttu-id="139f1-109">Die Funktion akzeptiert keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="139f1-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="139f1-110">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="139f1-110">Property value/Return value</span></span>

<span data-ttu-id="139f1-111">Die Funktion gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="139f1-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="139f1-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="139f1-112">Remarks</span></span>

<span data-ttu-id="139f1-113">Dies ist ein Beispiel einer langen Operation.</span><span class="sxs-lookup"><span data-stu-id="139f1-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="139f1-114">Sie ruft die Funktion [Bereichsgröße](xlabort.md) gelegentlich.</span><span class="sxs-lookup"><span data-stu-id="139f1-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="139f1-115">Dies ergibt den Prozessor (hilft Ihnen bei der gemeinsame Multitasking), und überprüft, ob der Benutzer die **ESC-Taste** , um den Vorgang abzubrechen gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="139f1-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="139f1-116">Wenn dies der Fall ist, bietet es dem Benutzer eine Möglichkeit, diesen Vorgang abbrechen.</span><span class="sxs-lookup"><span data-stu-id="139f1-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="139f1-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="139f1-117">Example</span></span>

<span data-ttu-id="139f1-118">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="139f1-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="139f1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="139f1-119">See also</span></span>



[<span data-ttu-id="139f1-120">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="139f1-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

