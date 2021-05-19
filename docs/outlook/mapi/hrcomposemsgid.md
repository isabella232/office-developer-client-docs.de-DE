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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424063"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="56e89-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="56e89-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="56e89-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56e89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56e89-105">Erstellt eine ASCII-Zeichenfolge, die einen zusammengesetzten Eintragsbezeichner für ein Objekt darstellt, in der Regel eine Nachricht in einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="56e89-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56e89-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="56e89-106">Header file:</span></span>  <br/> |<span data-ttu-id="56e89-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="56e89-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="56e89-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="56e89-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="56e89-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="56e89-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="56e89-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="56e89-110">Called by:</span></span>  <br/> |<span data-ttu-id="56e89-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="56e89-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="56e89-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e89-112">Parameters</span></span>

 <span data-ttu-id="56e89-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="56e89-113">_psession_</span></span>
  
> <span data-ttu-id="56e89-114">[in] Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56e89-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="56e89-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="56e89-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="56e89-116">[in] Größe des Datensatzschlüssels des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="56e89-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="56e89-117">Wenn null im  _cbStoreRecordKey-Parameter_ übergeben wird, zeigt der  _pszMsgID-Parameter_ auf eine Kopie des in Text konvertierten Eintragsbezeichners.</span><span class="sxs-lookup"><span data-stu-id="56e89-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="56e89-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="56e89-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="56e89-119">[in] Zeiger auf den Datensatzschlüssel des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="56e89-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="56e89-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="56e89-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="56e89-121">[in] Größe des Eintragsbezeichners der Nachricht oder eines anderen Objekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="56e89-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="56e89-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="56e89-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="56e89-123">[in] Zeiger auf die Eintrags-ID des Objekts.</span><span class="sxs-lookup"><span data-stu-id="56e89-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="56e89-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="56e89-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="56e89-125">[out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="56e89-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="56e89-126">Wenn der  _cbStoreRecordKey-Parameter_ größer als Null ist, zeigt der  _pszMsgID-Parameter_ auf einen zusammengesetzten Eintragsbezeichner, der in Text konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="56e89-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="56e89-127">Wenn  _cbStoreRecordKey_ null ist,  _zeigt pszMsgID_ auf einen in Text konvertierten Nichtcompound-Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="56e89-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="56e89-128">Return value</span><span class="sxs-lookup"><span data-stu-id="56e89-128">Return value</span></span>

<span data-ttu-id="56e89-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="56e89-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56e89-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56e89-130">Remarks</span></span>

<span data-ttu-id="56e89-131">Wenn sich die Nachricht oder ein anderes Objekt, für das der zusammengesetzte Eintragsbezeichner erstellt wird, in einem Nachrichtenspeicher befindet, wird die Bezeichnerzeichenfolge aus dem Eintragsbezeichner des Objekts und dem Datensatzschlüssel des Speichers erstellt.</span><span class="sxs-lookup"><span data-stu-id="56e89-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="56e89-132">Wenn sich das Objekt nicht in einem Speicher befindet, d. h. wenn die Byteanzahl für den im  _cbStoreRecordKey-Parameter_ übergebenen Speicherdatensatzschlüssel null ist, wird der Eintragsbezeichner des Objekts einfach kopiert und in eine Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="56e89-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="56e89-133">Das Aufrufen **der HrComposeMsgID-Funktion** entspricht dem Aufrufen der [HrComposeEID-Funktion](hrcomposeeid.md) und dann der [HrSzFromEntryID-Funktion.](hrszfromentryid.md)</span><span class="sxs-lookup"><span data-stu-id="56e89-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="56e89-134">**HrComposeMsgID** ermöglicht Clientanwendungen das Arbeiten mit Objekten in mehreren Speichern mithilfe von zusammengesetzten Eingabebezeichnern.</span><span class="sxs-lookup"><span data-stu-id="56e89-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="56e89-135">Eine Anwendung kann die [HrDecomposeMsgID-Funktion](hrdecomposemsgid.md) aufrufen, um die zusammengesetzte Eintrags-ID in ihre ursprünglichen Bestandteile zu teilen.</span><span class="sxs-lookup"><span data-stu-id="56e89-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

