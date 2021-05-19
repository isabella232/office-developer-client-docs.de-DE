---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424259"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="8e020-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8e020-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="8e020-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e020-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e020-105">Vergleicht zwei Eintragsbezeichner, die zu einem bestimmten Adressbuchanbieter gehören, um zu bestimmen, ob sie auf dasselbe Adressbuchobjekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="8e020-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="8e020-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e020-106">Parameters</span></span>

 <span data-ttu-id="8e020-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="8e020-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="8e020-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID1-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="8e020-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="8e020-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="8e020-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="8e020-110">[in] Ein Zeiger auf die erste Zutritts-ID, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e020-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="8e020-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="8e020-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="8e020-112">[in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEntryID2-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="8e020-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="8e020-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="8e020-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="8e020-114">[in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e020-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="8e020-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e020-115">_ulFlags_</span></span>
  
> <span data-ttu-id="8e020-116">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="8e020-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8e020-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="8e020-117">_lpulResult_</span></span>
  
> <span data-ttu-id="8e020-118">[out] Ein Zeiger auf das Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="8e020-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="8e020-119">Der Inhalt von  _lpulResult_ wird auf TRUE festgelegt, wenn sich die beiden Eintragsbezeichner auf dasselbe Objekt beziehen. Andernfalls wird der Inhalt auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e020-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e020-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e020-120">Return value</span></span>

<span data-ttu-id="8e020-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e020-121">S_OK</span></span> 
  
> <span data-ttu-id="8e020-122">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8e020-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8e020-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8e020-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="8e020-124">Eine oder beide der mit den  _Parametern lpEntryID1_ oder  _lpEntryID2 übergebenen_ Eintragsbezeichner werden von keinem Adressbuchanbieter erkannt.</span><span class="sxs-lookup"><span data-stu-id="8e020-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8e020-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e020-125">Remarks</span></span>

<span data-ttu-id="8e020-126">Clientanwendungen und Dienstanbieter rufen die **CompareEntryIDs-Methode** auf, um zwei Eintragsbezeichner zu vergleichen, die zu einem einzigen Adressbuchanbieter gehören, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="8e020-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="8e020-127">**CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="8e020-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="8e020-128">Diese Situation kann z. B. auftreten, nachdem eine neue Version eines Adressbuchanbieters installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8e020-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="8e020-129">MAPI übergibt diesen Aufruf an den Adressbuchanbieter, der für die Eintragsbezeichner zuständig ist, und ermittelt den entsprechenden Anbieter, indem die [MAPIUID-Struktur](mapiuid.md) in den Eintragsbezeichnern mit der vom Anbieter registrierten **MAPIUID-Struktur** übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8e020-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="8e020-130">Wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, legt **CompareEntryIDs** den Inhalt des  _lpulResult-Parameters_ auf TRUE fest. Wenn sie auf verschiedene Objekte verweisen, **legt CompareEntryIDs** den Inhalt auf FALSE fest.</span><span class="sxs-lookup"><span data-stu-id="8e020-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="8e020-131">In beiden Fällen gibt **CompareEntryIDs** S_OK.</span><span class="sxs-lookup"><span data-stu-id="8e020-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="8e020-132">Wenn **CompareEntryIDs** einen Fehler zurückgibt, der auftreten kann, wenn kein Adressbuchanbieter eine **MAPIUID-Struktur** registriert hat, die der in den Eintragsbezeichnern entspricht, sollten Clients und Anbieter keine Aktion basierend auf dem Ergebnis des Vergleichs ergreifen.</span><span class="sxs-lookup"><span data-stu-id="8e020-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="8e020-133">Sie sollten stattdessen den konservativsten Ansatz für die ausgeführte Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e020-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e020-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e020-134">See also</span></span>



[<span data-ttu-id="8e020-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8e020-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

