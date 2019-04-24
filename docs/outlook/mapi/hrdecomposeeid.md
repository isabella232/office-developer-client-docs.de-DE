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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348069"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="7f450-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="7f450-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="7f450-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f450-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f450-105">Trennt die verknüpfte Eintrags-ID eines Objekts, in der Regel eine Nachricht in einem Nachrichtenspeicher, in der Eintrags-ID des Objekts im Speicher und der Eintrags-ID des Speichers.</span><span class="sxs-lookup"><span data-stu-id="7f450-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f450-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7f450-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f450-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="7f450-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7f450-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7f450-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7f450-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7f450-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7f450-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7f450-110">Called by:</span></span>  <br/> |<span data-ttu-id="7f450-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7f450-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7f450-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f450-112">Parameters</span></span>

 <span data-ttu-id="7f450-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="7f450-113">_psession_</span></span>
  
> <span data-ttu-id="7f450-114">in Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f450-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="7f450-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="7f450-115">_cbEID_</span></span>
  
> <span data-ttu-id="7f450-116">in Die Größe des verknüpften Eintrags Bezeichners in Byte, der getrennt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f450-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="7f450-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="7f450-117">_pEID_</span></span>
  
> <span data-ttu-id="7f450-118">in Zeiger auf die verknüpfte Eintrags-ID, die getrennt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f450-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="7f450-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="7f450-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="7f450-120">Out Zeiger auf die zurückgegebene Größe in Bytes des Eintrags Bezeichners des Nachrichtenspeichers, der das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="7f450-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="7f450-121">Wenn der _pEID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID zeigt, zeigt der _pcbStoreEID_ -Parameter auf den Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7f450-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="7f450-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="7f450-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="7f450-123">Out Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Nachrichtenspeichers, der das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="7f450-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="7f450-124">Wenn der _pEID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID verweist, wird NULL im _ppStoreEID_ -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f450-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="7f450-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="7f450-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="7f450-126">Out Zeiger auf die zurückgegebene Größe in Bytes des Eintrags Bezeichners des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7f450-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="7f450-127">Wenn der _pEID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID zeigt, ist der _pcbMsgEID_ -Parameter gleich dem Wert des _cbEID_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="7f450-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="7f450-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="7f450-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="7f450-129">Out Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7f450-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="7f450-130">Wenn der _pEID_ -Parameter auf eine nicht zusammengesetzte Eintrags-ID zeigt, verweist _ppMsgEID_ auf einen Zeiger auf eine Kopie des nicht zusammengesetzten Eintrags Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="7f450-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7f450-131">Return value</span><span class="sxs-lookup"><span data-stu-id="7f450-131">Return value</span></span>

<span data-ttu-id="7f450-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f450-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f450-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f450-133">Remarks</span></span>

<span data-ttu-id="7f450-134">Wenn der vom _pEID_ -Parameter angegebene Bezeichner Compound ist, wird er in den Eintragsbezeichner des Objekts innerhalb des Nachrichtenspeichers und die Eintrags-ID des Speichers aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="7f450-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="7f450-135">Nicht zusammengesetzte Eintrags-ID-Zeichenfolgen werden einfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="7f450-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="7f450-136">Der zusammengesetzte Bezeichner, der getrennt werden soll, wird in der Regel durch die [HrComposeEID](hrcomposeeid.md) -Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f450-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7f450-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7f450-137">Notes to callers</span></span>

<span data-ttu-id="7f450-138">Der Speicher, der den _pEID_ -Parameter enthält, wird nach erfolgreichem Abschluss dieser Funktion freigegeben.</span><span class="sxs-lookup"><span data-stu-id="7f450-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="7f450-139">Die aufrufende Implementierung ist für die Freigabe des Arbeitsspeichers für die Ausgabeparameter verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="7f450-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

