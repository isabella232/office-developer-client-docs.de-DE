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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341720"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="6da70-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="6da70-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="6da70-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6da70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6da70-105">Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6da70-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="6da70-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6da70-106">Parameters</span></span>

 <span data-ttu-id="6da70-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6da70-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="6da70-108">in Ein Zeiger auf ein Handle des übergeordneten Fensters für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="6da70-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="6da70-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="6da70-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="6da70-110">in Ein Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS](dismissmodeless.md) -Prototyp basiert, oder NULL.</span><span class="sxs-lookup"><span data-stu-id="6da70-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="6da70-111">Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben.</span><span class="sxs-lookup"><span data-stu-id="6da70-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="6da70-112">MAPI Ruft die **DISMISSMODELESS** -Funktion auf, wenn der Benutzer das Dialogfeld nicht modale Adresse zurückweist und einen Client darüber informiert, \*\*\*\* dass das Dialogfeld nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="6da70-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="6da70-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="6da70-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="6da70-114">in Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS** -Funktion übergeben werden, auf die durch den _lpfnDismiss_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6da70-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="6da70-115">Dieser Parameter gilt nur für die nicht modale Version des Dialogfelds, indem das DIALOG_SDI-Flag im _ulFlags_ -Parameter eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6da70-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6da70-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6da70-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="6da70-117">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6da70-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6da70-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6da70-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="6da70-119">in Ein Zeiger auf die Eintrags-ID für den Eintrag, für den Details angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6da70-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="6da70-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="6da70-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="6da70-121">in Ein Zeiger auf eine Funktion, die auf dem Prototyp der [LPFNBUTTON](lpfnbutton.md) -Funktion basiert.</span><span class="sxs-lookup"><span data-stu-id="6da70-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="6da70-122">Mit einer **LPFNBUTTON** -Funktion wird dem Dialogfeld Details eine Schaltfläche hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6da70-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="6da70-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="6da70-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="6da70-124">in Ein Zeiger auf Daten, die als Parameter für die durch den _lpfButtonCallback_ -Parameter angegebene Funktion verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6da70-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="6da70-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="6da70-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="6da70-126">in Ein Zeiger auf eine Zeichenfolge, die den Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="6da70-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="6da70-127">Der _lpszButtonText_ -Parameter sollte NULL sein, wenn Sie keine erweiterbare Schaltfläche benötigen.</span><span class="sxs-lookup"><span data-stu-id="6da70-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="6da70-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6da70-128">_ulFlags_</span></span>
  
> <span data-ttu-id="6da70-129">in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert.</span><span class="sxs-lookup"><span data-stu-id="6da70-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="6da70-130">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6da70-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="6da70-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="6da70-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="6da70-132">Gibt an, dass **Details** S_OK zurückgegeben werden, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt **Details** S_FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="6da70-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="6da70-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="6da70-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="6da70-134">Zeigt die modale Version des Dialogfelds allgemeine Adresse an, das immer in nicht-Outlook-Clients angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6da70-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="6da70-135">Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="6da70-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="6da70-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="6da70-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="6da70-137">Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an.</span><span class="sxs-lookup"><span data-stu-id="6da70-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="6da70-138">Dieses Flag wird für nicht-Outlook-Clients ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6da70-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="6da70-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6da70-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6da70-140">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6da70-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6da70-141">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6da70-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6da70-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6da70-142">Return value</span></span>

<span data-ttu-id="6da70-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="6da70-143">S_OK</span></span> 
  
> <span data-ttu-id="6da70-144">Das Dialogfeld Details wurde erfolgreich für den Adressbucheintrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6da70-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6da70-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6da70-145">Remarks</span></span>

<span data-ttu-id="6da70-146">Client Anwendungen rufen die **Details** -Methode auf, um ein Dialogfeld anzuzeigen, das Details zu einem bestimmten Eintrag im Adressbuch bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6da70-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="6da70-147">Sie können die Parameter _lpfButtonCallback_, _lpvButtonContext_und _lpszButtonText_ verwenden, um dem Dialogfeld eine Client definierte Schaltfläche hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6da70-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="6da70-148">Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die von _lpfButtonCallback_verwiesen wird, wobei sowohl die Eintrags-ID der Schaltfläche als auch die Daten in _lpvButtonContext_übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6da70-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="6da70-149">Wenn Sie keine erweiterbare Schaltfläche benötigen, sollte _LPSZBUTTONTEXT_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6da70-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="6da70-150">**Details** unterstützt Unicode-Zeichenfolgen; Unicode-Zeichenfolgen werden in das Multibyte Character String-Format (MBCS) konvertiert, bevor Sie im Dialogfeld Details angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6da70-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6da70-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="6da70-151">MFCMAPI reference</span></span>

<span data-ttu-id="6da70-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6da70-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6da70-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6da70-153">**File**</span></span>|<span data-ttu-id="6da70-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6da70-154">**Function**</span></span>|<span data-ttu-id="6da70-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6da70-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6da70-156">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="6da70-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="6da70-157">CBaseDialog:: OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="6da70-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="6da70-158">MFCMAPI verwendet die **Details** -Methode, um ein Dialogfeld anzuzeigen, in dem die Details für einen Adressbucheintrag angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6da70-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6da70-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6da70-159">See also</span></span>



[<span data-ttu-id="6da70-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="6da70-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="6da70-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="6da70-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="6da70-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="6da70-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="6da70-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6da70-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="6da70-164">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6da70-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

