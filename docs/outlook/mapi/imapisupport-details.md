---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9923813d821e2b34497e3b498c19ce22ceda2eb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792351"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="1b849-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="1b849-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="1b849-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b849-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b849-105">Zeigt ein Dialogfeld, das Details zu einem bestimmten Buch Adresseintrag anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1b849-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1b849-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b849-106">Parameters</span></span>

 <span data-ttu-id="1b849-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1b849-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="1b849-108">[out] Ein Zeiger auf das Handle für das übergeordnete Fenster des Dialogfelds zurückgegebene.</span><span class="sxs-lookup"><span data-stu-id="1b849-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="1b849-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="1b849-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="1b849-110">[in] Ein Zeiger auf eine Funktion, die basierend auf dem [DISMISSMODELESS](dismissmodeless.md) Prototyp oder NULL.</span><span class="sxs-lookup"><span data-stu-id="1b849-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="1b849-111">Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1b849-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="1b849-112">MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse informiert einen Client, der **IMAPISupport::Details** anruft, dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="1b849-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="1b849-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="1b849-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="1b849-114">[in] Ein Zeiger auf Kontextinformationen zum Übergeben an die Funktion **DISMISSMODELESS** an, durch den Parameter _LpfnDismiss_ auf.</span><span class="sxs-lookup"><span data-stu-id="1b849-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="1b849-115">Dieser Parameter gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag in den Parameter _UlFlags_ einschließen.</span><span class="sxs-lookup"><span data-stu-id="1b849-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1b849-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1b849-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="1b849-117">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="1b849-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1b849-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1b849-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="1b849-119">[in] Ein Zeiger auf die Eintrags-ID für die Details angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1b849-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="1b849-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="1b849-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="1b849-121">[in] Ein Zeiger auf eine Funktion, die basierend auf den [LPFNBUTTON](lpfnbutton.md) Funktionsprototyp.</span><span class="sxs-lookup"><span data-stu-id="1b849-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="1b849-122">Eine **LPFNBUTTON** -Funktion hinzugefügt im Dialogfeld Details der eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="1b849-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="1b849-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="1b849-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="1b849-124">[in] Ein Zeiger auf Daten, die als Parameter für die Funktion, die durch den _LpfButtonCallback_ -Parameter angegebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b849-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="1b849-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="1b849-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="1b849-126">[in] Ein Zeiger auf eine Zeichenfolge, die auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist Text enthält.</span><span class="sxs-lookup"><span data-stu-id="1b849-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="1b849-127">Der Parameter _LpszButtonText_ sollte NULL sein, wenn eine nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1b849-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="1b849-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b849-128">_ulFlags_</span></span>
  
> <span data-ttu-id="1b849-129">[in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert.</span><span class="sxs-lookup"><span data-stu-id="1b849-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="1b849-130">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1b849-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="1b849-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="1b849-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="1b849-132">Die modale Version von der Adresse Standarddialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1b849-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="1b849-133">Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="1b849-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="1b849-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="1b849-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="1b849-135">Die ohne Modus Version von der Adresse Standarddialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1b849-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="1b849-136">Dieses Kennzeichen ist mit DIALOG_MODAL gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="1b849-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="1b849-137">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1b849-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1b849-138">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="1b849-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1b849-139">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="1b849-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b849-140">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1b849-140">Return value</span></span>

<span data-ttu-id="1b849-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b849-141">S_OK</span></span> 
  
> <span data-ttu-id="1b849-142">Im Dialogfeld Details der wurde erfolgreich für den Adresseintrag Adressbuch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1b849-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b849-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b849-143">Remarks</span></span>

<span data-ttu-id="1b849-144">Die **IMAPISupport::Details** -Methode wird für Address Book Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="1b849-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="1b849-145">Von adressbuchanbietern implementierte rufen Sie **Details** , um ein Dialogfeld angezeigt, das Details zu einem bestimmten Eintrag im Adressbuch bietet.</span><span class="sxs-lookup"><span data-stu-id="1b849-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="1b849-146">Der Parameter _LpfButtonCallback_, _LpvButtonContext_und _LpszButtonText_ können verwendet werden, um das Dialogfeld eine Schaltfläche Client definiert hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1b849-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="1b849-147">Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Callback-Funktion, die auf den _LpfButtonCallback_, sowohl die Eintrags-ID für die Schaltfläche und die Daten in _LpvButtonContext_übergeben.</span><span class="sxs-lookup"><span data-stu-id="1b849-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="1b849-148">Falls eine erweiterbare Schaltfläche nicht erforderlich ist, sollte _LpszButtonText_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1b849-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b849-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b849-149">See also</span></span>



[<span data-ttu-id="1b849-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="1b849-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="1b849-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="1b849-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="1b849-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="1b849-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="1b849-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b849-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

