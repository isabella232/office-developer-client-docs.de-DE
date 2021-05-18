---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404435"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="b55e2-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="b55e2-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="b55e2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b55e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b55e2-105">Trennt die ASCII-Darstellung des zusammengesetzten Eintragsbezeichners eines Objekts , in der Regel eine Nachricht in einem Nachrichtenspeicher, in den Eintragsbezeichner dieses Objekts im Speicher und den Eintragsbezeichner des Speichers.</span><span class="sxs-lookup"><span data-stu-id="b55e2-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b55e2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b55e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="b55e2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b55e2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b55e2-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b55e2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b55e2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b55e2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b55e2-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b55e2-110">Called by:</span></span>  <br/> |<span data-ttu-id="b55e2-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="b55e2-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="b55e2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b55e2-112">Parameters</span></span>

 <span data-ttu-id="b55e2-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="b55e2-113">_psession_</span></span>
  
> <span data-ttu-id="b55e2-114">[in] Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b55e2-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="b55e2-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="b55e2-115">_szMsgID_</span></span>
  
> <span data-ttu-id="b55e2-116">[in] Die Zeichenfolge, die den Eintragsbezeichner des Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="b55e2-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="b55e2-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="b55e2-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="b55e2-118">[out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Nachrichtenspeichers, der das Objekt enthält, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b55e2-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="b55e2-119">Wenn der  _szMsgID-Parameter_ auf eine Nichtkompound-Eintrags-ID-Zeichenfolge zeigt, zeigt der  _Parameter "pcbStoreEID"_ auf Null.</span><span class="sxs-lookup"><span data-stu-id="b55e2-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="b55e2-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="b55e2-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="b55e2-121">[out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID des Nachrichtenspeichers, der das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="b55e2-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="b55e2-122">Wenn der  _parameter szMsgID_ auf einen Nichtcompound-Eintragsbezeichner verweist, wird NULL im  _ppStoreEID-Parameter_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b55e2-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="b55e2-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="b55e2-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="b55e2-124">[out] Zeiger auf die zurückgegebene Größe des Eintragsbezeichners des Objekts im Speicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b55e2-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="b55e2-125">Wenn der _parameter szMsgID_ auf eine Nichtkompound-Eintrags-ID-Zeichenfolge verweist, entspricht der _parameter "pcbMsgEID"_ dem Wert des _cbEID-Parameters._</span><span class="sxs-lookup"><span data-stu-id="b55e2-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="b55e2-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="b55e2-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="b55e2-127">[out] Zeiger auf einen Zeiger auf die zurückgegebene Eintragsbezeichnerzeichenfolge des Objekts in seinem Speicher.</span><span class="sxs-lookup"><span data-stu-id="b55e2-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="b55e2-128">Wenn der  _szMsgID-Parameter_ auf einen Nichtcompound-Eintragsbezeichner verweist, zeigt  _ppMsgEID_ auf einen Zeiger auf eine konvertierte Kopie der Nichtcompound-Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="b55e2-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b55e2-129">Return value</span><span class="sxs-lookup"><span data-stu-id="b55e2-129">Return value</span></span>

<span data-ttu-id="b55e2-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="b55e2-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b55e2-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b55e2-131">Remarks</span></span>

<span data-ttu-id="b55e2-132">Wenn der durch den  _szMsgID-Parameter_ angegebene Bezeichner zusammengesetzt ist, wird er aus ASCII konvertiert und in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und den Eintragsbezeichner des Speichers aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="b55e2-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="b55e2-133">Nichtkompounde Eingabebezeichnerzeichenfolgen werden einfach konvertiert und kopiert.</span><span class="sxs-lookup"><span data-stu-id="b55e2-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="b55e2-134">Die zu trennende Zeichenfolge für zusammengesetzte Bezeichner ist in der Regel eine, die von der [HrComposeMsgID-Funktion erstellt](hrcomposemsgid.md) wird.</span><span class="sxs-lookup"><span data-stu-id="b55e2-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="b55e2-135">Das Aufrufen **der HrDecomposeMsgID-Funktion** entspricht dem Aufrufen der [HrEntryIDFromSz-Funktion](hrentryidfromsz.md) und dann der [HrDecomposeEID-Funktion.](hrdecomposeeid.md)</span><span class="sxs-lookup"><span data-stu-id="b55e2-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

