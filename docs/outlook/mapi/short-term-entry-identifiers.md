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
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="f7ff1-103">Kurzfristige Eintragsbezeichner</span><span class="sxs-lookup"><span data-stu-id="f7ff1-103">Short-term entry identifiers</span></span>

<span data-ttu-id="f7ff1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7ff1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7ff1-105">Eine kurzfristige Eintrags-ID wird einem Objekt von einem Dienstanbieter zugewiesen, wenn der Bezeichner schnell erstellt werden muss und nicht über die Zeit oder den Abstand zu halten ist.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="f7ff1-106">Die Eindeutigkeit einer kurzfristigen Eintrags-ID wird nur über die Lebensdauer der aktuellen Sitzung auf der aktuellen Arbeitsstation gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="f7ff1-107">NormalerWeise ist eine kurzfristige Eintrags-ID nur gültig, bis das Objekt, das es darstellt, freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="f7ff1-108">Kurzfristige Eintrags-IDs werden Zeilen in Tabellen und Einträgen in Dialogfeldern zugewiesen, in denen Daten schnell zum Browsen bereitgestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="f7ff1-109">Beispielsweise weisen Nachrichtenspeicher Anbieter kurzfristige Eintragsbezeichner zu Zeilen von Nachrichten in einer Inhaltstabelle und Empfängern in einer Recipients-Tabelle zu.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="f7ff1-110">Clients können diese kurzfristigen Eintragsbezeichner verwenden, um die Objekte zu öffnen, die von den Tabellenzeilen dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="f7ff1-111">Im Gegensatz zu langfristigen Eintrags Bezeichnern, die mit einer der openEntry \*\*\*\* -Methoden verwendet werden können, sollten jedoch kurzfristige Eintragsbezeichner mit der OpenEntry-Methode des Containers verwendet werden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f7ff1-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="f7ff1-112">Implementieren von kurzfristigen Eintrags Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="f7ff1-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="f7ff1-113">Die gängigsten Methoden zum Implementieren von kurzfristigen Eintrags-IDs sind folgende:</span><span class="sxs-lookup"><span data-stu-id="f7ff1-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="f7ff1-114">Festlegen, dass die kurzfristigen Eintragsbezeichner mit den langfristigen Bezeichnern identisch sind, sodass alle Flags nicht mehr verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="f7ff1-115">Unterscheiden sich die kurzfristigen Eintragsbezeichner von den langfristigen Bezeichnern, wobei alle Flags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="f7ff1-116">Clients können eine kurzfristige Eintrags-ID des zweiten Typs identifizieren, indem Sie das **abFlags** -Element wie folgt untersuchen:</span><span class="sxs-lookup"><span data-stu-id="f7ff1-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="f7ff1-117">Einige Dienstanbieter löschen ein oder mehrere Flags, um kurzfristige Eintragsbezeichner mit höherer Gültigkeit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="f7ff1-118">Die folgenden **abFlags** -Elemente stellen beispielsweise kurzfristige Eintragsbezeichner dar, die für mehrere Tage oder für mehrere Sitzungen verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="f7ff1-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="f7ff1-119">Clients können kurzfristige Eintrags-IDs schnell erfassen, verwenden und verwerfen.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="f7ff1-120">In den meisten Fällen können Sie auf die gleiche Weise wie langfristige Eintragsbezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="f7ff1-121">Sie können aus einer Tabelle abgerufen werden, an die **OpenEntry** -Methode übergeben und mit der **CompareEntryIDs** -Methode verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="f7ff1-122">Die einzige Ausnahme besteht darin, dass Sie nie von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7ff1-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="f7ff1-123">Die von getProps zurückgegebenen Eigenschaften sind immer langfristige Eintragsbezeichner. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f7ff1-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7ff1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7ff1-124">See also</span></span>

- [<span data-ttu-id="f7ff1-125">MAPI-Eintrags-IDs</span><span class="sxs-lookup"><span data-stu-id="f7ff1-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

