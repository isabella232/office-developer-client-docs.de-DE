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
ms.openlocfilehash: 828d7ebcbceead02441165e3af92ec7b47d9f001
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564626"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="c7531-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="c7531-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="c7531-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7531-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7531-105">Trennt die ASCII-Darstellung des Bezeichners zusammengesetzter Eintrag eines Objekts in der Regel eine Meldung in einem Nachrichtenspeicher in die Eintrags-ID dieses Objekts im Speicher und den Store-Eintrags-ID an.</span><span class="sxs-lookup"><span data-stu-id="c7531-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7531-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c7531-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7531-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c7531-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c7531-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c7531-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c7531-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c7531-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c7531-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c7531-110">Called by:</span></span>  <br/> |<span data-ttu-id="c7531-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="c7531-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="c7531-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7531-112">Parameters</span></span>

 <span data-ttu-id="c7531-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="c7531-113">_psession_</span></span>
  
> <span data-ttu-id="c7531-114">[in] Zeiger auf die Sitzung von der Clientanwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7531-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="c7531-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="c7531-115">_szMsgID_</span></span>
  
> <span data-ttu-id="c7531-116">[in] Die Zeichenfolge, die Eintrags-ID des Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7531-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="c7531-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="c7531-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="c7531-118">[out] Zeiger auf die zurückgegebene Größe in Bytes für die Eintrags-ID des Nachrichtenspeichers, die das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="c7531-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="c7531-119">Wenn der Parameter _SzMsgID_ auf eine noncompound Eintrags-ID zeigt eine Zeichenfolge, klicken Sie dann _PcbStoreEID_ -Parameter verweist auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c7531-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="c7531-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="c7531-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="c7531-121">[out] Zeiger auf einen Zeiger auf das zurückgegebene Eintrags-ID des Nachrichtenspeichers, die das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="c7531-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="c7531-122">Wenn der Parameter _SzMsgID_ zu einer noncompound Eintrags-ID verweist, wird im Parameter _PpStoreEID_ NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c7531-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="c7531-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="c7531-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="c7531-124">[out] Zeiger auf die zurückgegebene Größe in Bytes für die Eintrags-ID des Objekts in seiner Store.</span><span class="sxs-lookup"><span data-stu-id="c7531-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="c7531-125">Wenn der Parameter _SzMsgID_ auf eine Zeichenfolge noncompound Eintrag zeigt, ist der Parameter _PcbMsgEID_ gleich dem Wert des Parameters _CbEID_ .</span><span class="sxs-lookup"><span data-stu-id="c7531-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="c7531-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="c7531-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="c7531-127">[out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrag Bezeichnerzeichenfolge des Objekts in seiner Store.</span><span class="sxs-lookup"><span data-stu-id="c7531-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="c7531-128">Wenn der Parameter _SzMsgID_ auf einen Bezeichner noncompound Eintrag zeigt, verweist _PpMsgEID_ auf einen Zeiger auf eine konvertierte Kopie des Bezeichners noncompound Eintrag.</span><span class="sxs-lookup"><span data-stu-id="c7531-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c7531-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7531-129">Return value</span></span>

<span data-ttu-id="c7531-130">None.</span><span class="sxs-lookup"><span data-stu-id="c7531-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7531-131">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c7531-131">Remarks</span></span>

<span data-ttu-id="c7531-132">Wenn vom _SzMsgID_ -Parameter angegebene Bezeichner zusammengesetzter ist, wird es von ASCII konvertiert und Teilen in die Eintrags-ID des Objekts in seiner Nachrichtenspeicher und den Store-Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="c7531-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="c7531-133">Noncompound Eintrags-ID-Zeichenfolgen werden einfach konvertiert und kopiert.</span><span class="sxs-lookup"><span data-stu-id="c7531-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="c7531-134">Die zusammengesetzter Bezeichnerzeichenfolge getrennt werden ist normalerweise mit der Funktion [HrComposeMsgID](hrcomposemsgid.md) erstellt.</span><span class="sxs-lookup"><span data-stu-id="c7531-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="c7531-135">Aufrufen der Funktion **HrDecomposeMsgID** entspricht dem Aufrufen der [HrEntryIDFromSz](hrentryidfromsz.md) und klicken Sie dann die Funktion [HrDecomposeEID](hrdecomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="c7531-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

