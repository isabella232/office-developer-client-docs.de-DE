---
title: COM (Component Object Model) und MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334468"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="476a0-103">COM (Component Object Model) und MAPI</span><span class="sxs-lookup"><span data-stu-id="476a0-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="476a0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="476a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="476a0-105">Die Windows SDK-Dokumentation enthält eine umfassende Erläuterung der Regeln für die Implementierung von Objekten, die dem Component Object Model (COM) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="476a0-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="476a0-106">Diese Regeln behandeln die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="476a0-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="476a0-107">Entwerfen von Schnittstellen und Objekten.</span><span class="sxs-lookup"><span data-stu-id="476a0-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="476a0-108">Implementieren Sie die [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="476a0-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="476a0-109">Speicher verwalten.</span><span class="sxs-lookup"><span data-stu-id="476a0-109">Manage memory.</span></span>
    
- <span data-ttu-id="476a0-110">Referenz Zählungen behandeln.</span><span class="sxs-lookup"><span data-stu-id="476a0-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="476a0-111">Implementieren von Apartment-threaded-Objekten.</span><span class="sxs-lookup"><span data-stu-id="476a0-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="476a0-112">Obwohl alle MAPI-Objekte als COM-basiert gelten, da Sie Schnittstellen implementieren, die von [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)erben, weicht MAPI in einigen Situationen von den standardmäßigen com-Regeln ab.</span><span class="sxs-lookup"><span data-stu-id="476a0-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="476a0-113">Diese Abweichung ermöglicht Entwicklern mehr Flexibilität in ihren Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="476a0-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="476a0-114">Beispielsweise beschreibt eine MAPI-Schnittstelle, wie jede beliebige COM-Schnittstelle, einen Vertrag zwischen Implementierer und Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="476a0-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="476a0-115">Sobald die Schnittstelle erstellt und veröffentlicht wurde, kann und wird Ihre Definition nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="476a0-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="476a0-116">MAPI weicht von dieser Beschreibung nicht ab, aber es entspannt die Beschreibung etwas.</span><span class="sxs-lookup"><span data-stu-id="476a0-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="476a0-117">Implementierer können bestimmte Methoden nicht implementieren und einen der folgenden Fehlerwerte an den Aufrufer zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="476a0-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="476a0-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="476a0-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="476a0-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="476a0-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="476a0-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="476a0-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="476a0-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="476a0-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="476a0-122">Die anderen Abweichungen von den standardmäßigen COM-Regeln werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="476a0-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="476a0-123">**COM-Programmier Regel**</span><span class="sxs-lookup"><span data-stu-id="476a0-123">**COM programming rule**</span></span>|<span data-ttu-id="476a0-124">**MAPI-Variation**</span><span class="sxs-lookup"><span data-stu-id="476a0-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="476a0-125">Alle Zeichenfolgenparameter in Schnittstellenmethoden sollten Unicode sein.</span><span class="sxs-lookup"><span data-stu-id="476a0-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="476a0-126">MAPI-Schnittstellen sind so definiert, dass Unicode-oder ANSI-Zeichenfolgenparameter zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="476a0-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="476a0-127">Viele Methoden mit einem String-Parameter haben auch einen **ulFlags** -Parameter; die Breite eines String-Parameters wird durch den Wert des MAPI_UNICODE-Flags in **ulFlags**angegeben.</span><span class="sxs-lookup"><span data-stu-id="476a0-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="476a0-128">Einige MAPI-Schnittstellen unterstützen Unicode nicht und geben MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="476a0-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="476a0-129">Alle Schnittstellenmethoden sollten einen Rückgabetyp von HRESULT aufweisen.</span><span class="sxs-lookup"><span data-stu-id="476a0-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="476a0-130">MAPI verfügt über mindestens eine Methode, die einen nicht-HRESULT-Wert zurückgibt: [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="476a0-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="476a0-131">Aufrufer und Implementierer sollten Speicher für Schnittstellenparameter mithilfe der standardmäßigen COM-Aufgabenzuweisungen zuweisen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="476a0-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="476a0-132">Alle MAPI-Methoden verwenden die verknüpften Zuordnungen [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [mapifreebufferfreigegeben](mapifreebuffer.md) , um Speicher für Schnittstellenparameter zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="476a0-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="476a0-133">Alle MAPI-Implementierungen von Schnittstellen, die von OLE definiert werden, wie [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), verwenden die standardMÄßIGen com-Aufgabenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="476a0-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="476a0-134">Alle out-Zeigerparameter müssen explizit auf NULL festgelegt werden, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="476a0-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="476a0-135">MAPI-Schnittstellen erfordern, dass out-Zeigerparameter entweder auf NULL festgelegt oder unverändert bleiben, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="476a0-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="476a0-136">Alle MAPI-Implementierungen von Schnittstellen, die von OLE definiert wurden, haben bei einem Fehlschlagen explizit Parameter auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="476a0-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="476a0-137">Implementieren Sie nach Möglichkeit Aggregations Objekte.</span><span class="sxs-lookup"><span data-stu-id="476a0-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="476a0-138">MAPI-Schnittstellen sind nicht aggregierbar.</span><span class="sxs-lookup"><span data-stu-id="476a0-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="476a0-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="476a0-139">See also</span></span>



[<span data-ttu-id="476a0-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="476a0-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="476a0-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="476a0-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="476a0-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="476a0-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="476a0-143">Übersicht über MAPI-Objekte und-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="476a0-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

