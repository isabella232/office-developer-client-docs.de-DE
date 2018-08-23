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
ms.openlocfilehash: 335fac38ff3f084195a000ad32a27adcb85c1cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564815"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="637ca-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="637ca-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="637ca-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="637ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="637ca-105">Erstellt einen Eintrag zusammengesetzter Bezeichner für ein Objekt, das in der Regel eine Meldung in einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="637ca-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="637ca-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="637ca-106">Header file:</span></span>  <br/> |<span data-ttu-id="637ca-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="637ca-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="637ca-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="637ca-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="637ca-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="637ca-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="637ca-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="637ca-110">Called by:</span></span>  <br/> |<span data-ttu-id="637ca-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="637ca-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="637ca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="637ca-112">Parameters</span></span>

 <span data-ttu-id="637ca-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="637ca-113">_psession_</span></span>
  
> <span data-ttu-id="637ca-114">[in] Zeiger auf die Sitzung von der Clientanwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="637ca-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="637ca-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="637ca-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="637ca-116">[in] Größe des Schlüssels Datensatz des Nachrichtenspeichers aufbewahren der Nachricht oder eines anderen Objekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="637ca-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="637ca-117">Wenn 0 (null) der _PpEID_ -Parameter verweist auf eine Kopie des Eintrags-ID des Objekts in der _CbStoreRecordKey_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="637ca-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="637ca-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="637ca-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="637ca-119">[in] Zeiger auf den Eintrag Schlüssel des Nachrichtenspeichers, die die Nachricht oder eines anderen Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="637ca-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="637ca-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="637ca-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="637ca-121">[in] Größe des Eintrags-ID der Nachricht oder eines anderen Objekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="637ca-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="637ca-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="637ca-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="637ca-123">[in] Zeiger auf die Eintrags-ID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="637ca-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="637ca-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="637ca-124">_pcbEID_</span></span>
  
> <span data-ttu-id="637ca-125">[out] Zeiger auf die Größe des zurückgegebene Bezeichner in Bytes.</span><span class="sxs-lookup"><span data-stu-id="637ca-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="637ca-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="637ca-126">_ppEID_</span></span>
  
> <span data-ttu-id="637ca-127">[out] Zeiger auf einen Zeiger auf den Bezeichner des zurückgegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="637ca-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="637ca-128">Wenn der Wert des Parameters _CbStoreRecordKey_ größer als NULL ist, zeigt der _PpEID_ -Parameter auf einen Zeiger auf das zusammengesetzter Eintrags-ID, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="637ca-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="637ca-129">Wenn _CbStoreRecordKey_ gleich NULL ist, zeigt _PpEID_ auf einen Zeiger auf eine Kopie des Eintrags-ID für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="637ca-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="637ca-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="637ca-130">Return value</span></span>

<span data-ttu-id="637ca-131">None.</span><span class="sxs-lookup"><span data-stu-id="637ca-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="637ca-132">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="637ca-132">Remarks</span></span>

<span data-ttu-id="637ca-133">Wenn die Nachricht oder eines anderen Objekts für die die zusammengesetzter Eintrags-ID erstellt wird in einem Nachrichtenspeicher befindet, ist der Bezeichner aus Eintrags-ID für das Objekt und den Store-Eintrag Schlüssel erstellt.</span><span class="sxs-lookup"><span data-stu-id="637ca-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="637ca-134">Ist das Objekt nicht in einem Speicher, d. h., wird Wenn die Byteanzahl für den Store-Eintrag Schlüssel übergebenen _CbStoreRecordKey_ 0 (null) ist, ist das Objekt Eintrags-ID einfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="637ca-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="637ca-135">Die Funktion **HrComposeEID** ermöglicht, dass Anwendungen-Objekte in mehreren Informationsspeichern mithilfe von zusammengesetzten-Eintragsbezeichner entwickelt.</span><span class="sxs-lookup"><span data-stu-id="637ca-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="637ca-136">Eine Anwendung kann die [HrDecomposeEID](hrdecomposeeid.md) -Funktion, um die zusammengesetzter Eintrags-ID in seiner ursprünglichen Bestandteile aufgeteilt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="637ca-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="637ca-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="637ca-137">See also</span></span>



[<span data-ttu-id="637ca-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="637ca-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="637ca-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="637ca-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

