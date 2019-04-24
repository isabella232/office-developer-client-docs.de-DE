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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322358"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="cecc3-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="cecc3-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="cecc3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cecc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cecc3-105">Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cecc3-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="cecc3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cecc3-106">Parameters</span></span>

 <span data-ttu-id="cecc3-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="cecc3-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="cecc3-108">Out Ein Zeiger auf das Handle des übergeordneten Fensters des zurückgegebenen Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="cecc3-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="cecc3-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="cecc3-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="cecc3-110">in Ein Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS](dismissmodeless.md) -Prototyp basiert, oder NULL.</span><span class="sxs-lookup"><span data-stu-id="cecc3-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="cecc3-111">Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben.</span><span class="sxs-lookup"><span data-stu-id="cecc3-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="cecc3-112">MAPI Ruft die **DISMISSMODELESS** -Funktion auf, wenn der Benutzer das Dialogfeld nicht modale Adresse abschließt und einen Client informiert, der **IMAPISupport::D ails** , dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="cecc3-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="cecc3-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="cecc3-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="cecc3-114">in Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS** -Funktion übergeben werden, auf die durch den _lpfnDismiss_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cecc3-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="cecc3-115">Dieser Parameter gilt nur für die nicht modale Version des Dialogfelds, indem das DIALOG_SDI-Flag im _ulFlags_ -Parameter eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="cecc3-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="cecc3-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="cecc3-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="cecc3-117">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cecc3-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="cecc3-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="cecc3-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="cecc3-119">in Ein Zeiger auf die Eintrags-ID, für die Details angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cecc3-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="cecc3-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="cecc3-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="cecc3-121">in Ein Zeiger auf eine Funktion, die auf dem Prototyp der [LPFNBUTTON](lpfnbutton.md) -Funktion basiert.</span><span class="sxs-lookup"><span data-stu-id="cecc3-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="cecc3-122">Mit einer **LPFNBUTTON** -Funktion wird dem Dialogfeld Details eine Schaltfläche hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cecc3-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="cecc3-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="cecc3-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="cecc3-124">in Ein Zeiger auf Daten, die als Parameter für die durch den _lpfButtonCallback_ -Parameter angegebene Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cecc3-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="cecc3-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="cecc3-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="cecc3-126">in Ein Zeiger auf eine Zeichenfolge, die den Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="cecc3-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="cecc3-127">Der Parameter _lpszButtonText_ sollte NULL sein, wenn eine erweiterbare Schaltfläche nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cecc3-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="cecc3-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cecc3-128">_ulFlags_</span></span>
  
> <span data-ttu-id="cecc3-129">in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert.</span><span class="sxs-lookup"><span data-stu-id="cecc3-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="cecc3-130">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cecc3-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="cecc3-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="cecc3-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="cecc3-132">Zeigt die modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="cecc3-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="cecc3-133">Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="cecc3-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="cecc3-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="cecc3-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="cecc3-135">Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="cecc3-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="cecc3-136">Dieses Flag ist mit DIALOG_MODAL gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="cecc3-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="cecc3-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cecc3-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cecc3-138">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="cecc3-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="cecc3-139">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="cecc3-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cecc3-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cecc3-140">Return value</span></span>

<span data-ttu-id="cecc3-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="cecc3-141">S_OK</span></span> 
  
> <span data-ttu-id="cecc3-142">Das Dialogfeld Details wurde erfolgreich für den Adressbucheintrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cecc3-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cecc3-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cecc3-143">Remarks</span></span>

<span data-ttu-id="cecc3-144">Die **IMAPISupport::D ails** -Methode wird für Support Objekte des Adressbuch Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="cecc3-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="cecc3-145">Adressbuchanbieter rufen **Details** auf, um ein Dialogfeld anzuzeigen, in dem Details zu einem bestimmten Eintrag im Adressbuch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cecc3-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="cecc3-146">Der Parameter _lpfButtonCallback_, _lpvButtonContext_und _lpszButtonText_ kann verwendet werden, um dem Dialogfeld eine Client definierte Schaltfläche hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cecc3-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="cecc3-147">Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die von _lpfButtonCallback_verwiesen wird, wobei sowohl die Eintrags-ID der Schaltfläche als auch die Daten in _lpvButtonContext_übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="cecc3-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="cecc3-148">Wenn keine erweiterbare Schaltfläche erforderlich ist, sollte _LPSZBUTTONTEXT_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="cecc3-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cecc3-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cecc3-149">See also</span></span>



[<span data-ttu-id="cecc3-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="cecc3-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="cecc3-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="cecc3-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="cecc3-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="cecc3-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="cecc3-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cecc3-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

