---
title: Empfangen von Nachrichten mithilfe von TNEF-Anlage benutzerdefinierte Verarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 18fc0983554284355dcdfb301fd41a0161a860fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795367"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="5fae1-103">Empfangen von Nachrichten mithilfe von TNEF-Anlage benutzerdefinierte Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="5fae1-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="5fae1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fae1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fae1-105">Um eine TNEF-Nachricht mit Anlage benutzerdefinierte Verarbeitung zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5fae1-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="5fae1-106">Importieren Sie alle Übertragungseinehit Eigenschaften – die, die das messaging-System unterstützt – aus der eingehenden Nachricht in eine neue MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5fae1-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="5fae1-107">Dies umfasst den Nachrichtentext an, der den TNEF-Datenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="5fae1-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="5fae1-108">Identifizieren Sie und Decodieren Sie spezielle Anlage, die den TNEF-Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="5fae1-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="5fae1-109">Extrahieren Sie alle Anlagen aus der eingehenden Nachricht in MAPI-Anlagen für die neue MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5fae1-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="5fae1-110">Die wiederhergestellten Dateinamen oder andere identifizierende Marker auf die Anlagen platziert werden soll in die **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))-Eigenschaft der neuen Anlagen also, die die [ITnef::ExtractProps](itnef-extractprops.md) -Methode die Anlage-Tags in den Nachrichtentext codiert können später die richtige Anlage zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5fae1-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="5fae1-111">Erstellen Sie eine OLE- **IStream** -Schnittstelle zum Umschließen des decodierten TNEF-Streams und verwenden Sie dieses Objekt zusammen mit der neuen MAPI-Nachricht in einem Aufruf der Funktion [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="5fae1-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="5fae1-112">Rufen Sie die **ITnef::ExtractProps** -Methode, um die Nontransmittable-Eigenschaften auf die Nachricht aus der TNEF-Datenstrom wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="5fae1-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="5fae1-113">Rufen Sie die [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode mit dem MAPI_CREATE ist und MAPI_MODIFY Flags.</span><span class="sxs-lookup"><span data-stu-id="5fae1-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="5fae1-114">Dieses Anrufs die Anlage-Tags aus dem Nachrichtentext entfernt und in der Anlage Positionsinformationen in der MAPI-Nachricht konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5fae1-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="5fae1-115">Die Nachricht über die MAPI-Warteschlange zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5fae1-115">Deliver the message through the MAPI spooler.</span></span>
    

