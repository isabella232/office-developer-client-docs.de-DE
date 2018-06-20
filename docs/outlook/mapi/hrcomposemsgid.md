---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 418ffdd19412dcf948d36a5e7df33f7978d0df3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791899"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="e7988-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="e7988-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="e7988-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7988-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7988-105">Erstellt eine ASCII-Zeichenfolge, die eine zusammengesetzter Eintrags-ID für ein Objekt, das in der Regel eine Meldung in einem Nachrichtenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7988-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7988-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e7988-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7988-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e7988-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e7988-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e7988-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7988-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7988-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7988-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e7988-110">Called by:</span></span>  <br/> |<span data-ttu-id="e7988-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="e7988-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a><span data-ttu-id="e7988-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7988-112">Parameters</span></span>

 <span data-ttu-id="e7988-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="e7988-113">_psession_</span></span>
  
> <span data-ttu-id="e7988-114">[in] Zeiger auf die Sitzung von der Clientanwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7988-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="e7988-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="e7988-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="e7988-116">[in] Größe in Bytes des Schlüssels Datensatz des Nachrichtenspeichers, die die Nachricht oder eines anderen Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="e7988-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="e7988-117">Wenn 0 (null) im _CbStoreRecordKey_ -Parameter übergeben wird, wird der _PszMsgID_ Parameter verweist auf eine Kopie des Eintrags-ID in Text konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e7988-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="e7988-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="e7988-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="e7988-119">[in] Zeiger auf den Eintrag Schlüssel des Nachrichtenspeichers, die die Nachricht oder eines anderen Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="e7988-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="e7988-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="e7988-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="e7988-121">[in] Größe des Eintrags-ID der Nachricht oder eines anderen Objekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e7988-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="e7988-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="e7988-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="e7988-123">[in] Zeiger auf die Eintrags-ID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e7988-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="e7988-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="e7988-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="e7988-125">[out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e7988-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="e7988-126">Wenn der Parameter _CbStoreRecordKey_ größer als NULL ist, wird der _PszMsgID_ Parameter verweist auf ein zusammengesetzter Eintrags-ID in Text konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e7988-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="e7988-127">Wenn _CbStoreRecordKey_ gleich NULL ist, _PszMsgID_ verweist auf eine noncompound Eintrags-ID in Text konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e7988-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7988-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7988-128">Return value</span></span>

<span data-ttu-id="e7988-129">None.</span><span class="sxs-lookup"><span data-stu-id="e7988-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7988-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7988-130">Remarks</span></span>

<span data-ttu-id="e7988-131">Wenn die Nachricht oder eines anderen Objekts für die die zusammengesetzter Eintrags-ID erstellt wird, wird in einem Nachrichtenspeicher befindet, wird die Bezeichnerzeichenfolge aus Eintrags-ID für das Objekt und den Store-Eintrag Schlüssel erstellt.</span><span class="sxs-lookup"><span data-stu-id="e7988-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="e7988-132">Ist das Objekt nicht in einem Speicher, d. h., ist wenn die Byteanzahl für den Store-Eintrag Schlüssel in der _CbStoreRecordKey_ -Parameter übergeben NULL ist, ist Eintrags-ID für das Objekt einfach kopiert und in eine Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e7988-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="e7988-133">Aufrufen der Funktion **HrComposeMsgID** entspricht dem Aufrufen der [HrComposeEID](hrcomposeeid.md) und klicken Sie dann die Funktion [HrSzFromEntryID](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="e7988-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="e7988-134">**HrComposeMsgID** von Clientanwendungen-Objekte in mehreren Informationsspeichern mithilfe von zusammengesetzten-Eintragsbezeichner entwickelt.</span><span class="sxs-lookup"><span data-stu-id="e7988-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="e7988-135">Eine Anwendung kann die [HrDecomposeMsgID](hrdecomposemsgid.md) -Funktion, um die zusammengesetzter Eintrags-ID in seiner ursprünglichen Bestandteile aufgeteilt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7988-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

