---
title: Senden von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339697"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="e37c9-103">Senden von Nachrichten mithilfe der benutzerdefinierten TNEF-Anlagenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="e37c9-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="e37c9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e37c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e37c9-105">So passen Sie die Anlagenverarbeitung beim Senden einer Nachricht an:</span><span class="sxs-lookup"><span data-stu-id="e37c9-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="e37c9-106">Rufen Sie ein TNEF-Objekt ab, indem Sie eine **IStream-Schnittstelle** und eine Nachricht an die [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="e37c9-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="e37c9-107">Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e37c9-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="e37c9-108">Verwenden [Sie IMAPIProp-Methoden,](imapipropiunknown.md) um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="e37c9-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="e37c9-109">Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt in das Messagingsystem im vom Messagingsystem benötigten Format.</span><span class="sxs-lookup"><span data-stu-id="e37c9-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="e37c9-110">Rufen Sie die [ITnef::AddProps-Methode](itnef-addprops.md) auf, um nur die Eigenschaften der Nachricht hinzuzufügen, d. h. keine der Eigenschaften für die Anlagen, indem Sie das Flag TNEF_PROP_MESSAGE_ONLY festlegen.</span><span class="sxs-lookup"><span data-stu-id="e37c9-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="e37c9-111">Rufen Sie [ITnef::AddProps](itnef-addprops.md) mit diesen Elementen auf: das TNEF_PROP_EXCLUDE-Flag, ein Eigenschaftentagarray, das die **Eigenschaft PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) enthält, und einen Anlagenbezeichner, der die zu verarbeitende Anlage angibt.</span><span class="sxs-lookup"><span data-stu-id="e37c9-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="e37c9-112">Verwenden Sie die [ITnef::SetProps-Methode,](itnef-setprops.md) um das **eigenschaftstag PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) mit einer eindeutigen Zeichenfolge hinzuzufügen, die die Anlage an das Messagingsystem identifiziert, wenn die Anlage einen Dateinamen hat, den das Messagingsystem nicht unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="e37c9-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="e37c9-113">Beispielsweise mehrere Anlagen mit demselben ursprünglichen Dateinamen oder ein Dateiname, der kein gültiger Dateiname für das Messagingsystem ist.</span><span class="sxs-lookup"><span data-stu-id="e37c9-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="e37c9-114">Diese Zeichenfolge wird mit einer Schlüsselnummer verwendet, wenn die Anlagentags in den markierten Nachrichtentext geschrieben werden, um eine Anlage ihren Daten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e37c9-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="e37c9-115">Weitere Informationen finden Sie unter [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="e37c9-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="e37c9-116">Wiederholen Sie **die AddProps-** und **SetProps-Aufrufe** für jede Anlage.</span><span class="sxs-lookup"><span data-stu-id="e37c9-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="e37c9-117">Rufen Sie die [ITnef::Finish-Methode](itnef-finish.md) auf, um die Nachricht in den TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="e37c9-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="e37c9-118">Rufen Sie den markierten Nachrichtentext ab, indem Sie die [ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e37c9-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="e37c9-119">Dieser markierte Text wird mithilfe von Methoden aus der **IStream-Schnittstelle** gelesen, mithilfe des Anlagenmodells des Messagingsystems codiert und in das Messagingsystem geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e37c9-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="e37c9-120">Rufen Sie [die IUnknown::Release-Methode auf,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) um das [ITnef-Objekt frei](itnefiunknown.md) zu geben.</span><span class="sxs-lookup"><span data-stu-id="e37c9-120">Call the [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="e37c9-121">Schreiben Sie die verbleibenden Anlagen über das Anlagenmodell des Messagingsystems in das Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="e37c9-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="e37c9-122">Ihr Transportanbieter sollte das zuvor beschriebene Verfahren verwenden, um Anlagen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e37c9-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="e37c9-123">Wenn dies nicht möglich ist, sollte der Transportanbieter die folgenden Schritte für die angepasste Anlagenverarbeitung verwenden:</span><span class="sxs-lookup"><span data-stu-id="e37c9-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="e37c9-124">Der Transportanbieter stellt sicher, **PR_ATTACH_TRANSPORT_NAME** Eigenschaften aller Anlagen eindeutige Werte enthalten, die gültige Anlagenbezeichner für das Messagingsystem sind.</span><span class="sxs-lookup"><span data-stu-id="e37c9-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="e37c9-125">Der Transportanbieter verwendet dann einen einzelnen Aufruf von **ITnef::AddProps** für jede Anlage und über TNEF_PROP_CONTAINED Flag.</span><span class="sxs-lookup"><span data-stu-id="e37c9-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

