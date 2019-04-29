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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418015"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="37502-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="37502-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="37502-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37502-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37502-105">Führt eine Aufgabe wie das Anzeigen eines Dialogfelds oder das Starten eines programmgesteuerten Vorgangs aus, wenn ein Benutzer der Clientanwendung auf das Schaltflächen-Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="37502-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="37502-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37502-106">Parameters</span></span>

 <span data-ttu-id="37502-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37502-107">_ulFlags_</span></span>
  
> <span data-ttu-id="37502-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="37502-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="37502-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="37502-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="37502-110">in Ein Handle für das übergeordnete Fenster des Dialogfelds, in dem das Schaltflächen-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="37502-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37502-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37502-111">Return value</span></span>

<span data-ttu-id="37502-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="37502-112">S_OK</span></span> 
  
> <span data-ttu-id="37502-113">Das Schaltflächen-Steuerelement wurde erfolgreich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="37502-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37502-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37502-114">Remarks</span></span>

<span data-ttu-id="37502-115">Die **IMAPIControl:: Activate** -Methode führt Aufgaben aus, die auf das Klicken des Schaltflächen-Steuerelements durch einen Benutzer folgen.</span><span class="sxs-lookup"><span data-stu-id="37502-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="37502-116">Nachdem der Klick ausgeführt wurde, ruft MAPI im Rahmen der Verarbeitung der Anzeigetabelle einen Aufruf an, um die Aktivierung nach dem ersten Aufruf von [IMAPIControl:: GetState](imapicontrol-getstate.md) zu **aktivieren** , um zu bestimmen, ob die Schaltfläche aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="37502-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="37502-117">Weitere Informationen zum Implementieren von **Activate** und den anderen [IMAPIControl: IUnknown](imapicontroliunknown.md) -Methoden finden Sie unter [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="37502-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37502-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37502-118">See also</span></span>



[<span data-ttu-id="37502-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="37502-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="37502-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37502-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

