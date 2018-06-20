---
title: TNEF-markierte Nachrichtentext
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bedfc0457b0de8287a4e7bc8bdf8fb57404e4fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795739"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="f3618-103">TNEF-markierte Nachrichtentext</span><span class="sxs-lookup"><span data-stu-id="f3618-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="f3618-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3618-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3618-105">Markierte des Nachrichtentexts wird von TNEF zum Anlage Positionen in der übergeordneten Nachricht zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f3618-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="f3618-106">Dies erfolgt durch ein Platzhalter im Nachrichtentext an der Position der Anlage hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f3618-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="f3618-107">Dieser Platzhalter oder ein Attachment-Tag beschreibt die Anlage in einer Weise, dass TNEF weiß, wie Sie das Attachment-Objekt und seine Position auflösen können.</span><span class="sxs-lookup"><span data-stu-id="f3618-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="f3618-108">Die Tags sind wie folgt formatiert:</span><span class="sxs-lookup"><span data-stu-id="f3618-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="f3618-109">** \<Objekt Titel\> ** und ** \<Dateinamen\> ** sind Variablen, die mit den Werten, die aus der Anlage selbst ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f3618-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="f3618-110">In Fällen, in dem diese Werte nicht verfügbar sind, wird der Titel von TNEF basierend auf den Anlagetyp übernommen.</span><span class="sxs-lookup"><span data-stu-id="f3618-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="f3618-111">Die ** \<KeyNum\> ** Variable enthält die Textdarstellung des Schlüssels Anlage, die die Anlage durch TNEF zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f3618-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="f3618-112">Der Basiswert des Schlüssels übergeben wird in den [OpenTnefStreamEx](opentnefstreamex.md) -Aufruf.</span><span class="sxs-lookup"><span data-stu-id="f3618-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="f3618-113">Der Basiswert darf nicht NULL sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx**identisch sein.</span><span class="sxs-lookup"><span data-stu-id="f3618-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="f3618-114">Es reicht, um basierend auf der Systemzeit aus den Zufallszahlengenerator Ihrer Laufzeitbibliothek bereitstellt, solange Sie sicherstellen, dass sie nie NULL sind Pseudo-Zufallszahlen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3618-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="f3618-115">Die ** \<Transport Namen\> ** Variable enthält entweder den Stream Namen in der [OpenTnefStreamEx](opentnefstreamex.md) -Anruf oder der Wert der Eigenschaft **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3618-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f3618-116">Die **PR_ATTACH_TRANSPORT_NAME** -Eigenschaft und die ** \<Transport Namen\> ** Variable in einem Text-Tag Nachricht haben nichts tun mit dem Namen des Anbieters Transport Sie implementieren.</span><span class="sxs-lookup"><span data-stu-id="f3618-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="f3618-117">Diese Elemente stellen den Namen der Anlage für den Transportdienst und messaging-System.</span><span class="sxs-lookup"><span data-stu-id="f3618-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="f3618-118">Der Nachrichtentext gekennzeichnet ist, wenn für einen markierten Text ein Transportdienstes auffordert, durch die [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f3618-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="f3618-119">Beim Lesen aus dem markierten Textstream ersetzt TNEF das einzelne Zeichen, das im Nachrichtentext im Index in der Eigenschaft **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) mit dem entsprechenden Tag bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3618-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="f3618-120">Beim Schreiben in den markierten Textstream TNEF überprüft die eingehenden Daten für Tags zugeordnete Anlage gesucht und ersetzt das Tag durch ein einzelnes Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="f3618-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="f3618-121">Beachten Sie, dass mithilfe des Nachrichtentexts markierte ein Transportdienstes die Positionierung von Anlagen unabhängig von den meisten Änderungen an den Nachrichtentext beibehalten kann von messaging-Systeme.</span><span class="sxs-lookup"><span data-stu-id="f3618-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

