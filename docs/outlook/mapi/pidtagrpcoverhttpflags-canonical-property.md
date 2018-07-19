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
ms.openlocfilehash: 151aa730f2ae6a4d39ffa474eb7ecd79ed5602eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794989"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="76a74-103">PidTagRpcOverHttpFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="76a74-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="76a74-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76a74-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76a74-105">Enthält die Einstellungen in einem Profil von Microsoft Office Outlook verwendet werden, um mit Microsoft Exchange Server eine Verbindung über einen Remoteprozeduraufruf (RPC) über Hypertext Transfer Protocol (HTTP).</span><span class="sxs-lookup"><span data-stu-id="76a74-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76a74-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="76a74-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76a74-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="76a74-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="76a74-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="76a74-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76a74-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="76a74-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="76a74-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="76a74-110">Data type:</span></span>  <br/> |<span data-ttu-id="76a74-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="76a74-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="76a74-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="76a74-112">Area:</span></span>  <br/> |<span data-ttu-id="76a74-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="76a74-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76a74-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76a74-114">Remarks</span></span>

<span data-ttu-id="76a74-115">Die **PR_ROH_FLAGS** -Eigenschaft wird im Abschnitt globale Profil ein Profil Messaging Application Programming Interface (MAPI) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="76a74-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="76a74-116">Der Wert der **PR_ROH_FLAGS** ist eine Bitmaske, die von einem oder mehreren der folgenden Werte bestehen.</span><span class="sxs-lookup"><span data-stu-id="76a74-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="76a74-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="76a74-117">**Name**</span></span>|<span data-ttu-id="76a74-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="76a74-118">**Value**</span></span>|<span data-ttu-id="76a74-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76a74-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="76a74-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="76a74-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="76a74-121">0 x 1</span><span class="sxs-lookup"><span data-stu-id="76a74-121">0x1</span></span>  <br/> |<span data-ttu-id="76a74-122">Verbinden Sie mit dem Exchange-Server mit RPC über HTTP.</span><span class="sxs-lookup"><span data-stu-id="76a74-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="76a74-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="76a74-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="76a74-124">0 x 2</span><span class="sxs-lookup"><span data-stu-id="76a74-124">0x2</span></span>  <br/> |<span data-ttu-id="76a74-125">Verbinden Sie mit dem Exchange-Server nur über Secure Socket Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="76a74-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="76a74-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="76a74-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="76a74-127">0 x 4</span><span class="sxs-lookup"><span data-stu-id="76a74-127">0x4</span></span>  <br/> |<span data-ttu-id="76a74-128">Sitzung gegenseitig authentifizieren beim Herstellen einer Verbindung mit SSL.</span><span class="sxs-lookup"><span data-stu-id="76a74-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="76a74-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="76a74-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="76a74-130">0 x 8</span><span class="sxs-lookup"><span data-stu-id="76a74-130">0x8</span></span>  <br/> |<span data-ttu-id="76a74-131">Bei schnellen Netzwerken zuerst eine Verbindung über HTTP.</span><span class="sxs-lookup"><span data-stu-id="76a74-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="76a74-132">Verbinden Sie dann mithilfe von TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="76a74-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="76a74-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="76a74-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="76a74-134">0 x 20</span><span class="sxs-lookup"><span data-stu-id="76a74-134">0x20</span></span>  <br/> |<span data-ttu-id="76a74-135">Bei langsamen Netzwerken zuerst eine Verbindung über HTTP.</span><span class="sxs-lookup"><span data-stu-id="76a74-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="76a74-136">Verbinden Sie dann mithilfe von TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="76a74-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="76a74-137">Beispielsweise die **PR_ROH_FLAGS** festgelegt einschalten RPC über HTTP, SSL erforderlich ist, und um anzugeben, dass das HTTP-Protokoll zuerst bei langsamer Verbindung verwendet werden soll Eigenschaftensatz-den Wert der Eigenschaft **PR_ROH_FLAGS** `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` gleich 0 x 23 ist.</span><span class="sxs-lookup"><span data-stu-id="76a74-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="76a74-138">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="76a74-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76a74-139">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="76a74-139">Protocol specifications</span></span>

<span data-ttu-id="76a74-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76a74-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76a74-141">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="76a74-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="76a74-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76a74-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76a74-143">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="76a74-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="76a74-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76a74-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76a74-145">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="76a74-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76a74-146">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="76a74-146">Header files</span></span>

<span data-ttu-id="76a74-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76a74-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="76a74-148">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="76a74-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="76a74-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="76a74-149">Mapitags.h</span></span>
  
> <span data-ttu-id="76a74-150">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="76a74-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76a74-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76a74-151">See also</span></span>



[<span data-ttu-id="76a74-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76a74-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76a74-153">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76a74-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76a74-154">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="76a74-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76a74-155">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="76a74-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

