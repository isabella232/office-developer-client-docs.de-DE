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
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424679"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="18f74-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="18f74-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="18f74-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18f74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18f74-105">Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="18f74-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="18f74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="18f74-106">Parameters</span></span>

 <span data-ttu-id="18f74-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="18f74-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="18f74-108">[in] Ein Zeiger auf ein Handle des übergeordneten Fensters für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="18f74-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="18f74-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="18f74-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="18f74-110">[in] Ein Zeiger auf eine Funktion basierend auf dem [DISMISSMODELESS-Prototyp](dismissmodeless.md) oder NULL.</span><span class="sxs-lookup"><span data-stu-id="18f74-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="18f74-111">Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="18f74-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="18f74-112">MAPI ruft die **FUNKTION DISMISSMODELESS** auf, wenn der Benutzer das Dialogfeld "Modeless Address" schließt und einen Client informiert, der **Details** aufruft, dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="18f74-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="18f74-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="18f74-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="18f74-114">[in] Ein Zeiger auf Kontextinformationen, der an die **DISMISSMODELESS-Funktion übergeben** wird, auf die der  _lpfnDismiss-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="18f74-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="18f74-115">Dieser Parameter gilt nur für die moduslose Version des Dialogfelds, indem das DIALOG_SDI im  _ulFlags-Parameter verwendet_ wird.</span><span class="sxs-lookup"><span data-stu-id="18f74-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="18f74-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="18f74-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="18f74-117">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="18f74-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="18f74-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="18f74-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="18f74-119">[in] Ein Zeiger auf die Eintrags-ID für den Eintrag, für den Details angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="18f74-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="18f74-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="18f74-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="18f74-121">[in] Ein Zeiger auf eine Funktion basierend auf dem [LPFNBUTTON-Funktionsprototyp.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="18f74-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="18f74-122">Eine **LPFNBUTTON-Funktion** fügt dem Dialogfeld Details eine Schaltfläche hinzu.</span><span class="sxs-lookup"><span data-stu-id="18f74-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="18f74-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="18f74-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="18f74-124">[in] Ein Zeiger auf Daten, die als Parameter für die durch den  _lpfButtonCallback-Parameter_ angegebene Funktion verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="18f74-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="18f74-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="18f74-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="18f74-126">[in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="18f74-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="18f74-127">Der  _lpszButtonText-Parameter_ sollte NULL sein, wenn Sie keine erweiterbare Schaltfläche benötigen.</span><span class="sxs-lookup"><span data-stu-id="18f74-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="18f74-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="18f74-128">_ulFlags_</span></span>
  
> <span data-ttu-id="18f74-129">[in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert.</span><span class="sxs-lookup"><span data-stu-id="18f74-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="18f74-130">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="18f74-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="18f74-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="18f74-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="18f74-132">Gibt an, dass **Details** S_OK, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls **gibt Details** S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="18f74-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="18f74-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="18f74-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="18f74-134">Zeigen Sie die modale Version des Dialogfelds allgemeine Adresse an, das immer in Nicht-Outlook angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="18f74-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="18f74-135">Dieses Flag schließen sich gegenseitig mit DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="18f74-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="18f74-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="18f74-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="18f74-137">Zeigt die moduslose Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="18f74-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="18f74-138">Dieses Flag wird für Nicht-Outlook ignoriert.</span><span class="sxs-lookup"><span data-stu-id="18f74-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="18f74-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="18f74-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="18f74-140">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="18f74-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="18f74-141">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="18f74-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="18f74-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18f74-142">Return value</span></span>

<span data-ttu-id="18f74-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="18f74-143">S_OK</span></span> 
  
> <span data-ttu-id="18f74-144">Das Dialogfeld Details wurde erfolgreich für den Adressbucheintrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18f74-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18f74-145">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18f74-145">Remarks</span></span>

<span data-ttu-id="18f74-146">Clientanwendungen rufen die **Details-Methode** auf, um ein Dialogfeld anzuzeigen, das Details zu einem bestimmten Eintrag im Adressbuch enthält.</span><span class="sxs-lookup"><span data-stu-id="18f74-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="18f74-147">Sie können die Parameter  _lpfButtonCallback,_  _lpvButtonContext_ und  _lpszButtonText_ verwenden, um dem Dialogfeld eine clientdefinierte Schaltfläche hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="18f74-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="18f74-148">Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die von _lpfButtonCallback_ verwiesen wird. Dabei wird sowohl der Eintragsbezeichner der Schaltfläche als auch die Daten in _lpvButtonContext übergeben._</span><span class="sxs-lookup"><span data-stu-id="18f74-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="18f74-149">Wenn Sie keine erweiterbare Schaltfläche benötigen,  _sollte lpszButtonText_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="18f74-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="18f74-150">**Details** unterstützen Unicode-Zeichenzeichenfolgen; Unicode-Zeichenfolgen werden in das MbCS-Format (MultiByte Character String) konvertiert, bevor sie im Dialogfeld Details angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="18f74-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="18f74-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="18f74-151">MFCMAPI reference</span></span>

<span data-ttu-id="18f74-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="18f74-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="18f74-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="18f74-153">**File**</span></span>|<span data-ttu-id="18f74-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="18f74-154">**Function**</span></span>|<span data-ttu-id="18f74-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="18f74-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18f74-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="18f74-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="18f74-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="18f74-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="18f74-158">MFCMAPI verwendet die **Details-Methode,** um ein Dialogfeld anzuzeigen, in dem die Details für einen Adressbucheintrag angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="18f74-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18f74-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18f74-159">See also</span></span>



[<span data-ttu-id="18f74-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="18f74-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="18f74-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="18f74-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="18f74-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="18f74-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="18f74-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="18f74-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="18f74-164">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="18f74-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

