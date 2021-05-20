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
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436111"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="85c3f-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="85c3f-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="85c3f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85c3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85c3f-105">Trennt die zusammengesetzte Eintrags-ID eines Objekts, in der Regel eine Nachricht in einem Nachrichtenspeicher, in die Eintrags-ID dieses Objekts im Speicher und den Eintragsbezeichner des Speichers.</span><span class="sxs-lookup"><span data-stu-id="85c3f-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85c3f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="85c3f-106">Header file:</span></span>  <br/> |<span data-ttu-id="85c3f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="85c3f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="85c3f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="85c3f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="85c3f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="85c3f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="85c3f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="85c3f-110">Called by:</span></span>  <br/> |<span data-ttu-id="85c3f-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="85c3f-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="85c3f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="85c3f-112">Parameters</span></span>

 <span data-ttu-id="85c3f-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="85c3f-113">_psession_</span></span>
  
> <span data-ttu-id="85c3f-114">[in] Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85c3f-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="85c3f-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="85c3f-115">_cbEID_</span></span>
  
> <span data-ttu-id="85c3f-116">[in] Die Größe des zusammengesetzten Eintragsbezeichners, der getrennt werden soll, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="85c3f-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="85c3f-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="85c3f-117">_pEID_</span></span>
  
> <span data-ttu-id="85c3f-118">[in] Zeiger auf den zusammengesetzten Eintragsbezeichner, der getrennt werden soll.</span><span class="sxs-lookup"><span data-stu-id="85c3f-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="85c3f-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="85c3f-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="85c3f-120">[out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Nachrichtenspeichers, der das Objekt enthält, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="85c3f-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="85c3f-121">Wenn der  _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, zeigt der  _parameter "pcbStoreEID"_ auf den Wert Null.</span><span class="sxs-lookup"><span data-stu-id="85c3f-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="85c3f-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="85c3f-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="85c3f-123">[out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID des Nachrichtenspeichers, der das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="85c3f-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="85c3f-124">Wenn der  _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, wird NULL im  _ppStoreEID-Parameter_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85c3f-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="85c3f-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="85c3f-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="85c3f-126">[out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Objekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="85c3f-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="85c3f-127">Wenn der _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, entspricht der _parameter "pcbMsgEID"_ dem Wert des _cbEID-Parameters._</span><span class="sxs-lookup"><span data-stu-id="85c3f-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="85c3f-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="85c3f-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="85c3f-129">[out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="85c3f-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="85c3f-130">Wenn der  _pEID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, zeigt  _ppMsgEID_ auf einen Zeiger auf eine Kopie der Nichtcompound-Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="85c3f-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85c3f-131">Return value</span><span class="sxs-lookup"><span data-stu-id="85c3f-131">Return value</span></span>

<span data-ttu-id="85c3f-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="85c3f-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85c3f-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="85c3f-133">Remarks</span></span>

<span data-ttu-id="85c3f-134">Wenn der durch den  _pEID-Parameter_ angegebene Bezeichner zusammengesetzt ist, wird er in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und den Eintragsbezeichner des Speichers aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="85c3f-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="85c3f-135">Nichtkompounde Eingabebezeichnerzeichenfolgen werden einfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="85c3f-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="85c3f-136">Der zusammengesetzte Bezeichner, der getrennt werden soll, ist in der Regel eine, die von der [HrComposeEID-Funktion erstellt](hrcomposeeid.md) wird.</span><span class="sxs-lookup"><span data-stu-id="85c3f-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="85c3f-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="85c3f-137">Notes to callers</span></span>

<span data-ttu-id="85c3f-138">Der Speicher, der den  _pEID-Parameter_ enthält, wird nach erfolgreichem Abschluss dieser Funktion freigegeben.</span><span class="sxs-lookup"><span data-stu-id="85c3f-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="85c3f-139">Die aufrufende Implementierung ist für das Freispeichern von Arbeitsspeicher für die Ausgabeparameter verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="85c3f-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

