---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429047"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="debed-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="debed-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="debed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="debed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="debed-105">Erstellt eine verknüpfte Eintrags-ID für ein Objekt, in der Regel eine Nachricht in einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="debed-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="debed-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="debed-106">Header file:</span></span>  <br/> |<span data-ttu-id="debed-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="debed-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="debed-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="debed-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="debed-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="debed-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="debed-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="debed-110">Called by:</span></span>  <br/> |<span data-ttu-id="debed-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="debed-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a><span data-ttu-id="debed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="debed-112">Parameters</span></span>

 <span data-ttu-id="debed-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="debed-113">_psession_</span></span>
  
> <span data-ttu-id="debed-114">in Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="debed-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="debed-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="debed-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="debed-116">in Größe (in Byte) des Daten Satz Schlüssels des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt hält.</span><span class="sxs-lookup"><span data-stu-id="debed-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="debed-117">Wenn NULL im _cbStoreRecordKey_ -Parameter übergeben wird, zeigt der _ppEID_ -Parameter auf eine Kopie der Eintrags-ID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="debed-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="debed-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="debed-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="debed-119">in Zeiger auf den Datensatzschlüssel des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="debed-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="debed-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="debed-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="debed-121">in Größe (in Bytes) der Eintrags-ID der Nachricht oder eines anderen Objekts.</span><span class="sxs-lookup"><span data-stu-id="debed-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="debed-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="debed-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="debed-123">in Zeiger auf die Eintrags-ID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="debed-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="debed-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="debed-124">_pcbEID_</span></span>
  
> <span data-ttu-id="debed-125">Out Zeiger auf die Größe des zurückgegebenen Bezeichners in Byte.</span><span class="sxs-lookup"><span data-stu-id="debed-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="debed-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="debed-126">_ppEID_</span></span>
  
> <span data-ttu-id="debed-127">Out Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="debed-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="debed-128">Wenn der Wert des _cbStoreRecordKey_ -Parameters größer als NULL ist, zeigt der Parameter _ppEID_ auf einen Zeiger auf den verknüpften Eintragsbezeichner, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="debed-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="debed-129">Wenn _cbStoreRecordKey_ ist, verweist _ppEID_ auf einen Zeiger auf eine Kopie des Eintrags Bezeichners des Objekts.</span><span class="sxs-lookup"><span data-stu-id="debed-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="debed-130">Return value</span><span class="sxs-lookup"><span data-stu-id="debed-130">Return value</span></span>

<span data-ttu-id="debed-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="debed-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="debed-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="debed-132">Remarks</span></span>

<span data-ttu-id="debed-133">Wenn die Nachricht oder ein anderes Objekt, für das die verknüpfte Eintrags-ID erstellt wird, in einem Nachrichtenspeicher gespeichert ist, wird der Bezeichner aus der Eintrags-ID des Objekts und dem Record-Schlüssel des Speichers erstellt.</span><span class="sxs-lookup"><span data-stu-id="debed-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="debed-134">Wenn sich das Objekt nicht in einem Speicher befindet, das heißt, wenn die Bytezahl für den in _cbStoreRecordKey_ übergebenen Speicher Eintragsschlüssel NULL ist, wird die Eintrags-ID des Objekts einfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="debed-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="debed-135">Mit der **HrComposeEID** -Funktion können Anwendungen mit Objekten in mehreren speichern mithilfe von verknüpften Eingabe Bezeichnern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="debed-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="debed-136">Eine Anwendung kann die [HrDecomposeEID](hrdecomposeeid.md) -Funktion aufrufen, um den verknüpften Eintragsbezeichner in seine ursprünglichen Bestandteile aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="debed-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="debed-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="debed-137">See also</span></span>



[<span data-ttu-id="debed-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="debed-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="debed-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="debed-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

