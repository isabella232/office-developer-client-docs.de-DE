---
title: Kanonische Pidtagrpcoverhttpflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327447"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="e3843-103">Kanonische Pidtagrpcoverhttpflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e3843-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e3843-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3843-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3843-105">Enthält die Einstellungen in einem Profil, das von Microsoft Office Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über Hypertext Transfer Protocol (HTTP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3843-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3843-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e3843-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3843-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e3843-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e3843-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e3843-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3843-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="e3843-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="e3843-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e3843-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3843-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e3843-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e3843-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e3843-112">Area:</span></span>  <br/> |<span data-ttu-id="e3843-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="e3843-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3843-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3843-114">Remarks</span></span>

<span data-ttu-id="e3843-115">Die **PR_ROH_FLAGS** -Eigenschaft wird im Abschnitt globaler Profil eines MAPI-Profils (Messaging Application Programming Interface) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e3843-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="e3843-116">Der Wert von **PR_ROH_FLAGS** ist eine Bitmaske, die aus einem oder mehreren der folgenden Flags besteht.</span><span class="sxs-lookup"><span data-stu-id="e3843-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="e3843-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3843-117">**Name**</span></span>|<span data-ttu-id="e3843-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e3843-118">**Value**</span></span>|<span data-ttu-id="e3843-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3843-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e3843-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="e3843-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="e3843-121">0x1</span><span class="sxs-lookup"><span data-stu-id="e3843-121">0x1</span></span>  <br/> |<span data-ttu-id="e3843-122">Stellen Sie über RPC über HTTP eine Verbindung mit dem Exchange-Server her.</span><span class="sxs-lookup"><span data-stu-id="e3843-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="e3843-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="e3843-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="e3843-124">0x2</span><span class="sxs-lookup"><span data-stu-id="e3843-124">0x2</span></span>  <br/> |<span data-ttu-id="e3843-125">Stellen Sie eine Verbindung mit dem Exchange-Server nur über Secure Sockets Layer (SSL) her.</span><span class="sxs-lookup"><span data-stu-id="e3843-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="e3843-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="e3843-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="e3843-127">0x4</span><span class="sxs-lookup"><span data-stu-id="e3843-127">0x4</span></span>  <br/> |<span data-ttu-id="e3843-128">Die Sitzung gegenseitig authentifizieren, wenn eine Verbindung über SSL hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e3843-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="e3843-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="e3843-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="e3843-130">0x8</span><span class="sxs-lookup"><span data-stu-id="e3843-130">0x8</span></span>  <br/> |<span data-ttu-id="e3843-131">Stellen Sie in schnellen Netzwerken zuerst eine Verbindung über HTTP her.</span><span class="sxs-lookup"><span data-stu-id="e3843-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="e3843-132">Stellen Sie dann eine Verbindung über TCP/IP her.</span><span class="sxs-lookup"><span data-stu-id="e3843-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="e3843-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="e3843-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="e3843-134">0x20</span><span class="sxs-lookup"><span data-stu-id="e3843-134">0x20</span></span>  <br/> |<span data-ttu-id="e3843-135">Stellen Sie in langsamen Netzwerken zuerst eine Verbindung über HTTP her.</span><span class="sxs-lookup"><span data-stu-id="e3843-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="e3843-136">Stellen Sie dann eine Verbindung über TCP/IP her.</span><span class="sxs-lookup"><span data-stu-id="e3843-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="e3843-137">Wenn Sie beispielsweise festlegen möchten, dass die **PR_ROH_FLAGS** -Eigenschaft RPC über HTTP aktivieren muss, um SSL zu erfordern, und um anzugeben, dass das HTTP-Protokoll zuerst bei langsamen Verbindungen verwendet werden soll, legen `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` Sie den Wert der **PR_ROH_FLAGS** -Eigenschaft auf, die gleich 0x23 ist.</span><span class="sxs-lookup"><span data-stu-id="e3843-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e3843-138">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e3843-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3843-139">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e3843-139">Protocol specifications</span></span>

<span data-ttu-id="e3843-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3843-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3843-141">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e3843-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3843-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3843-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3843-143">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3843-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="e3843-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3843-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3843-145">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e3843-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3843-146">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e3843-146">Header files</span></span>

<span data-ttu-id="e3843-147">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e3843-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3843-148">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e3843-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3843-149">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e3843-149">Mapitags.h</span></span>
  
> <span data-ttu-id="e3843-150">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e3843-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3843-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3843-151">See also</span></span>



[<span data-ttu-id="e3843-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3843-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3843-153">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3843-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3843-154">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e3843-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3843-155">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e3843-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

