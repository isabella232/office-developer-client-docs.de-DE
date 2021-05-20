---
title: Kurzfristige Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439562"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="b1588-103">Kurzfristige Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="b1588-103">Short-term entry identifiers</span></span>

<span data-ttu-id="b1588-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1588-105">Ein kurzfristiger Eintragsbezeichner wird von einem Dienstanbieter einem Objekt zugewiesen, wenn der Bezeichner schnell erstellt werden muss und nicht über zeit- oder entfernungsüber einen Bestimmten Zeitraum verfügen muss.</span><span class="sxs-lookup"><span data-stu-id="b1588-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="b1588-106">Die Eindeutigkeit eines kurzfristigen Eintragsbezeichners wird nur während der Laufzeit der aktuellen Sitzung auf der aktuellen Arbeitsstation garantiert.</span><span class="sxs-lookup"><span data-stu-id="b1588-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="b1588-107">In der Regel ist eine kurzfristige Eintrags-ID nur gültig, bis das objekt, das sie darstellt, freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1588-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="b1588-108">Kurzfristige Eintragsbezeichner werden Zeilen in Tabellen und Einträgen in Dialogfeldern zugewiesen, wo es erforderlich ist, schnell Daten für das Browsen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="b1588-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="b1588-109">Nachrichtenspeicheranbieter weisen beispielsweise Zeilen von Nachrichten in einer Inhaltstabelle und Empfängern in einer Empfängertabelle kurzfristige Eintragsbezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="b1588-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="b1588-110">Clients können diese kurzfristigen Eintragsbezeichner verwenden, um die durch die Tabellenzeilen dargestellten Objekte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b1588-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="b1588-111">Im Gegensatz zu langfristigen Eintragsbezeichnern, die mit einer der **OpenEntry-Methoden** verwendet werden können, sollten jedoch kurzfristige Eintragsbezeichner mit der **OpenEntry-Methode** des Containers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1588-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="b1588-112">Implementieren kurzfristiger Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="b1588-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="b1588-113">Die gängigsten Methoden zum Implementieren kurzfristiger Eintragsbezeichner sind:</span><span class="sxs-lookup"><span data-stu-id="b1588-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="b1588-114">Machen Sie die kurzfristigen Eintragsbezeichner mit den langfristigen Bezeichnern identisch, ohne dass alle Kennzeichen nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1588-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="b1588-115">Ändern Sie die Kurzzeiteintragsbezeichner von den langfristigen Bezeichnern, indem Sie alle Kennzeichen festlegen.</span><span class="sxs-lookup"><span data-stu-id="b1588-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="b1588-116">Clients können einen kurzfristigen Eintragsbezeichner des zweiten Typs identifizieren, indem sie sein **abFlags-Mitglied** wie folgt untersuchen:</span><span class="sxs-lookup"><span data-stu-id="b1588-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="b1588-117">Einige Dienstanbieter löschen ein oder mehrere Kennzeichen, um kurzfristige Eintragsbezeichner zu erstellen, die eine höhere Gültigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="b1588-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="b1588-118">Die folgenden **abFlags-Mitglieder** stellen beispielsweise kurzfristige Eintragsbezeichner dar, die für mehrere Tage oder für mehrere Sitzungen verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="b1588-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="b1588-119">Clients erwerben, verwenden und verwerfen schnell kurzfristige Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b1588-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="b1588-120">Sie können meist auf die gleiche Weise wie langfristige Eintragsbezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1588-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="b1588-121">Sie können aus einer Tabelle abgerufen, an die **OpenEntry-Methode** übergeben und mit der **CompareEntryIDs-Methode verglichen** werden.</span><span class="sxs-lookup"><span data-stu-id="b1588-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="b1588-122">Die einzige Ausnahme ist, dass sie nie von der [IMAPIProp::GetProps-Methode zurückgegeben](imapiprop-getprops.md) werden.</span><span class="sxs-lookup"><span data-stu-id="b1588-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="b1588-123">Die von **GetProps** zurückgegebenen Eigenschaften sind immer langfristige Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b1588-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1588-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1588-124">See also</span></span>

- [<span data-ttu-id="b1588-125">MAPI-Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="b1588-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

