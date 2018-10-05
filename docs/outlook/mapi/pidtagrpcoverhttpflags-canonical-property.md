---
title: PidTagRpcOverHttpFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388266"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="f36f9-103">PidTagRpcOverHttpFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f36f9-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f36f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f36f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f36f9-105">Enthält die Einstellungen in einem Profil von Microsoft Office Outlook verwendet werden, um mit Microsoft Exchange Server eine Verbindung über einen Remoteprozeduraufruf (RPC) über Hypertext Transfer Protocol (HTTP).</span><span class="sxs-lookup"><span data-stu-id="f36f9-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f36f9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f36f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f36f9-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f36f9-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f36f9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f36f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f36f9-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="f36f9-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="f36f9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f36f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="f36f9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f36f9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f36f9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f36f9-112">Area:</span></span>  <br/> |<span data-ttu-id="f36f9-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="f36f9-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f36f9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f36f9-114">Remarks</span></span>

<span data-ttu-id="f36f9-115">Die **PR_ROH_FLAGS** -Eigenschaft wird im Abschnitt globale Profil ein Profil Messaging Application Programming Interface (MAPI) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f36f9-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="f36f9-116">Der Wert der **PR_ROH_FLAGS** ist eine Bitmaske, die von einem oder mehreren der folgenden Werte bestehen.</span><span class="sxs-lookup"><span data-stu-id="f36f9-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="f36f9-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="f36f9-117">**Name**</span></span>|<span data-ttu-id="f36f9-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f36f9-118">**Value**</span></span>|<span data-ttu-id="f36f9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f36f9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f36f9-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="f36f9-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="f36f9-121">0 x 1</span><span class="sxs-lookup"><span data-stu-id="f36f9-121">0x1</span></span>  <br/> |<span data-ttu-id="f36f9-122">Verbinden Sie mit dem Exchange-Server mit RPC über HTTP.</span><span class="sxs-lookup"><span data-stu-id="f36f9-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="f36f9-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="f36f9-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="f36f9-124">0 x 2</span><span class="sxs-lookup"><span data-stu-id="f36f9-124">0x2</span></span>  <br/> |<span data-ttu-id="f36f9-125">Verbinden Sie mit dem Exchange-Server nur über Secure Socket Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="f36f9-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="f36f9-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="f36f9-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="f36f9-127">0 x 4</span><span class="sxs-lookup"><span data-stu-id="f36f9-127">0x4</span></span>  <br/> |<span data-ttu-id="f36f9-128">Sitzung gegenseitig authentifizieren beim Herstellen einer Verbindung mit SSL.</span><span class="sxs-lookup"><span data-stu-id="f36f9-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="f36f9-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="f36f9-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="f36f9-130">0 x 8</span><span class="sxs-lookup"><span data-stu-id="f36f9-130">0x8</span></span>  <br/> |<span data-ttu-id="f36f9-131">Bei schnellen Netzwerken zuerst eine Verbindung über HTTP.</span><span class="sxs-lookup"><span data-stu-id="f36f9-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="f36f9-132">Verbinden Sie dann mithilfe von TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f36f9-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="f36f9-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="f36f9-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="f36f9-134">0 x 20</span><span class="sxs-lookup"><span data-stu-id="f36f9-134">0x20</span></span>  <br/> |<span data-ttu-id="f36f9-135">Bei langsamen Netzwerken zuerst eine Verbindung über HTTP.</span><span class="sxs-lookup"><span data-stu-id="f36f9-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="f36f9-136">Verbinden Sie dann mithilfe von TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f36f9-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="f36f9-137">Beispielsweise die **PR_ROH_FLAGS** festgelegt einschalten RPC über HTTP, SSL erforderlich ist, und um anzugeben, dass das HTTP-Protokoll zuerst bei langsamer Verbindung verwendet werden soll Eigenschaftensatz-den Wert der Eigenschaft **PR_ROH_FLAGS** `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` gleich 0 x 23 ist.</span><span class="sxs-lookup"><span data-stu-id="f36f9-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f36f9-138">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f36f9-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f36f9-139">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f36f9-139">Protocol specifications</span></span>

<span data-ttu-id="f36f9-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f36f9-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f36f9-141">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f36f9-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f36f9-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f36f9-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f36f9-143">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="f36f9-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="f36f9-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f36f9-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f36f9-145">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f36f9-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f36f9-146">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f36f9-146">Header files</span></span>

<span data-ttu-id="f36f9-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f36f9-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="f36f9-148">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f36f9-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="f36f9-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f36f9-149">Mapitags.h</span></span>
  
> <span data-ttu-id="f36f9-150">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f36f9-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f36f9-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f36f9-151">See also</span></span>



[<span data-ttu-id="f36f9-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f36f9-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f36f9-153">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f36f9-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f36f9-154">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f36f9-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f36f9-155">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f36f9-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

