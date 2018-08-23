---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7cae156e29503c8b50755c99023805aa6d14e704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573369"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="29976-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="29976-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="29976-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29976-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29976-105">Trennt die zusammengesetzter Eintrags-ID eines Objekts in der Regel eine Meldung in einem Nachrichtenspeicher in die Eintrags-ID dieses Objekts im Speicher und den Store-Eintrags-ID an.</span><span class="sxs-lookup"><span data-stu-id="29976-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29976-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="29976-106">Header file:</span></span>  <br/> |<span data-ttu-id="29976-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="29976-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="29976-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="29976-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="29976-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="29976-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="29976-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="29976-110">Called by:</span></span>  <br/> |<span data-ttu-id="29976-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="29976-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="29976-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="29976-112">Parameters</span></span>

 <span data-ttu-id="29976-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="29976-113">_psession_</span></span>
  
> <span data-ttu-id="29976-114">[in] Zeiger auf die Sitzung von der Clientanwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="29976-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="29976-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="29976-115">_cbEID_</span></span>
  
> <span data-ttu-id="29976-116">[in] Größe in Bytes des Bezeichners zusammengesetzter Eintrag getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="29976-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="29976-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="29976-117">_pEID_</span></span>
  
> <span data-ttu-id="29976-118">[in] Zeiger auf den Eintrag zusammengesetzter Bezeichner getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="29976-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="29976-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="29976-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="29976-120">[out] Zeiger auf die zurückgegebene Größe in Bytes für die Eintrags-ID des Nachrichtenspeichers, die das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="29976-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="29976-121">Wenn der Parameter _pEID_ auf eine noncompound Eintrags-ID verweist, verweist der Parameter _PcbStoreEID_ auf den Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="29976-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="29976-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="29976-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="29976-123">[out] Zeiger auf einen Zeiger auf das zurückgegebene Eintrags-ID des Nachrichtenspeichers, die das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="29976-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="29976-124">Wenn der Parameter _pEID_ auf eine noncompound Eintrags-ID verweist, wird im Parameter _PpStoreEID_ NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29976-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="29976-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="29976-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="29976-126">[out] Zeiger auf die zurückgegebene Größe, der die Eintrags-ID des Objekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="29976-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="29976-127">Wenn der Parameter _pEID_ auf einen Bezeichner noncompound Eintrag zeigt, ist der Parameter _PcbMsgEID_ gleich dem Wert des Parameters _CbEID_ .</span><span class="sxs-lookup"><span data-stu-id="29976-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="29976-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="29976-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="29976-129">[out] Zeiger auf einen Zeiger auf das zurückgegebene Eintrags-ID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="29976-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="29976-130">Wenn der Parameter _pEID_ auf eine noncompound Eintrags-ID verweist, verweist _PpMsgEID_ auf einen Zeiger auf eine Kopie des Bezeichners noncompound Eintrag.</span><span class="sxs-lookup"><span data-stu-id="29976-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="29976-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29976-131">Return value</span></span>

<span data-ttu-id="29976-132">None.</span><span class="sxs-lookup"><span data-stu-id="29976-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29976-133">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="29976-133">Remarks</span></span>

<span data-ttu-id="29976-134">Wenn vom _pEID_ -Parameter angegebene Bezeichner zusammengesetzter ist, wird es in die Eintrags-ID des Objekts in seiner Nachrichtenspeicher und den Store-Eintrags-ID unterteilt.</span><span class="sxs-lookup"><span data-stu-id="29976-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="29976-135">Noncompound Eintrags-ID-Zeichenfolgen werden einfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="29976-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="29976-136">Der zusammengesetzte Bezeichner, der getrennt werden ist in der Regel durch die Funktion [HrComposeEID](hrcomposeeid.md) erstellt.</span><span class="sxs-lookup"><span data-stu-id="29976-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="29976-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="29976-137">Notes to callers</span></span>

<span data-ttu-id="29976-138">Nach dem erfolgreichen Abschluss dieser Funktion wird der Speicher, der den Parameter _pEID enthält,_ freigegeben.</span><span class="sxs-lookup"><span data-stu-id="29976-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="29976-139">Die aufrufende Implementierung ist verantwortlich für die Freigabe von Speicher für die Ausgabeparameter.</span><span class="sxs-lookup"><span data-stu-id="29976-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

