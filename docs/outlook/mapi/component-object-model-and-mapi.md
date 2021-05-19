---
title: COM (Component Object Model) und MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334468"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="a71ea-103">COM (Component Object Model) und MAPI</span><span class="sxs-lookup"><span data-stu-id="a71ea-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="a71ea-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a71ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a71ea-105">Die Windows-SDK-Dokumentation enthält eine umfassende Diskussion der Regeln für die Implementierung von Objekten, die dem Component Object Model (COM) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a71ea-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="a71ea-106">Diese Regeln gehen wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="a71ea-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="a71ea-107">Entwerfen von Schnittstellen und Objekten.</span><span class="sxs-lookup"><span data-stu-id="a71ea-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="a71ea-108">Implementieren Sie [die IUnknown-Schnittstelle.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a71ea-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="a71ea-109">Verwalten des Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="a71ea-109">Manage memory.</span></span>
    
- <span data-ttu-id="a71ea-110">Behandeln der Verweiszählung.</span><span class="sxs-lookup"><span data-stu-id="a71ea-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="a71ea-111">Implementieren von Objekten mit Apartmentthread.</span><span class="sxs-lookup"><span data-stu-id="a71ea-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="a71ea-112">Obwohl alle MAPI-Objekte als COM-basiert betrachtet werden, da sie Schnittstellen implementieren, die von [IUnknown erben,](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)weicht MAPI in einigen Situationen von den standardmäßigen COM-Regeln ab.</span><span class="sxs-lookup"><span data-stu-id="a71ea-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="a71ea-113">Diese Abweichung ermöglicht Entwicklern mehr Flexibilität bei ihren Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="a71ea-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="a71ea-114">Eine MAPI-Schnittstelle beschreibt z. B. wie jede COM-Schnittstelle einen Vertrag zwischen dem Implementier und dem Anrufer.</span><span class="sxs-lookup"><span data-stu-id="a71ea-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="a71ea-115">Nachdem die Schnittstelle erstellt und veröffentlicht wurde, kann und ändert sich ihre Definition nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="a71ea-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="a71ea-116">MAPI weicht nicht von dieser Beschreibung ab, aber es lockert die Beschreibung etwas.</span><span class="sxs-lookup"><span data-stu-id="a71ea-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="a71ea-117">Implementierer können bestimmte Methoden nicht implementieren und einen der folgenden Fehlerwerte an den Aufrufer zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="a71ea-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="a71ea-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a71ea-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="a71ea-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="a71ea-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="a71ea-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a71ea-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="a71ea-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a71ea-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="a71ea-122">Die anderen Abweichungen von den standardmäßigen COM-Regeln werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a71ea-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="a71ea-123">**COM-Programmierregel**</span><span class="sxs-lookup"><span data-stu-id="a71ea-123">**COM programming rule**</span></span>|<span data-ttu-id="a71ea-124">**MAPI-Variation**</span><span class="sxs-lookup"><span data-stu-id="a71ea-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a71ea-125">Alle Zeichenfolgenparameter in Schnittstellenmethoden sollten Unicode sein.</span><span class="sxs-lookup"><span data-stu-id="a71ea-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="a71ea-126">MAPI-Schnittstellen sind so definiert, dass sie Unicode- oder ANSI-Zeichenfolgenparameter zulassen.</span><span class="sxs-lookup"><span data-stu-id="a71ea-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="a71ea-127">Viele Methoden mit einem Zeichenfolgenparameter verfügen auch über einen **ulFlags-Parameter.** die Breite eines Zeichenfolgenparameters wird durch den Wert des MAPI_UNICODE in **ulFlags angegeben.**</span><span class="sxs-lookup"><span data-stu-id="a71ea-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="a71ea-128">Einige MAPI-Schnittstellen unterstützen Unicode nicht und geben MAPI_E_BAD_CHARWIDTH zurück, wenn MAPI_UNICODE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a71ea-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="a71ea-129">Alle Schnittstellenmethoden sollten den Rückgabetyp HRESULT haben.</span><span class="sxs-lookup"><span data-stu-id="a71ea-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="a71ea-130">MAPI verfügt über mindestens eine Methode, die einen Nicht-HRESULT-Wert zurückgibt: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="a71ea-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="a71ea-131">Anrufer und Implementierer sollten mithilfe der standardmäßigen COM-Aufgabenzuweisungen Arbeitsspeicher für Schnittstellenparameter zuordnen und frei machen.</span><span class="sxs-lookup"><span data-stu-id="a71ea-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="a71ea-132">Alle MAPI-Methoden verwenden die verknüpften Zuweisungen [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) zum Verwalten des Arbeitsspeichers für Schnittstellenparameter.</span><span class="sxs-lookup"><span data-stu-id="a71ea-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="a71ea-133">Alle MAPI-Implementierungen von von OLE definierten Schnittstellen, z. B. [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)verwenden die standardmäßigen COM-Aufgabenzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="a71ea-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="a71ea-134">Alle out-Zeigerparameter müssen explizit auf NULL festgelegt werden, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a71ea-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="a71ea-135">FÜR MAPI-Schnittstellen müssen out-Zeigerparameter entweder auf NULL festgelegt oder unverändert bleiben, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a71ea-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="a71ea-136">Bei allen MAPI-Implementierungen von schnittstellen, die von OLE definiert wurden, werden die Parameter bei einem Fehler explizit auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a71ea-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="a71ea-137">Implementieren Sie nach Möglichkeit aggregierbare Objekte.</span><span class="sxs-lookup"><span data-stu-id="a71ea-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="a71ea-138">MAPI-Schnittstellen sind nicht aggregierbar.</span><span class="sxs-lookup"><span data-stu-id="a71ea-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a71ea-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a71ea-139">See also</span></span>



[<span data-ttu-id="a71ea-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a71ea-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a71ea-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="a71ea-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="a71ea-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a71ea-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="a71ea-143">Übersicht über das MAPI-Objekt und die Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a71ea-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

