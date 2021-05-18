---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- dialogmsgproc-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1de1b73f5672067f07518ef3367d77349395a1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406514"
---
# <a name="dialogmsgproc"></a><span data-ttu-id="1a557-104">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="1a557-104">DIALOGMsgProc</span></span>

<span data-ttu-id="1a557-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1a557-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1a557-106">Dieses Verfahren ist dem systemeigenen Windows, das [von fShowDialog angezeigt wird,](fshowdialog.md) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1a557-106">This procedure is associated with the native Windows dialog box that [fShowDialog](fshowdialog.md) displays.</span></span> <span data-ttu-id="1a557-107">Es stellt die von Windows aufgerufenen Dienstroutinen für die Ereignisse (Nachrichten) zur Verfügung, die auftreten, wenn der Benutzer eine der Schaltflächen, Eingabefelder oder Steuerelemente des Dialogfelds betreibt.</span><span class="sxs-lookup"><span data-stu-id="1a557-107">It provides the service routines called by Windows for the events (messages) that occur when the user operates one of the dialog box's buttons, entry fields, or controls.</span></span> 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="1a557-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a557-108">Parameters</span></span>

 <span data-ttu-id="1a557-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="1a557-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="1a557-110">Enthält das HWND-Windows-Handle des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="1a557-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="1a557-111">_message_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="1a557-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="1a557-112">Die Nachricht, auf die reagiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a557-112">The message to respond to.</span></span>
  
 <span data-ttu-id="1a557-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="1a557-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="1a557-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="1a557-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="1a557-115">Argumente, die von Windows.</span><span class="sxs-lookup"><span data-stu-id="1a557-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1a557-116">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a557-116">Property value/Return value</span></span>

 <span data-ttu-id="1a557-117">**TRUE,** wenn die Nachricht verarbeitet wird, **FALSE,** wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="1a557-117">**TRUE** if message processed, **FALSE** if not.</span></span> 
  
### <a name="example"></a><span data-ttu-id="1a557-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1a557-118">Example</span></span>

<span data-ttu-id="1a557-119">Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="1a557-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a557-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a557-120">See also</span></span>



[<span data-ttu-id="1a557-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="1a557-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

