---
title: Senden von Nachrichten mithilfe von TNEF-Anlage benutzerdefinierte Verarbeitung
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 1dae8d3a7830ddbc50176ec09415457ca9fdac23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795481"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="a3698-103">Senden von Nachrichten mithilfe von TNEF-Anlage benutzerdefinierte Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="a3698-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="a3698-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3698-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3698-105">So passen Sie Anlage Verarbeitung beim Senden einer Nachricht an</span><span class="sxs-lookup"><span data-stu-id="a3698-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="a3698-106">Abrufen eines TNEF-Objekts, indem Sie eine **IStream** -Schnittstelle und eine Nachricht an die Funktion [OpenTnefStreamEx](opentnefstreamex.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="a3698-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="a3698-107">Erhalten Sie eine Liste aller definierten Eigenschaften für die Nachricht, durch die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a3698-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="a3698-108">Verwenden Sie [IMAPIProp](imapipropiunknown.md) Methoden, um alle Eigenschaften von messaging-System unterstützt auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="a3698-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="a3698-109">Schreiben Sie zu einem geeigneten Zeitpunkt diese Eigenschaften in der messaging-System im Format von messaging-System erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a3698-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="a3698-110">Rufen Sie die [ITnef::AddProps](itnef-addprops.md) -Methode, um nur die Eigenschaften für die Nachricht hinzufügen – d. h., keine der Eigenschaften auf die Anlagen – durch das TNEF_PROP_MESSAGE_ONLY-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="a3698-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="a3698-111">Rufen Sie [ITnef::AddProps](itnef-addprops.md) mit dieser Elemente: das Flag TNEF_PROP_EXCLUDE, einer Array-Eigenschaft Tag mit dem **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) Eigenschaft und einer Anlage-ID, der die Anlage zu verarbeitenden angibt.</span><span class="sxs-lookup"><span data-stu-id="a3698-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="a3698-112">Verwenden Sie die [ITnef::SetProps](itnef-setprops.md) -Methode hinzu, die die Anlage an die messaging-System gibt an, ob die Anlage ein Dateinamens hat das **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) Eigenschafts-Tag durch eine eindeutige Zeichenfolge, die die Messaging-System unterstützt nicht.</span><span class="sxs-lookup"><span data-stu-id="a3698-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="a3698-113">Beispielsweise mehrere Anlagen mit dem gleichen ursprünglichen Dateinamen oder einen Dateinamen ein, der kein gültiger Dateiname für die messaging-System ist.</span><span class="sxs-lookup"><span data-stu-id="a3698-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="a3698-114">Diese Zeichenfolge wird mit einem Schlüssel mit verwendet werden, wenn die Anlage-Tags im markierten Text schreiben, deren Daten eine Anlage zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a3698-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="a3698-115">Weitere Informationen finden Sie unter [TNEF-Tagged des Nachrichtentexts](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="a3698-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="a3698-116">Wiederholen Sie die **AddProps** und **SetProps** Anrufe für jede Anlage.</span><span class="sxs-lookup"><span data-stu-id="a3698-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="a3698-117">Rufen Sie die [ITnef::Finish](itnef-finish.md) -Methode, um die Nachricht in der TNEF-Stream codieren, nachdem alle angeforderten Eigenschaften hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a3698-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="a3698-118">Aufrufen der [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode den markierten Nachrichtentext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a3698-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="a3698-119">Dieser markierte Text wird mithilfe der Methoden aus der **IStream** -Schnittstelle, mit der messaging-System Anlage Modell codiert und in die messaging-System geschrieben gelesen.</span><span class="sxs-lookup"><span data-stu-id="a3698-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="a3698-120">Rufen Sie die [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode, um das Objekt [ITnef](itnefiunknown.md) freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a3698-120">Call the [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="a3698-121">Schreiben Sie die verbleibenden Anlagen auf die messaging-System über die messaging-System Anlage Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="a3698-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="a3698-122">Der Transportdienst sollten das oben beschriebene Verfahren auf Anlagen Prozess verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3698-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="a3698-123">Wenn dies nicht möglich ist, sollte der Adressbuchhierarchie für angepasste Anlage Verarbeitung die folgenden Schritte verwenden:</span><span class="sxs-lookup"><span data-stu-id="a3698-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="a3698-124">Der Transportdienst wird sichergestellt, dass die **PR_ATTACH_TRANSPORT_NAME** Eigenschaften aller Anlagen eindeutige Werte enthalten, die gültige Anlage Bezeichner für die messaging-System sind.</span><span class="sxs-lookup"><span data-stu-id="a3698-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="a3698-125">Der Adressbuchhierarchie verwendet einen einzigen Anruf zu **ITnef::AddProps** für jede Anlage, die in das Flag TNEF_PROP_CONTAINED übergeben.</span><span class="sxs-lookup"><span data-stu-id="a3698-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

