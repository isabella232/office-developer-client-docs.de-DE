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
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="52ddc-103">COM (Component Object Model) und MAPI</span><span class="sxs-lookup"><span data-stu-id="52ddc-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="52ddc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52ddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52ddc-105">Die Windows SDK-Dokumentation enthält eine umfassende Erläuterung der Regeln für die Implementierung von Objekten, die dem Component Object Model (com) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="52ddc-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="52ddc-106">Diese Regeln behandeln Folgendes:</span><span class="sxs-lookup"><span data-stu-id="52ddc-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="52ddc-107">Entwerfen von Schnittstellen und Objekten</span><span class="sxs-lookup"><span data-stu-id="52ddc-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="52ddc-108">Implementieren Sie die [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="52ddc-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="52ddc-109">Speicher verwalten.</span><span class="sxs-lookup"><span data-stu-id="52ddc-109">Manage memory.</span></span>
    
- <span data-ttu-id="52ddc-110">Referenzzählung behandeln.</span><span class="sxs-lookup"><span data-stu-id="52ddc-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="52ddc-111">Implementieren von Apartment-threaded-Objekten.</span><span class="sxs-lookup"><span data-stu-id="52ddc-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="52ddc-112">Obwohl alle MAPI-Objekte als com-basiert betrachtet werden, da Sie Schnittstellen implementieren, die von [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)erben, weicht MAPI in einigen Situationen von den standardmäßigen com-Regeln ab.</span><span class="sxs-lookup"><span data-stu-id="52ddc-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="52ddc-113">Durch diese Abweichung können Entwickler flexibler in ihren Implementierungen sein.</span><span class="sxs-lookup"><span data-stu-id="52ddc-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="52ddc-114">Beispielsweise wird eine MAPI-Schnittstelle, wie jede com-Schnittstelle, einen Vertrag zwischen Implementierer und Aufrufer beschrieben.</span><span class="sxs-lookup"><span data-stu-id="52ddc-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="52ddc-115">Nachdem die Schnittstelle erstellt und veröffentlicht wurde, kann und wird Ihre Definition nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="52ddc-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="52ddc-116">MAPI weicht nicht von dieser Beschreibung ab, aber Sie lockert die Beschreibung etwas.</span><span class="sxs-lookup"><span data-stu-id="52ddc-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="52ddc-117">Implementierer können auswählen, dass keine bestimmten Methoden implementiert werden, wobei einer der folgenden Fehlerwerte an den Aufrufer zurückgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="52ddc-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="52ddc-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="52ddc-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="52ddc-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="52ddc-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="52ddc-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="52ddc-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="52ddc-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="52ddc-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="52ddc-122">Die anderen Abweichungen von den com-Standardregeln werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="52ddc-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="52ddc-123">**COM-Programmier Regel**</span><span class="sxs-lookup"><span data-stu-id="52ddc-123">**COM programming rule**</span></span>|<span data-ttu-id="52ddc-124">**MAPI-Variation**</span><span class="sxs-lookup"><span data-stu-id="52ddc-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52ddc-125">Alle Zeichenfolgenparameter in Schnittstellenmethoden sollten Unicode sein.</span><span class="sxs-lookup"><span data-stu-id="52ddc-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="52ddc-126">MAPI-Schnittstellen sind so definiert, dass Unicode-oder ANSI-Zeichenfolgenparameter zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="52ddc-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="52ddc-127">Viele Methoden mit einem String-Parameter haben auch einen **ulFlags** -Parameter; die Breite eines Zeichenfolgenparameters wird durch den Wert des MAPI_UNICODE-Flags in **ulFlags**angegeben.</span><span class="sxs-lookup"><span data-stu-id="52ddc-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="52ddc-128">Einige MAPI-Schnittstellen unterstützen Unicode nicht und geben MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="52ddc-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="52ddc-129">Alle Schnittstellenmethoden sollten einen Rückgabetyp HRESULT aufweisen.</span><span class="sxs-lookup"><span data-stu-id="52ddc-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="52ddc-130">MAPI verfügt über mindestens eine Methode, die einen nicht-HRESULT-Wert zurückgibt: [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="52ddc-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="52ddc-131">Anrufer und Implementierer sollten Speicher für Schnittstellenparameter mithilfe der standardmäßigen com-Aufgabenzuweisungen reservieren und freigeben.</span><span class="sxs-lookup"><span data-stu-id="52ddc-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="52ddc-132">Alle MAPI-Methoden verwenden die verknüpften Zuweisungen [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [mapifreebufferfreigegeben](mapifreebuffer.md) , um den Arbeitsspeicher für Schnittstellenparameter zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="52ddc-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="52ddc-133">Alle MAPI-Implementierungen von Schnittstellen, die durch OLE definiert sind, wie [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), verwenden die standardmäßigen com-Aufgabenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="52ddc-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="52ddc-134">Alle out-Zeigerparameter müssen explizit auf NULL festgelegt werden, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="52ddc-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="52ddc-135">MAPI-Schnittstellen erfordern, dass out-Zeigerparameter entweder auf NULL festgelegt werden oder unverändert bleiben, wenn eine Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="52ddc-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="52ddc-136">Alle MAPI-Implementierungen von Schnittstellen, die durch OLE definiert sind, legen explizit Parameter auf NULL bei einem Fehler fest.</span><span class="sxs-lookup"><span data-stu-id="52ddc-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="52ddc-137">Implementieren Sie aggregierte Objekte, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="52ddc-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="52ddc-138">MAPI-Schnittstellen sind nicht aggregiert.</span><span class="sxs-lookup"><span data-stu-id="52ddc-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52ddc-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52ddc-139">See also</span></span>



[<span data-ttu-id="52ddc-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="52ddc-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="52ddc-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="52ddc-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="52ddc-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="52ddc-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="52ddc-143">Übersicht über MAPI-Objekte und-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="52ddc-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

