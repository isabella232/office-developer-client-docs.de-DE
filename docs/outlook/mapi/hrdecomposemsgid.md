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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348090"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="e874d-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="e874d-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="e874d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e874d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e874d-105">Trennt die ASCII-Darstellung des verknüpften Eintrags Bezeichners eines Objekts, in der Regel eine Nachricht in einem Nachrichtenspeicher, in der Eintrags-ID des Objekts im Speicher und der Eintrags-ID des Speichers.</span><span class="sxs-lookup"><span data-stu-id="e874d-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e874d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e874d-106">Header file:</span></span>  <br/> |<span data-ttu-id="e874d-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e874d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e874d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e874d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e874d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e874d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e874d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e874d-110">Called by:</span></span>  <br/> |<span data-ttu-id="e874d-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e874d-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e874d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e874d-112">Parameters</span></span>

 <span data-ttu-id="e874d-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="e874d-113">_psession_</span></span>
  
> <span data-ttu-id="e874d-114">in Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e874d-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="e874d-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="e874d-115">_szMsgID_</span></span>
  
> <span data-ttu-id="e874d-116">in Die Zeichenfolge, die die Eintrags-ID des Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="e874d-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="e874d-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="e874d-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="e874d-118">Out Zeiger auf die zurückgegebene Größe in Bytes des Eintrags Bezeichners des Nachrichtenspeichers, der das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="e874d-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="e874d-119">Wenn der _szMsgID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID-Zeichenfolge verweist, zeigt der Parameter _pcbStoreEID_ auf NULL.</span><span class="sxs-lookup"><span data-stu-id="e874d-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="e874d-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="e874d-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="e874d-121">Out Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Nachrichtenspeichers, der das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="e874d-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="e874d-122">Wenn der _szMsgID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID verweist, wird NULL im _ppStoreEID_ -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e874d-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="e874d-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="e874d-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="e874d-124">Out Zeiger auf die zurückgegebene Größe in Bytes des Eintrags Bezeichners des Objekts innerhalb des Speichers.</span><span class="sxs-lookup"><span data-stu-id="e874d-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="e874d-125">Wenn der _szMsgID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID-Zeichenfolge verweist, ist der _pcbMsgEID_ -Parameter gleich dem Wert des _cbEID_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="e874d-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="e874d-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="e874d-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="e874d-127">Out Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID-Zeichenfolge des Objekts innerhalb des Speichers.</span><span class="sxs-lookup"><span data-stu-id="e874d-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="e874d-128">Wenn der _szMsgID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID zeigt, verweist _ppMsgEID_ auf einen Zeiger auf eine konvertierte Kopie des nicht verknüpften Eintrags Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="e874d-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e874d-129">Return value</span><span class="sxs-lookup"><span data-stu-id="e874d-129">Return value</span></span>

<span data-ttu-id="e874d-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="e874d-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e874d-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e874d-131">Remarks</span></span>

<span data-ttu-id="e874d-132">Wenn der durch den _szMsgID_ -Parameter angegebene Bezeichner verknüpft ist, wird er aus ASCII konvertiert und in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und des Eintrags Bezeichners des Speichers aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="e874d-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="e874d-133">Nicht zusammengesetzte Eintrags-ID-Zeichenfolgen werden einfach konvertiert und kopiert.</span><span class="sxs-lookup"><span data-stu-id="e874d-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="e874d-134">Die zu Trenn Ende Verbund Bezeichner-Zeichenfolge wird in der Regel durch die [HrComposeMsgID](hrcomposemsgid.md) -Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="e874d-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="e874d-135">Das Aufrufen der **HrDecomposeMsgID** -Funktion entspricht dem Aufrufen der [HrEntryIDFromSz](hrentryidfromsz.md) -Funktion und dann der [HrDecomposeEID](hrdecomposeeid.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e874d-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

