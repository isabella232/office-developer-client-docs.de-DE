---
title: Empfangen von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328427"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="5703e-103">Empfangen von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="5703e-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="5703e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5703e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5703e-105">So erhalten Sie eine TNEF-Nachricht mit angepasster Anlagenverarbeitung:</span><span class="sxs-lookup"><span data-stu-id="5703e-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="5703e-106">Importieren Sie alle transmitable-Eigenschaften, die vom Messagingsystem unterstützt werden, von der eingehenden Nachricht in eine neue MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5703e-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="5703e-107">Hierzu gehört der Nachrichtentext, der den TNEF-Datenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="5703e-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="5703e-108">Identifizieren und Decodieren Sie die spezielle Anlage, die den TNEF-Datenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="5703e-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="5703e-109">Extrahieren Sie alle Anlagen aus der eingehenden Nachricht in MAPI-Anlagen in der neuen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5703e-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="5703e-110">Die wiederhergestellten Dateinamen oder anderen identifizierenden Marker für die Anlagen sollten in der **PR_ATTACH_TRANSPORT_NAME** ([pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))-Eigenschaft der neuen Anlagen platziert werden, damit die [ITnef:: ExtractProps](itnef-extractprops.md) -Methode die richtige Anlage kann später mit den im Nachrichtentext codierten Anlagen Tags verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="5703e-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="5703e-111">Erstellen Sie eine OLE **IStream** -Schnittstelle, um den deCODIERTen TNEF-Stream zu umbrechen, und verwenden Sie dieses Objekt zusammen mit der neuen MAPI-Nachricht in einem Aufruf der [OpenTnefStreamEx](opentnefstreamex.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5703e-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="5703e-112">Rufen Sie die **ITnef:: ExtractProps** -Methode auf, um die nicht übertragbaren Eigenschaften für die Nachricht aus dem TNEF-Datenstrom wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="5703e-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="5703e-113">Rufen Sie die [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode auf, wobei die Flags MAPI_CREATE und MAPI_MODIFY festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5703e-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="5703e-114">Dieser Aufruf entfernt die Anlagen Tags aus dem Nachrichtentext und wandelt sie in die Informationen zur Anlagen Position in der MAPI-Nachricht um.</span><span class="sxs-lookup"><span data-stu-id="5703e-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="5703e-115">Übermitteln Sie die Nachricht über den MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="5703e-115">Deliver the message through the MAPI spooler.</span></span>
    

