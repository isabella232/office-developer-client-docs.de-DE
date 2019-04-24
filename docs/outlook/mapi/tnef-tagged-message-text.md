---
title: Nachrichten Text mit TNEF-Tags
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339592"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="6ea1e-103">Nachrichten Text mit TNEF-Tags</span><span class="sxs-lookup"><span data-stu-id="6ea1e-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="6ea1e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ea1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ea1e-105">Der getaggte Nachrichtentext wird von TNEF verwendet, um die Anlagen Positionen in der übergeordneten Nachricht aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="6ea1e-106">Dies geschieht durch Hinzufügen eines Platzhalters im Nachrichtentext an der Position der Anlage.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="6ea1e-107">Dieser Platzhalter oder das Attachment-Tag beschreibt die Anlage so, dass TNEF weiß, wie die Anlage und ihre Position aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="6ea1e-108">Die Tags werden wie folgt formatiert:</span><span class="sxs-lookup"><span data-stu-id="6ea1e-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="6ea1e-109">**Objekt Titel\> und Dateiname sind Variablen mit Werten, die aus der Anlage selbst entnommen werden. \<** **\> \<**</span><span class="sxs-lookup"><span data-stu-id="6ea1e-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="6ea1e-110">In Fällen, in denen diese Werte nicht verfügbar sind, wird der Titel von TNEF basierend auf dem Anlagentyp standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="6ea1e-111">Die \*\* \<KeyNum\> \*\* -Variable enthält die Textdarstellung des Anlagen Schlüssels, der der Anlage von TNEF zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="6ea1e-112">Der Basiswert des Schlüssels wird an den [OpenTnefStreamEx](opentnefstreamex.md) -Aufruf übergeben.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="6ea1e-113">Der Basiswert darf nicht NULL sein und sollte bei jedem Aufruf von **OpenTnefStreamEx**nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="6ea1e-114">Es sollte ausreichen, Pseudozufallszahlen basierend auf der Systemzeit von beliebigen Zufallszahlengeneratoren ihrer Laufzeitbibliothek zu verwenden, sofern Sie sicherstellen, dass Sie niemals NULL sind.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="6ea1e-115">Die \*\* \<Variable Transport\> Name\*\* enthält entweder den Streamnamen, der an den [OpenTnefStreamEx](opentnefstreamex.md) -Aufruf übergeben wird, oder den Wert der **PR_ATTACH_TRANSPORT_NAME** ([pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6ea1e-116">Die **PR_ATTACH_TRANSPORT_NAME** -Eigenschaft und die \*\* \<Transport\> Name\*\* -Variable in einem Nachrichten texttag haben nichts mit dem Namen des Transportanbieters zu tun, den Sie implementieren.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="6ea1e-117">Diese Elemente stellen den Namen einer Anlage für den Transportanbieter und das Messagingsystem dar.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="6ea1e-118">Der Nachrichtentext wird gekennzeichnet, wenn ein Transportanbieter einen markierten Nachrichtentext durch Aufrufen der [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode anfordert.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="6ea1e-119">Beim Lesen aus dem markierten Textstream ersetzt TNEF das einzelne Zeichen, das sich im Nachrichtentext des in der **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md))-Eigenschaft angegebenen Index befand, durch das entsprechende Tag.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="6ea1e-120">Beim Schreiben in den getaggten Textstream prüft TNEF die eingehenden Daten nach Tags, sucht die zugehörige Anlage und ersetzt das Tag durch ein einzelnes Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="6ea1e-121">Beachten Sie, dass ein Transportanbieter mithilfe des markierten Nachrichtentexts die Positionierung von Anlagen unabhängig von den meisten am Nachrichtentext durch Messagingsysteme vorgenommenen Änderungen beibehalten kann.</span><span class="sxs-lookup"><span data-stu-id="6ea1e-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

