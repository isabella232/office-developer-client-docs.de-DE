---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409209"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="0234e-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="0234e-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="0234e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0234e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0234e-105">Konvertiert den internen Eintragsbezeichner eines Nachrichtenspeichers in einen Eintragsbezeichner, der vom Messagingsystem besser verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0234e-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0234e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0234e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0234e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0234e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0234e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0234e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0234e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0234e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0234e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0234e-110">Called by:</span></span>  <br/> |<span data-ttu-id="0234e-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0234e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="0234e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0234e-112">Parameters</span></span>

 <span data-ttu-id="0234e-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0234e-113">_ulFlags_</span></span>
  
> <span data-ttu-id="0234e-114">[in] Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="0234e-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="0234e-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0234e-115">The following flag can be set:</span></span>
    
<span data-ttu-id="0234e-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0234e-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0234e-117">Die Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="0234e-117">The strings are in Unicode format.</span></span> <span data-ttu-id="0234e-118">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="0234e-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="0234e-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="0234e-119">_szDLLName_</span></span>
  
> <span data-ttu-id="0234e-120">[in] Der Name der Nachrichtenspeicheranbieter-DLL.</span><span class="sxs-lookup"><span data-stu-id="0234e-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="0234e-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="0234e-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="0234e-122">[in] Größe des ursprünglichen Eintragsbezeichners für den Nachrichtenspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0234e-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="0234e-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="0234e-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="0234e-124">[in] Zeiger auf eine [ENTRYID-Struktur,](entryid.md) die den ursprünglichen Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="0234e-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="0234e-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="0234e-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="0234e-126">[out] Zeiger auf die Größe des neuen Eintragsbezeichners in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0234e-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="0234e-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="0234e-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="0234e-128">[out] Zeiger auf einen Zeiger auf eine **ENTRYID-Struktur,** die den neuen Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="0234e-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0234e-129">Return value</span><span class="sxs-lookup"><span data-stu-id="0234e-129">Return value</span></span>

<span data-ttu-id="0234e-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="0234e-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0234e-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0234e-131">Remarks</span></span>

<span data-ttu-id="0234e-132">Ein Nachrichtenspeicherobjekt behält einen internen Eintragsbezeichner bei, der nur für Dienstanbieter sinnvoll ist, die mit diesem Nachrichtenspeicher zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0234e-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="0234e-133">Für andere Messagingkomponenten stellt MAPI eine umschlossene Version des internen Eintragsbezeichners zur Verfügung, die ihn als zum Nachrichtenspeicher gehörig erkennbar macht.</span><span class="sxs-lookup"><span data-stu-id="0234e-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="0234e-134">Coresident-Dienstanbieter sollten immer den ursprünglichen eintragsbezeichner des nachrichtenspeichers erhalten. Clientanwendungen sollten immer die umschlossene Version erhalten, die dann überall in der Messagingdomäne und in anderen Domänen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0234e-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="0234e-135">Ein Dienstanbieter kann einen Nachrichtenspeichereintragsbezeichner mithilfe der **WrapStoreEntryID-Funktion** oder der [IMAPISupport::WrapStoreEntryID-Methode](imapisupport-wrapstoreentryid.md) umschließen, die die **WrapStoreEntryID-Funktion** aufruft.</span><span class="sxs-lookup"><span data-stu-id="0234e-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="0234e-136">Der Anbieter muss die Eintrags-ID umschließen, wenn die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeichers verfügbar ist oder in einen Profilabschnitt geschrieben wird, und wenn die **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) -Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0234e-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="0234e-137">MAPI umschließt einen Nachrichtenspeichereintragsbezeichner, wenn auf einen [IMAPISession::OpenMsgStore-Aufruf reagiert](imapisession-openmsgstore.md) wird.</span><span class="sxs-lookup"><span data-stu-id="0234e-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="0234e-138">Wenn eine Clientanwendung einen umschlossenen Nachrichtenspeichereintragsbezeichner an MAPI übergibt, z. B. in einem [IMAPISession::OpenEntry-Aufruf,](imapisession-openentry.md) entpackt MAPI den Eintragsbezeichner, bevor er zum Aufrufen einer Anbietermethode wie [IMSProvider::Logon](imsprovider-logon.md) oder [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0234e-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

