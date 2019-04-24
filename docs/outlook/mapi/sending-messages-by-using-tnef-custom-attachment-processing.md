---
title: Senden von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung
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
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="00e83-103">Senden von Nachrichten mit der benutzerdefinierten TNEF-Anlagenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="00e83-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="00e83-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00e83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00e83-105">So passen Sie die Anlagenverarbeitung beim Senden einer Nachricht an</span><span class="sxs-lookup"><span data-stu-id="00e83-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="00e83-106">Rufen Sie ein TNEF-Objekt ab, indem Sie eine **IStream** -Schnittstelle und eine Nachricht an die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="00e83-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="00e83-107">Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="00e83-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="00e83-108">Verwenden Sie [IMAPIProp](imapipropiunknown.md) -Methoden, um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="00e83-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="00e83-109">Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt im vom Messagingsystem erforderlichen Format in das Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="00e83-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="00e83-110">Rufen Sie die [ITnef::](itnef-addprops.md) AddProps-Methode auf, um nur die Eigenschaften der Nachricht hinzuzufügen, also keine der Eigenschaften in den Anlagen, indem Sie das TNEF_PROP_MESSAGE_ONLY-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="00e83-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="00e83-111">Rufen Sie [ITnef::](itnef-addprops.md) AddProps mit diesen Elementen auf: das TNEF_PROP_EXCLUDE-Flag, ein Property-Tag-Array, das die **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md)) enthält. -Eigenschaft und eine Anlagen-ID, die die zu verarbeitende Anlage angibt.</span><span class="sxs-lookup"><span data-stu-id="00e83-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="00e83-112">Verwenden Sie die [ITnef::](itnef-setprops.md) SetProps-Methode, um das **PR_ATTACH_TRANSPORT_NAME** ([pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))-Eigenschaftentag mit einer eindeutigen Zeichenfolge hinzuzufügen, die die Anlage des Messagingsystems identifiziert, wenn die Anlage einen Dateinamen aufweist, den die Messagingsystem kann nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="00e83-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="00e83-113">Beispielsweise mehrere Anlagen mit demselben ursprünglichen Dateinamen oder ein Dateiname, der kein gültiger Dateiname für das Messagingsystem ist.</span><span class="sxs-lookup"><span data-stu-id="00e83-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="00e83-114">Diese Zeichenfolge wird mit einer Schlüsselnummer verwendet, wenn Sie die Anlagen Tags im markierten Nachrichtentext schreiben, um eine Anlage mit Ihren Daten zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="00e83-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="00e83-115">Weitere Informationen finden Sie unter [TNEF-Tagged Nachrichten Text](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="00e83-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="00e83-116">Wiederholen \*\*\*\* Sie die AddProps-und SetProps-Aufrufe für jede Anlage. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="00e83-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="00e83-117">Rufen Sie die [ITnef:: Finish](itnef-finish.md) -Methode auf, um die Nachricht in den TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="00e83-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="00e83-118">Rufen Sie den markierten Nachrichtentext ab, indem Sie die [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="00e83-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="00e83-119">Dieser markierte Text wird mithilfe von Methoden der **IStream** -Schnittstelle gelesen, mit dem Anlagenmodell des Messagingsystems codiert und an das Messagingsystem geschrieben.</span><span class="sxs-lookup"><span data-stu-id="00e83-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="00e83-120">Rufen Sie die [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode auf, um das [ITnef](itnefiunknown.md) -Objekt freigegeben.</span><span class="sxs-lookup"><span data-stu-id="00e83-120">Call the [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="00e83-121">Schreiben Sie die verbleibenden Anlagen über das Anlagenmodell des Messagingsystems an das Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="00e83-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="00e83-122">Der Transportanbieter sollte das zuvor beschriebene Verfahren zum Verarbeiten von Anlagen verwenden.</span><span class="sxs-lookup"><span data-stu-id="00e83-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="00e83-123">Wenn dies nicht möglich ist, sollte der Transportanbieter die folgenden Schritte für die angepasste Anlagenverarbeitung ausführen:</span><span class="sxs-lookup"><span data-stu-id="00e83-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="00e83-124">Der Transportanbieter stellt sicher, dass die **PR_ATTACH_TRANSPORT_NAME** -Eigenschaften aller Anlagen eindeutige Werte enthalten, die gültige Anlagen-IDs für das Messagingsystem sind.</span><span class="sxs-lookup"><span data-stu-id="00e83-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="00e83-125">Der Transportanbieter verwendet dann einen einzelnen Aufruf von **ITnef::** AddProps für jede Anlage, wobei das TNEF_PROP_CONTAINED-Flag übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="00e83-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

