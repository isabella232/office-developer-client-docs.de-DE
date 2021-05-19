---
title: Vergleichen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415355"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="cc606-103">Vergleichen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="cc606-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="cc606-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc606-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc606-105">Die [IABLogon::CompareEntryIDs-Implementierung](iablogon-compareentryids.md) Ihres Anbieters vergleicht die Eintragsbezeichner für zwei Objekte Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="cc606-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="cc606-106">MAPI ruft diese Methode auf, nachdem sie ermittelt haben, dass die beiden Eintragsbezeichner die registrierte [MAPIUID Ihres Anbieters enthalten.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="cc606-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="cc606-107">Daher muss die **CompareEntryIDs-Methode** nicht überprüfen, ob die eintragsbezeichner, die für die  _Parameter lpEntryID1_ und  _lpEntryID2_ übergeben werden, zu Ihrem Anbieter gehören.</span><span class="sxs-lookup"><span data-stu-id="cc606-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="cc606-108">Das **Aufrufen von IABLogon::CompareEntryIDs** entspricht dem Abrufen der **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))-Eigenschaft für jedes der beiden Objekte und dem direkten Vergleich.</span><span class="sxs-lookup"><span data-stu-id="cc606-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="cc606-109">**So implementieren Sie CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="cc606-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="cc606-110">Überprüfen Sie den Typ der übergebenen Eintragsbezeichner, wenn der Anbieter diese Informationen speichert.</span><span class="sxs-lookup"><span data-stu-id="cc606-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="cc606-111">Beispielsweise kann eine Eintrags-ID zu einem Messagingbenutzer gehören, während der andere zu einer Verteilerliste gehört.</span><span class="sxs-lookup"><span data-stu-id="cc606-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="cc606-112">Wenn die Typen nicht übereinstimmen, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE ein, und geben Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="cc606-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="cc606-113">Vergleichen Sie die Größen der beiden Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="cc606-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="cc606-114">Wenn sie nicht identisch sind, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE ein, und geben Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="cc606-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="cc606-115">Überprüfen Sie, ob die Größe der Eintragsbezeichner die richtige Größe für ihren Typ ist.</span><span class="sxs-lookup"><span data-stu-id="cc606-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="cc606-116">Wenn nicht, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE ein, und geben Sie den Fehlerwert MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="cc606-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="cc606-117">Überprüfen Sie, ob die Eintragsbezeichner identisch sind.</span><span class="sxs-lookup"><span data-stu-id="cc606-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="cc606-118">Wenn sie gleich vergleichen, legen Sie den Inhalt des  _lpulResult-Parameters_ auf TRUE und zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cc606-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="cc606-119">Legen Sie andernfalls den Wert auf FALSE, bevor Sie ihn zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cc606-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="cc606-120">Wenn Ihr Anbieter einen kurzfristigen Eintragsbezeichner mit einem langfristigen Bezeichner vergleicht, sollte er den gleichen Vergleich haben.</span><span class="sxs-lookup"><span data-stu-id="cc606-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

