---
title: MAPI-Schnittstellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e485079de800c63b02d71b3c3ccb90d66101c64b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793015"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="84fdd-103">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="84fdd-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="84fdd-104">**Gilt für**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84fdd-104">**Applies to:** Outlook \*</span></span> 
  
<span data-ttu-id="84fdd-105">Die Dokumentation für jede Schnittstelle besteht aus einem einleitenden Abschnitt, der eine kurze Beschreibung des Zwecks der Schnittstelle enthält, , gefolgt von einer Tabelle, die die folgenden Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="84fdd-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84fdd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="84fdd-106">Header file:</span></span>  <br/> |<span data-ttu-id="84fdd-107">Die Headerdatei, in der die Schnittstelle definiert ist, und die beim Kompilieren des Quellcodes einbezogen werden muss.</span><span class="sxs-lookup"><span data-stu-id="84fdd-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="84fdd-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="84fdd-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="84fdd-109">Das Objekt, das die Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="84fdd-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="84fdd-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="84fdd-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="84fdd-111">Eine Liste der Komponenten, die eine Implementierung der Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="84fdd-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="84fdd-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="84fdd-112">Called by:</span></span>  <br/> |<span data-ttu-id="84fdd-113">Eine Liste der Komponenten, die in der Regel die Methoden der Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="84fdd-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="84fdd-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="84fdd-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="84fdd-115">Die GUID des Schnittstellenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="84fdd-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="84fdd-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="84fdd-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="84fdd-117">Der Zeigertyp für das Objekt, das die Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="84fdd-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="84fdd-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="84fdd-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="84fdd-p101">Für von [IMAPIProp](imapipropiunknown.md) abgeleitete Schnittstellen. Bei �nontransacted" werden die �nderungen sofort wirksam; bei �transacted" werden die �nderungen erst wirksam, wenn [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird.  </span><span class="sxs-lookup"><span data-stu-id="84fdd-p101">For interfaces derived from [IMAPIProp](imapipropiunknown.md). If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.  </span></span><br/> |
   
<span data-ttu-id="84fdd-p102">Nach der ersten Tabelle folgt eine weitere Tabelle, in der alle Methoden dieser Schnittstelle in der vtable-Reihenfolge aufgelistet sind. Bei einer vtable handelt es sich um ein Array von Funktionszeigern, die von dem Compiler mit einem Funktionszeiger für jede Methode eines MAPI-Objekts erstellt werden. Die Methoden werden in der gleichen Reihenfolge aufgelistet, in der sie deklariert sind. Methoden, die von anderen Schnittstellen geerbt werden, sind nicht in der Tabelle in vtable-Reihenfolge dargestellt, können jedoch auf die gleiche Art und Weise verwendet werden, wie in der Schnittstelle dokumentiert, die sie definiert.</span><span class="sxs-lookup"><span data-stu-id="84fdd-p102">Following the first table is another table that lists all the methods of this interface in vtable order. A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object. The methods are listed in the same order that they are declared. Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="84fdd-p103">Nach jedem Schnittstellenthema werden dann die Methoden der Schnittstelle in alphabetischer Reihenfolge dokumentiert. Die Dokumentation umfasst für jede Methode umfasst eine kurze Beschreibung des Zwecks, einen Syntaxblock sowie die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="84fdd-p103">After each interface topic, the interface's methods are then documented in alphabetical order. For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="84fdd-127">**Überschrift**</span><span class="sxs-lookup"><span data-stu-id="84fdd-127">**Heading**</span></span>|<span data-ttu-id="84fdd-128">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="84fdd-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84fdd-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="84fdd-129">Parameters</span></span>  <br/> |<span data-ttu-id="84fdd-130">Eine Beschreibung der einzelnen Parameter in der Methode.</span><span class="sxs-lookup"><span data-stu-id="84fdd-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="84fdd-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84fdd-131">Return Value</span></span>  <br/> |<span data-ttu-id="84fdd-p104">Eine Beschreibung der eindeutigen Werte, die die Methode zurückgeben kann. Dies sind die Werte, nach denen Anrufer in ihrem Code suchen sollten.</span><span class="sxs-lookup"><span data-stu-id="84fdd-p104">A description of the unique values that the method can return. These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="84fdd-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84fdd-134">Remarks</span></span>  <br/> |<span data-ttu-id="84fdd-135">Eine Beschreibung davon, warum und wie die Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84fdd-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="84fdd-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84fdd-136">See Also</span></span>  <br/> |<span data-ttu-id="84fdd-137">Querverweise zu anderen Themen in dieser Referenz.</span><span class="sxs-lookup"><span data-stu-id="84fdd-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84fdd-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84fdd-138">See also</span></span>



[<span data-ttu-id="84fdd-139">MAPI Reference</span><span class="sxs-lookup"><span data-stu-id="84fdd-139">MAPI Reference</span></span>](mapi-reference.md)

