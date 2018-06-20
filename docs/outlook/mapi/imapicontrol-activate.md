---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fb6cd23acdb81af250e7e6dfe6facf7226850363
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792069"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="9ea7d-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="9ea7d-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="9ea7d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ea7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ea7d-105">Führt eine Aufgabe wie etwa Anzeigen eines Dialogfelds oder einen programmgesteuerten Vorgang starten, wenn Benutzer eine Clientanwendung das Button-Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="9ea7d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ea7d-106">Parameters</span></span>

 <span data-ttu-id="9ea7d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ea7d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9ea7d-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9ea7d-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9ea7d-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="9ea7d-110">[in] Ein Handle für das übergeordnete Fenster im Dialogfeld, in dem das Schaltflächensteuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9ea7d-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9ea7d-111">Return value</span></span>

<span data-ttu-id="9ea7d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ea7d-112">S_OK</span></span> 
  
> <span data-ttu-id="9ea7d-113">Das Button-Steuerelement wurde erfolgreich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ea7d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ea7d-114">Remarks</span></span>

<span data-ttu-id="9ea7d-115">Die **IMAPIControl::Activate** -Methode führt die Aufgaben, die nach Klicken auf das Schaltflächensteuerelement eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="9ea7d-116">Klicken Sie dann auf als Teil der Verarbeitung der Tabelle anzeigen, tritt nach dem richtet MAPI eines Aufrufs an **Activate** nach der ersten aufrufenden [IMAPIControl::GetState](imapicontrol-getstate.md) um festzustellen, ob die Schaltfläche aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9ea7d-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="9ea7d-117">Weitere Informationen zum **Aktivieren** und die andere implementieren [IMAPIControl: IUnknown](imapicontroliunknown.md) Methoden finden Sie unter [Implementierung der Steuerelement-Objekts](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="9ea7d-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ea7d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ea7d-118">See also</span></span>



[<span data-ttu-id="9ea7d-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="9ea7d-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="9ea7d-120">IMAPIControl: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ea7d-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

