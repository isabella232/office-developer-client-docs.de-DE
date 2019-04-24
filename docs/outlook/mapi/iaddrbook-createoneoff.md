---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349315"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="68585-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="68585-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="68585-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68585-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68585-105">Erstellt eine Eintrags-ID für eine einmalige Adresse.</span><span class="sxs-lookup"><span data-stu-id="68585-105">Creates an entry identifier for a one-off address.</span></span>
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="68585-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68585-106">Parameters</span></span>

 <span data-ttu-id="68585-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="68585-107">_lpszName_</span></span>
  
> <span data-ttu-id="68585-108">in Ein Zeiger auf den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="68585-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="68585-109">Der _lpszName_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="68585-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="68585-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="68585-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="68585-111">in Ein Zeiger auf den Adresstyp des Empfängers, wie FAX oder SMTP.</span><span class="sxs-lookup"><span data-stu-id="68585-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="68585-112">Der _lpszAdrType_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="68585-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="68585-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="68585-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="68585-114">in Ein Zeiger auf die Adresse des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="68585-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="68585-115">Der _lpszAddress_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="68585-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="68585-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68585-116">_ulFlags_</span></span>
  
> <span data-ttu-id="68585-117">in Eine Bitmaske von Flags, die sich auf den einmaligen Empfänger auswirkt.</span><span class="sxs-lookup"><span data-stu-id="68585-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="68585-118">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="68585-118">The following flags can be set:</span></span>
    
<span data-ttu-id="68585-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="68585-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="68585-120">Der Empfänger kann formatierten Nachrichteninhalt nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="68585-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="68585-121">Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft des Empfängers auf false fest.</span><span class="sxs-lookup"><span data-stu-id="68585-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="68585-122">Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die Messaging Adresse des Empfängers, auf die durch _lpszAddress_ verwiesen wird, wird als Internet Adresse interpretiert.</span><span class="sxs-lookup"><span data-stu-id="68585-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="68585-123">In diesem Fall wird **PR_SEND_RICH_INFO** auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="68585-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="68585-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="68585-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="68585-125">Der Anzeigename, der Adresstyp und die Adresse sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="68585-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="68585-126">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="68585-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="68585-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="68585-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="68585-128">Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="68585-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="68585-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="68585-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="68585-130">Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmaligen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="68585-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="68585-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68585-131">Return value</span></span>

<span data-ttu-id="68585-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="68585-132">S_OK</span></span> 
  
> <span data-ttu-id="68585-133">Der einmalige Eintragsbezeichner wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="68585-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68585-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68585-134">Remarks</span></span>

<span data-ttu-id="68585-135">Clients rufen die **CreateOneOff** -Methode auf, um eine Eintrags-ID für einen einmaligen Empfänger zu erstellen: einen Empfänger, der keinem der Container eines der derzeit geladenen Adressbuchanbieter angehört.</span><span class="sxs-lookup"><span data-stu-id="68585-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="68585-136">Einmal Empfänger können jede Art von Adresse haben, die von einem der aktiven Adressbuchanbieter für die Sitzung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="68585-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="68585-137">Einmal Empfänger werden in der Regel mit einer Vorlage für ihren jeweiligen Adresstyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="68585-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="68585-138">Der Adressbuchanbieter, der den Adresstyp unterstützt, liefert die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="68585-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="68585-139">Ein Benutzer einer Clientanwendung gibt die relevanten Informationen in die Vorlage ein.</span><span class="sxs-lookup"><span data-stu-id="68585-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="68585-140">MAPI unterstützt Unicode-Zeichenfolgen für den Anzeigenamen, den Adresstyp und die Adressparameter von **CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="68585-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="68585-141">Das MAPI_SEND_NO_RICH_INFO-Flag steuert, ob formatierter Text im Rich-Text-Format (RTF) zusammen mit jeder Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="68585-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="68585-142">Das Transport Neutral Encapsulation Format (TNEF) – ein Format, das für die Übertragung von formatiertem Text verwendet wird – wird von den meisten Transport Anbietern gesendet, unabhängig davon, wie der Empfänger seine **PR_SEND_RICH_INFO** -Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="68585-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="68585-143">Dies ist kein Problem für Messaging-Clients, die mit zwischenmenschlichen Nachrichten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="68585-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="68585-144">Da TNEF jedoch normalerweise zum Senden benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird, kann dies ein Problem für formularbasierte Clients oder Clients sein, die benutzerdefinierte MAPI-Eigenschaften erfordern.</span><span class="sxs-lookup"><span data-stu-id="68585-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="68585-145">Weitere Informationen finden Sie unter [Senden von Nachrichten mit TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="68585-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="68585-146">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="68585-146">MFCMAPI reference</span></span>

<span data-ttu-id="68585-147">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="68585-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="68585-148">**Datei**</span><span class="sxs-lookup"><span data-stu-id="68585-148">**File**</span></span>|<span data-ttu-id="68585-149">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="68585-149">**Function**</span></span>|<span data-ttu-id="68585-150">**Comment**</span><span class="sxs-lookup"><span data-stu-id="68585-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68585-151">Mapiabfunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="68585-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="68585-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="68585-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="68585-153">MFCMAPI verwendet die **CreateOneOff** -Methode, um eine EINTRAGS-ID für eine Adresse zu erstellen, die in keinem Adressbuch gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="68585-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68585-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68585-154">See also</span></span>



[<span data-ttu-id="68585-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="68585-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="68585-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="68585-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="68585-157">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="68585-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

