---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- Dialogmsgproc-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790396"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="901c5-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="901c5-104">DIALOGMsgProc</span></span>

<span data-ttu-id="901c5-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="901c5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="901c5-106">Dieses Verfahren ist zugeordnet, mit dem systemeigenen Windows-Dialogfeld, [fShowDialog](fshowdialog.md) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="901c5-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="901c5-107">Es bietet die Service-Routinen, die von Windows für die Ereignisse (Nachrichten), die auftreten, wenn der Benutzer des Dialogfelds Schaltflächen, Felder oder Steuerelemente arbeitet aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="901c5-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="901c5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="901c5-108">Parameters</span></span>

 <span data-ttu-id="901c5-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="901c5-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="901c5-110">Enthält das HWND Windows Handle des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="901c5-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="901c5-111">_Nachricht_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="901c5-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="901c5-112">Die Nachricht zu antworten.</span><span class="sxs-lookup"><span data-stu-id="901c5-112">The message to respond to.</span></span>
  
 <span data-ttu-id="901c5-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="901c5-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="901c5-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="901c5-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="901c5-115">Durch Windows übergebene Argumente.</span><span class="sxs-lookup"><span data-stu-id="901c5-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="901c5-116">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="901c5-116">Property value/Return value</span></span>

 <span data-ttu-id="901c5-117">**True,** Wenn die Nachricht verarbeitet, **FALSE,** Wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="901c5-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="901c5-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="901c5-118">Example</span></span>

<span data-ttu-id="901c5-119">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="901c5-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="901c5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="901c5-120">See also</span></span>



[<span data-ttu-id="901c5-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="901c5-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

