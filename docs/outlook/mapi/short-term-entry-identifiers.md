---
title: Kurzfristige-Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f601971e61eb6430bef9d50b093642ee04b14044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795534"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="ca5bd-103">Kurzfristige-Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="ca5bd-103">Short-term entry identifiers</span></span>

<span data-ttu-id="ca5bd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca5bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca5bd-105">Kurzfristige Eintrags-ID wird von einem Dienstanbieter zu einem Objekt zugewiesen, wenn der Bezeichner schnell erstellt werden muss und muss nicht über die Zeit oder Abstand letzten.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="ca5bd-106">Die Eindeutigkeit von kurzfristige Eintrags-ID ist nur während der Lebensdauer der aktuellen Sitzung auf der aktuellen Arbeitsstation garantiert.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="ca5bd-107">In der Regel ist eine kurzfristige Eintrags-ID gültig nur, bis das Objekt, das es darstellt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="ca5bd-108">Kurzfristige-Eintragsbezeichner zugewiesenen auf Zeilen in Tabellen und den Einträgen in Dialogfeldern, in dem sie Daten zum Durchsuchen von schnell bereitstellen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="ca5bd-109">Beispielsweise weisen Nachricht Anbieter kurzfristige-Eintragsbezeichner an Zeilen von Nachrichten in einer Inhaltstabelle und Empfänger in einer Empfängertabelle.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="ca5bd-110">Clients können diese kurzfristige-Eintragsbezeichner verwenden, um die Zeilen der Tabelle dargestellte Objekte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="ca5bd-111">Im Gegensatz zu langfristige Eintragsbezeichner, die mit einer der Methoden **OpenEntry** verwendet werden können, sollte kurzfristige-Eintragsbezeichner mit dem Container **OpenEntry** -Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="ca5bd-112">Implementieren von kurzfristige-Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="ca5bd-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="ca5bd-113">Die am häufigsten verwendeten Methoden, um kurzfristige-Eintragsbezeichner implementieren umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ca5bd-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="ca5bd-114">Stellt die kurzfristige-Eintragsbezeichner dieselbe wie die langfristige Bezeichner, wobei alle Kennzeichen nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="ca5bd-115">Stellt die kurzfristige-Eintragsbezeichner langfristige-IDs festlegen aller die Kennzeichen anders.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="ca5bd-116">Clients können einen kurzfristigen Eintrag Bezeichner des zweiten Typs identifiziert, anhand dessen **AbFlags** Member wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ca5bd-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="ca5bd-117">Einige Dienstanbieter deaktivieren Sie ein oder mehrere Flags zum kurzfristige-Eintragsbezeichner erstellen, die größer Gültigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="ca5bd-118">Die folgenden **AbFlags** Elemente darstellen beispielsweise kurzfristige Eintragsbezeichner, die für mehrere Tage oder mehrerer Sitzungen verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="ca5bd-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="ca5bd-119">Clients schnell zu erwerben, verwenden und kurzfristige-Eintragsbezeichner verwerfen.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="ca5bd-120">In den meisten Fällen können sie die gleiche Weise wie langfristige-Eintragsbezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="ca5bd-121">Sie können aus einer Tabelle, die **OpenEntry** -Methode übergeben, und im Vergleich mit **dem Eintragsbezeichner** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="ca5bd-122">Die einzige Ausnahme ist, dass sie nie aus der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="ca5bd-123">Die Eigenschaften von **GetProps** zurückgegeben werden immer langfristige-Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="ca5bd-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca5bd-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca5bd-124">See also</span></span>

- [<span data-ttu-id="ca5bd-125">MAPI-Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="ca5bd-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

