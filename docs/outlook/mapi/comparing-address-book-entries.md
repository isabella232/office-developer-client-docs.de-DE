---
title: Vergleichen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 808d5f4bfca15cae4ca7aab6758d3b5361813bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791420"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="53c64-103">Vergleichen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="53c64-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="53c64-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53c64-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53c64-105">Der Implementierung des Anbieters [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) vergleicht den Eintrag-IDs für zwei Objekte des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="53c64-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="53c64-106">MAPI ruft diese Methode auf, nachdem festgestellt wurde, dass die zwei-Eintragsbezeichner des Anbieters enthalten [MAPIUID](mapiuid.md)registriert.</span><span class="sxs-lookup"><span data-stu-id="53c64-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="53c64-107">Aus diesem Grund muss **CompareEntryIDs** -Methode nicht überprüfen, ob die für die Parameter _lpEntryID1_ und _lpEntryID2_ übergebenen Eintragsbezeichner an Ihren Anbieter gehören.</span><span class="sxs-lookup"><span data-stu-id="53c64-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="53c64-108">Aufrufen von **IABLogon::CompareEntryIDs** entspricht dem die **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))-Eigenschaft für jedes der beiden Objekte abrufen und diese direkt vergleicht.</span><span class="sxs-lookup"><span data-stu-id="53c64-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="53c64-109">**CompareEntryIds implementieren**</span><span class="sxs-lookup"><span data-stu-id="53c64-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="53c64-110">Überprüfen Sie den Typ der Eintragsbezeichner übergeben, wenn vom Dienstanbieter, die betreffenden Informationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="53c64-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="53c64-111">Beispielsweise kann eine Eintrags-ID zu einem messaging Benutzer gehören, während der anderen in einer Verteilerliste gehören möglicherweise.</span><span class="sxs-lookup"><span data-stu-id="53c64-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="53c64-112">Wenn die Typen nicht übereinstimmen, legen Sie den Inhalt des Parameters _LpulResult_ auf false festgelegt und zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="53c64-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="53c64-113">Vergleichen Sie die Größen der zwei Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="53c64-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="53c64-114">Wenn sie nicht identisch sind, legen Sie den Inhalt des Parameters _LpulResult_ auf FALSE und zurück.</span><span class="sxs-lookup"><span data-stu-id="53c64-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="53c64-115">Überprüfen Sie, dass die Größe der Eintragsbezeichner die richtige Größe für ihren Typ ist.</span><span class="sxs-lookup"><span data-stu-id="53c64-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="53c64-116">Wenn dies nicht der Fall ist, legen Sie den Inhalt des Parameters _LpulResult_ auf false fest, und geben Sie den Fehlerwert MAPI_E_UNKNOWN_ENTRYID zurück.</span><span class="sxs-lookup"><span data-stu-id="53c64-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="53c64-117">Überprüfen Sie, ob die Eintragsbezeichner identisch sind.</span><span class="sxs-lookup"><span data-stu-id="53c64-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="53c64-118">Wenn sie gleichermaßen vergleichen, den Inhalt des Parameters _LpulResult_ auf TRUE festgelegt und zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="53c64-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="53c64-119">Andernfalls ihn auf FALSE festgelegt vor der Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="53c64-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="53c64-120">Wenn der Anbieter eine kurzfristige Eintrags-ID mit einem langfristige Bezeichner verglichen wird ist, sollte sie gleichermaßen vergleichen.</span><span class="sxs-lookup"><span data-stu-id="53c64-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

