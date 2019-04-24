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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325669"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="84840-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="84840-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="84840-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84840-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84840-105">Konvertiert die interne Eintrags-ID eines Nachrichtenspeichers in eine Eintrags-ID, die vom Messagingsystem nutzbar ist.</span><span class="sxs-lookup"><span data-stu-id="84840-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84840-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="84840-106">Header file:</span></span>  <br/> |<span data-ttu-id="84840-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="84840-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="84840-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="84840-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="84840-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="84840-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="84840-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="84840-110">Called by:</span></span>  <br/> |<span data-ttu-id="84840-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="84840-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="84840-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="84840-112">Parameters</span></span>

 <span data-ttu-id="84840-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="84840-113">_ulFlags_</span></span>
  
> <span data-ttu-id="84840-114">in Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="84840-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="84840-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="84840-115">The following flag can be set:</span></span>
    
<span data-ttu-id="84840-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84840-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="84840-117">Die Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="84840-117">The strings are in Unicode format.</span></span> <span data-ttu-id="84840-118">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="84840-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="84840-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="84840-119">_szDLLName_</span></span>
  
> <span data-ttu-id="84840-120">in Der Name der DLL des Nachrichtenspeicher Anbieters.</span><span class="sxs-lookup"><span data-stu-id="84840-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="84840-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="84840-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="84840-122">in Größe (in Bytes) der ursprünglichen Eintrags-ID für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="84840-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="84840-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="84840-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="84840-124">in Zeiger auf eine [Eintrags](entryid.md) -ID-Struktur, die den ursprünglichen Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="84840-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="84840-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="84840-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="84840-126">Out Zeiger auf die Größe des neuen Eintrags Bezeichners in Bytes.</span><span class="sxs-lookup"><span data-stu-id="84840-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="84840-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="84840-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="84840-128">Out Zeiger auf einen Zeiger auf eine **Eintrags** -ID-Struktur, die den neuen Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="84840-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="84840-129">Return value</span><span class="sxs-lookup"><span data-stu-id="84840-129">Return value</span></span>

<span data-ttu-id="84840-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="84840-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84840-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84840-131">Remarks</span></span>

<span data-ttu-id="84840-132">Ein Nachrichtenspeicherobjekt behält eine interne Eintrags-ID bei, die nur für Dienstanbieter von Bedeutung ist, die mit diesem Nachrichtenspeicher in Kontakt stehen.</span><span class="sxs-lookup"><span data-stu-id="84840-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="84840-133">Für andere Messagingkomponenten stellt MAPI eine verpackte Version des internen Eintrags Bezeichners zur Verdeutlichung bereit, die dem Nachrichtenspeicher zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84840-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="84840-134">Der Anbieter für die Bereitstellen von Dienstanbietern sollte immer den ursprünglichen, unverpackten Nachrichtenspeicher Eintragsbezeichner erhalten. Clientanwendungen sollten immer die verpackte Version erhalten, die dann an beliebiger Stelle in der Messaging Domäne und in anderen Domänen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="84840-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="84840-135">Ein Dienstanbieter kann einen Eintragsbezeichner für den Nachrichtenspeicher mit der **WrapStoreEntryID** -Funktion oder der [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md) -Methode, die die **WrapStoreEntryID** -Funktion aufruft, umschließen.</span><span class="sxs-lookup"><span data-stu-id="84840-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="84840-136">Der Anbieter muss die Eintrags-ID umbrechen, wenn die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeichers verfügbar gemacht oder in einen Profil Abschnitt geschrieben wird und das **PR_STORE_ENTRYID** ([pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md)) Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="84840-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="84840-137">MAPI umschließt eine Nachrichtenspeicher-Eintrags-ID, wenn auf einen [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) -Aufruf reagiert wird.</span><span class="sxs-lookup"><span data-stu-id="84840-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="84840-138">Wenn eine Clientanwendung einen eingebundenen Nachrichtenspeicher-Eintragsbezeichner an MAPI übergibt, beispielsweise in einem [IMAPISession:: OpenEntry](imapisession-openentry.md) -Aufruf, wird die Eintrags-ID von MAPI vor der Verwendung zum Aufrufen einer Anbietermethode wie [IMSProvider:: LOGON](imsprovider-logon.md) oder [ IMSProvider:: CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="84840-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

