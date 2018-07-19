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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fefd81a7d6cdfda24df93ec928cd3305cb8ef8be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791998"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="4922e-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="4922e-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="4922e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4922e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4922e-105">Erstellt einen Eintrag Bezeichner für eine einmalige Adresse.</span><span class="sxs-lookup"><span data-stu-id="4922e-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4922e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4922e-106">Parameters</span></span>

 <span data-ttu-id="4922e-107">_Wert_</span><span class="sxs-lookup"><span data-stu-id="4922e-107">_lpszName_</span></span>
  
> <span data-ttu-id="4922e-108">[in] Ein Zeiger auf den Wert des Empfängers **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4922e-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="4922e-109">Der _Wert_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4922e-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="4922e-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="4922e-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="4922e-111">[in] Ein Zeiger auf den Typ des Empfängers, wie FAX oder SMTP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4922e-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="4922e-112">Der Parameter _LpszAdrType_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4922e-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="4922e-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="4922e-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="4922e-114">[in] Ein Zeiger auf die Adresse des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="4922e-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="4922e-115">Der Parameter _LpszAddress_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4922e-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="4922e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4922e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="4922e-117">[in] Eine Bitmaske aus Flags, die den einmal-Empfänger auswirkt.</span><span class="sxs-lookup"><span data-stu-id="4922e-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="4922e-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4922e-118">The following flags can be set:</span></span>
    
<span data-ttu-id="4922e-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="4922e-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="4922e-120">Der Empfänger kann nicht formatierte Nachrichteninhalt behandeln.</span><span class="sxs-lookup"><span data-stu-id="4922e-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="4922e-121">Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, wird der MAPI-Eigenschaft des Empfängers- **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4922e-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="4922e-122">Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, wird diese Eigenschaft von MAPI auf TRUE festgelegt, es sei denn, die Adresse des Empfängers messaging auf das _LpszAddress_ interpretiert wird, um eine IP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="4922e-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="4922e-123">In diesem Fall wird MAPI **PR_SEND_RICH_INFO** auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4922e-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="4922e-124">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4922e-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4922e-125">Der Anzeigename, Adresstyp und Adresse sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="4922e-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="4922e-126">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="4922e-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="4922e-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4922e-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="4922e-128">[out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="4922e-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4922e-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="4922e-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="4922e-130">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmaligen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="4922e-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4922e-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4922e-131">Return value</span></span>

<span data-ttu-id="4922e-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="4922e-132">S_OK</span></span> 
  
> <span data-ttu-id="4922e-133">Der Bezeichner des Eingangs wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="4922e-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4922e-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4922e-134">Remarks</span></span>

<span data-ttu-id="4922e-135">Clients rufen die **CreateOneOff** -Methode zum Erstellen eines Eintrags-ID für einen einmaligen Empfänger – einen Empfänger, die nicht zu keiner der Container aus der aktuell geladenen adressbuchanbietern implementierte gehört.</span><span class="sxs-lookup"><span data-stu-id="4922e-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="4922e-136">Einmaligen Empfänger können jede Art von-Adresse, die unterstützt wird von einem der aktiven adressbuchanbietern implementierte besitzen, für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4922e-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="4922e-137">Einmaligen Empfänger werden in der Regel mit einer Vorlage für ihre speziellen Adresstyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="4922e-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="4922e-138">Der Adressbuchanbieter, die den Adresstyp unterstützt stellt die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="4922e-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="4922e-139">Ein Benutzer von einer Clientanwendung gibt die entsprechende Informationen in die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="4922e-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="4922e-140">MAPI unterstützt Unicode-Zeichenfolgen für die Anzeigenamen, den Adresstyp und die Adressenparameter der **CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="4922e-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="4922e-141">Das Flag MAPI_SEND_NO_RICH_INFO steuert, ob formatierter Text in Rich Text Format (RTF) zusammen mit jeder Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4922e-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="4922e-142">Die Transport Neutral Encapsulation Format (TNEF) – ein Format, das für die Übertragung verwendet wird formatierter Text – wird von den meisten Transport Anbietern, unabhängig davon, wie der Empfänger die **PR_SEND_RICH_INFO** -Eigenschaft festgelegt wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="4922e-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="4922e-143">Dies gilt nicht für die messaging-Clients, die mit Nachrichten zwischen Personen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4922e-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="4922e-144">Da TNEF in der Regel zum Senden von benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird, kann nicht unterstützt, es jedoch ein Problem für formularbasierte oder Clients, die eine benutzerdefinierte MAPI-Eigenschaften erfordern.</span><span class="sxs-lookup"><span data-stu-id="4922e-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="4922e-145">Weitere Informationen finden Sie unter [Senden von Nachrichten mit TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="4922e-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4922e-146">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="4922e-146">MFCMAPI reference</span></span>

<span data-ttu-id="4922e-147">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4922e-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4922e-148">**Datei**</span><span class="sxs-lookup"><span data-stu-id="4922e-148">**File**</span></span>|<span data-ttu-id="4922e-149">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="4922e-149">**Function**</span></span>|<span data-ttu-id="4922e-150">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4922e-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4922e-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4922e-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="4922e-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="4922e-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="4922e-153">MFCMAPI (engl.) verwendet die **CreateOneOff** -Methode, um eine Eintrags-ID für eine Adresse erstellen, die in jeder Adressbuch nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="4922e-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4922e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4922e-154">See also</span></span>



[<span data-ttu-id="4922e-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="4922e-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="4922e-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4922e-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="4922e-157">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="4922e-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

