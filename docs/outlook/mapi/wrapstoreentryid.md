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
ms.openlocfilehash: aff46cca7a7d530b2eede1790176058e3b91abc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795852"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="6f118-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="6f118-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="6f118-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f118-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f118-105">Konvertiert einen Nachrichtenspeicher interne Eintrags-ID auf einen Eintrag Bezeichner Verwendbarkeit von messaging-System.</span><span class="sxs-lookup"><span data-stu-id="6f118-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f118-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6f118-106">Header file:</span></span>  <br/> |<span data-ttu-id="6f118-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f118-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6f118-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6f118-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6f118-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6f118-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6f118-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6f118-110">Called by:</span></span>  <br/> |<span data-ttu-id="6f118-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6f118-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6f118-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f118-112">Parameters</span></span>

 <span data-ttu-id="6f118-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f118-113">_ulFlags_</span></span>
  
> <span data-ttu-id="6f118-114">[in] Bitmaske der Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="6f118-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="6f118-115">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6f118-115">The following flag can be set:</span></span>
    
<span data-ttu-id="6f118-116">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f118-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6f118-117">Die Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6f118-117">The strings are in Unicode format.</span></span> <span data-ttu-id="6f118-118">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6f118-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="6f118-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="6f118-119">_szDLLName_</span></span>
  
> <span data-ttu-id="6f118-120">[in] Der Name des Anbieters Nachricht DLL.</span><span class="sxs-lookup"><span data-stu-id="6f118-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="6f118-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="6f118-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="6f118-122">[in] Größe des den ursprünglichen Eintrag Bezeichner für den Nachrichtenspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="6f118-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="6f118-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="6f118-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="6f118-124">[in] Zeiger auf eine [ENTRYID](entryid.md) -Struktur, die die ursprünglichen Eintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="6f118-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="6f118-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="6f118-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="6f118-126">[out] Zeiger auf die Größe des neuen Eintrags-ID in Bytes.</span><span class="sxs-lookup"><span data-stu-id="6f118-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="6f118-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="6f118-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="6f118-128">[out] Zeiger auf einen Zeiger auf eine **ENTRYID** -Struktur, die die neue Eintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="6f118-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6f118-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f118-129">Return value</span></span>

<span data-ttu-id="6f118-130">None.</span><span class="sxs-lookup"><span data-stu-id="6f118-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f118-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f118-131">Remarks</span></span>

<span data-ttu-id="6f118-132">Ein Meldungsobjekt Store behält eine interne Eintrags-ID der nur für Service Provider Coresident mit diesem Nachrichtenspeicher von Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="6f118-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="6f118-133">Für andere Messagingkomponenten stellt MAPI eine gepackten Version von der internen Eintrags-ID, mit die Hilfe erkennbar wie, mit dem Nachrichtenspeicher gehören.</span><span class="sxs-lookup"><span data-stu-id="6f118-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="6f118-134">Coresident-Dienstanbieter müssen immer die ursprünglichen allein stehenden Store Eintrags-ID angegeben werden; Clientanwendungen sollte immer die gepackten Version angegeben werden, die dann verwendbar an einer beliebigen Stelle in der messaging-Domäne und in anderen Domänen.</span><span class="sxs-lookup"><span data-stu-id="6f118-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="6f118-135">Ein Dienstanbieter kann umschließen eine Nachricht Store Eintrag ID mit der Funktion **WrapStoreEntryID** oder die [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) -Methode, die die **WrapStoreEntryID** -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="6f118-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="6f118-136">Der Anbieter muss die Eintrags-ID umbrochen, wenn der Nachrichtenspeicher **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) Verfügbarmachen-Eigenschaft oder Schreiben in einem Profilabschnitt und, **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) verfügbar zu machen. -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6f118-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="6f118-137">MAPI umbrochen eine Nachricht Store Eintrags-ID wird, wenn Sie einem Anruf [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) reagiert.</span><span class="sxs-lookup"><span data-stu-id="6f118-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="6f118-138">Wenn eine Clientanwendung eine gepackten Store Eintrags-ID MAPI übergibt, entpackt beispielsweise einen Aufruf [IMAPISession::OpenEntry](imapisession-openentry.md) MAPI die Eintrags-ID vor der Verwendung eine Anbieter-Methode wie [IMSProvider::Logon](imsprovider-logon.md) oder [aufrufen IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="6f118-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

