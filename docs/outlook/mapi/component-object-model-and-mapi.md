---
title: Component Object Model und MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cf687a7bfadb0981ca3440c2f81bc5de8f910924
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791443"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="7f8c5-103">Component Object Model und MAPI</span><span class="sxs-lookup"><span data-stu-id="7f8c5-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="7f8c5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f8c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f8c5-105">Die Windows SDK-Dokumentation umfasst eine umfassende Erläuterung der Regeln für die Implementierung von Objekten, die an Component Object Model (COM) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="7f8c5-106">Diese Regeln behandelt, wie Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="7f8c5-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="7f8c5-107">Entwerfen von Schnittstellen und Objekte.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="7f8c5-108">Implementieren Sie die [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28VS.85%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-108">Implement the [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="7f8c5-109">Arbeitsspeicher verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-109">Manage memory.</span></span>
    
- <span data-ttu-id="7f8c5-110">Behandeln Sie Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="7f8c5-111">Implementieren des Apartmentthreading-Thread-Objekte.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="7f8c5-112">Auch wenn alle Objekte der MAPI-COM-basierte betrachtet werden, da diese Schnittstellen implementieren, die von [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28VS.85%29.aspx)erben, weicht MAPI in manchen Fällen von den standard-COM-Regeln ab.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="7f8c5-113">Diese Abweichung kann Entwickler mehr Flexibilität, in deren Implementierung.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="7f8c5-114">Beispielsweise beschreibt eine MAPI-Schnittstelle wie jede COM-Schnittstelle, einen Vertrag zwischen Implementierer und des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="7f8c5-115">Nachdem die Schnittstelle erstellt und veröffentlicht wird, dessen Definition kann nicht und wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="7f8c5-116">MAPI Featureordner nicht auf diese Beschreibung, aber es etwas lockert die Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="7f8c5-117">Implementierer können keine bestimmte Methoden implementiert einen der folgenden Fehlerwerte an den Anrufer zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="7f8c5-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="7f8c5-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7f8c5-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="7f8c5-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="7f8c5-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="7f8c5-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7f8c5-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="7f8c5-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7f8c5-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="7f8c5-122">Die anderen Abweichung von den standard-COM-Regeln werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="7f8c5-123">**COM-Programmierung Regel**</span><span class="sxs-lookup"><span data-stu-id="7f8c5-123">**COM programming rule**</span></span>|<span data-ttu-id="7f8c5-124">**MAPI-Variante**</span><span class="sxs-lookup"><span data-stu-id="7f8c5-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f8c5-125">Alle Parameter in Schnittstellenmethoden sollte Unicode sein.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="7f8c5-126">MAPI-Schnittstellen sind definiert, um Unicode- oder ANSI-Parameter zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="7f8c5-127">Außerdem müssen viele Methoden, die einen Zeichenfolgenparameter haben einen Parameter **UlFlags** ; die Breite eines Parameters wird durch den Wert der die Option MAPI_UNICODE in **UlFlags**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="7f8c5-128">Einige MAPI-Schnittstellen nicht unterstützen Unicode und MAPI_E_BAD_CHARWIDTH zurück, wenn die Option MAPI_UNICODE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="7f8c5-129">Alle Schnittstellenmethoden sollte den Rückgabetyp HRESULT verfügen.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="7f8c5-130">MAPI hat mindestens eine Methode, die einen nicht-HRESULT-Wert zurückgibt: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="7f8c5-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="7f8c5-131">Anrufer und -Implementierer sollte reservieren und Speicher für die Parameter für die Benutzeroberfläche mithilfe der standardmäßigen COM-Aufgabe Allocators freigeben.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="7f8c5-132">Alle MAPI-Methoden mit der verknüpften Allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) können Speicher für die Parameter für die Benutzeroberfläche verwalten.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="7f8c5-133">Alle MAPI-Implementierungen von OLE, wie etwa [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx), definierten Schnittstellen verwenden Sie die standardmäßigen COM-Aufgabe Allocators.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="7f8c5-134">Zeigerparameter müssen ganz hin explizit auf NULL festgelegt werden, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="7f8c5-135">MAPI-Schnittstellen erfordern, dass out-Zeigerparameter, die entweder werden auf NULL festgelegt wurde, oder bleiben unverändert, wenn eine Methode, ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="7f8c5-136">Legen Sie alle MAPI-Implementierungen von OLE explizit definierten Schnittstellen out-Parameter auf NULL bei einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="7f8c5-137">Implementieren einer aggregierbaren Objekte nach Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="7f8c5-138">MAPI-Schnittstellen sind nicht aggregierbaren.</span><span class="sxs-lookup"><span data-stu-id="7f8c5-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f8c5-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f8c5-139">See also</span></span>



[<span data-ttu-id="7f8c5-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="7f8c5-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="7f8c5-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="7f8c5-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="7f8c5-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7f8c5-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="7f8c5-143">MAPI-Objekt und Übersicht über die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="7f8c5-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

