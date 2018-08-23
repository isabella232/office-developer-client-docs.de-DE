---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e240ec4e7a61b9e7484f467926501f8c5f5a59f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592346"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="8d547-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="8d547-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="8d547-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d547-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d547-105">Zeigt ein Dialogfeld, das Details zu einem bestimmten Buch Adresseintrag anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8d547-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="8d547-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d547-106">Parameters</span></span>

 <span data-ttu-id="8d547-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8d547-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="8d547-108">[in] Ein Zeiger auf ein Handle für das übergeordnete Fenster für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8d547-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="8d547-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="8d547-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="8d547-110">[in] Ein Zeiger auf eine Funktion, die basierend auf dem [DISMISSMODELESS](dismissmodeless.md) Prototyp oder NULL.</span><span class="sxs-lookup"><span data-stu-id="8d547-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="8d547-111">Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8d547-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="8d547-112">MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse informiert einen Client, der **Details** anruft, dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="8d547-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="8d547-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="8d547-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="8d547-114">[in] Ein Zeiger auf Kontextinformationen zum Übergeben an die Funktion **DISMISSMODELESS** an, durch den Parameter _LpfnDismiss_ auf.</span><span class="sxs-lookup"><span data-stu-id="8d547-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="8d547-115">Dieser Parameter gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag in den Parameter _UlFlags_ einschließen.</span><span class="sxs-lookup"><span data-stu-id="8d547-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8d547-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d547-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="8d547-117">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="8d547-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8d547-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d547-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="8d547-119">[in] Ein Zeiger auf die Eintrags-ID für den Eintrag für den Details angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8d547-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="8d547-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="8d547-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="8d547-121">[in] Ein Zeiger auf eine Funktion, die basierend auf den [LPFNBUTTON](lpfnbutton.md) Funktionsprototyp.</span><span class="sxs-lookup"><span data-stu-id="8d547-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="8d547-122">Eine **LPFNBUTTON** -Funktion hinzugefügt im Dialogfeld Details der eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="8d547-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="8d547-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="8d547-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="8d547-124">[in] Ein Zeiger auf Daten, die als Parameter für die Funktion, die durch den _LpfButtonCallback_ -Parameter angegebenen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8d547-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="8d547-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="8d547-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="8d547-126">[in] Ein Zeiger auf eine Zeichenfolge mit Text auf die Schaltfläche hinzugefügt, angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="8d547-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="8d547-127">Der Parameter _LpszButtonText_ sollte NULL sein, wenn Sie nicht über eine Schaltfläche extensible benötigen.</span><span class="sxs-lookup"><span data-stu-id="8d547-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="8d547-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d547-128">_ulFlags_</span></span>
  
> <span data-ttu-id="8d547-129">[in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert.</span><span class="sxs-lookup"><span data-stu-id="8d547-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="8d547-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8d547-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="8d547-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="8d547-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="8d547-132">Gibt an, dass **Details** gibt S_OK zurück, wenn die Adresse; tatsächlich geändert werden **Details** haben andernfalls S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="8d547-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="8d547-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="8d547-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="8d547-134">Anzeigen der modalen Version allgemeine Adresse im Dialogfeld, der immer in nicht-Outlook-Clients angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8d547-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="8d547-135">Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="8d547-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="8d547-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="8d547-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="8d547-137">Die ohne Modus Version von der Adresse Standarddialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d547-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="8d547-138">Dieses Kennzeichen werden für nicht-Outlook-Clients ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8d547-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="8d547-139">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8d547-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8d547-140">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="8d547-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="8d547-141">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="8d547-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d547-142">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8d547-142">Return value</span></span>

<span data-ttu-id="8d547-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d547-143">S_OK</span></span> 
  
> <span data-ttu-id="8d547-144">Im Dialogfeld Details der wurde erfolgreich für den Adresseintrag Adressbuch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d547-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d547-145">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="8d547-145">Remarks</span></span>

<span data-ttu-id="8d547-146">Clientanwendungen rufen Sie die **Details** -Methode, um ein Dialogfeld angezeigt, das Details zu einem bestimmten Eintrag im Adressbuch bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8d547-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="8d547-147">Der Parameter _LpfButtonCallback_, _LpvButtonContext_und _LpszButtonText_ können, um das Dialogfeld eine Schaltfläche Client definiert hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8d547-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="8d547-148">Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Callback-Funktion, die auf den _LpfButtonCallback_, sowohl die Eintrags-ID für die Schaltfläche und die Daten in _LpvButtonContext_übergeben.</span><span class="sxs-lookup"><span data-stu-id="8d547-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="8d547-149">Wenn Sie eine extensible Schaltfläche nicht erforderlich ist, sollte _LpszButtonText_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8d547-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="8d547-150">**Details** unterstützt Unicode-Zeichenfolgen. Unicode-Zeichenfolgen werden in der multibyte-Zeichenfolge handeln Zeichenformat konvertiert, bevor sie im Dialogfeld Details angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8d547-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8d547-151">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="8d547-151">MFCMAPI reference</span></span>

<span data-ttu-id="8d547-152">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8d547-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8d547-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8d547-153">**File**</span></span>|<span data-ttu-id="8d547-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8d547-154">**Function**</span></span>|<span data-ttu-id="8d547-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8d547-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d547-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="8d547-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="8d547-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="8d547-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="8d547-158">MFCMAPI (engl.) verwendet die **Details** -Methode, um ein Dialogfeld angezeigt, das Details für ein Buch Adresseintrag anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8d547-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d547-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d547-159">See also</span></span>



[<span data-ttu-id="8d547-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="8d547-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="8d547-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="8d547-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="8d547-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="8d547-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="8d547-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8d547-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="8d547-164">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8d547-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

