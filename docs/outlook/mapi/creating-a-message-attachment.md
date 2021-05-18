---
title: Erstellen einer Nachrichtenanlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405996"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="df055-103">Erstellen einer Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="df055-103">Creating a message attachment</span></span>
  
<span data-ttu-id="df055-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df055-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df055-105">Bei einer Nachrichtenanlage handelt es sich um einige zusätzliche Daten, z. B. eine Datei, eine andere Nachricht oder ein OLE-Objekt, die Sie zusammen mit einer Nachricht senden oder speichern können.</span><span class="sxs-lookup"><span data-stu-id="df055-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="df055-106">Jede Anlage verfügt über eine Auflistung von Eigenschaften, die sie identifiziert und den Typ und die Art des Renderns beschreibt.</span><span class="sxs-lookup"><span data-stu-id="df055-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="df055-107">Wie Empfänger können Nachrichtenanlagen nur über die Nachricht zugegriffen werden, zu der sie gehören.</span><span class="sxs-lookup"><span data-stu-id="df055-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="df055-108">Damit eine Anlage verwendet werden kann, muss ihre Nachricht daher geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="df055-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="df055-109">Erstellen einer Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="df055-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="df055-110">Rufen Sie die [IMessage::CreateAttach-Methode](imessage-createattach.md) der Nachricht auf, und übergeben Sie NULL als Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="df055-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="df055-111">**CreateAttach** gibt eine Zahl zurück, die die neue Anlage innerhalb der Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="df055-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="df055-112">Die Anlagennummer wird in der **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft gespeichert und ist nur gültig, solange die Nachricht mit der Anlage geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="df055-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="df055-113">Rufen [Sie IMAPIProp::SetProps](imapiprop-setprops.md) auf, um **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) zu legen, um anzugeben, wie auf die Anlage zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="df055-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="df055-114">**PR_ATTACH_METHOD** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="df055-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="df055-115">Legen Sie es auf:</span><span class="sxs-lookup"><span data-stu-id="df055-115">Set it to:</span></span> 
    
   - <span data-ttu-id="df055-116">ATTACH_BY_VALUE, wenn es sich bei der Anlage um Binärdaten handelt.</span><span class="sxs-lookup"><span data-stu-id="df055-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="df055-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE oder ATTACH_BY_REF_ONLY, wenn es sich bei der Anlage um eine Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="df055-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="df055-118">ATTACH_EMBEDDED_MSG, wenn es sich bei der Anlage um eine Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="df055-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="df055-119">ATTACH_OLE, wenn es sich bei der Anlage um ein OLE-Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="df055-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="df055-120">Legen Sie die entsprechende Anlagedateneigenschaft auf:</span><span class="sxs-lookup"><span data-stu-id="df055-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="df055-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) für Binärdaten und OLE 1-Objekte.</span><span class="sxs-lookup"><span data-stu-id="df055-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="df055-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) für Dateien.</span><span class="sxs-lookup"><span data-stu-id="df055-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="df055-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) für Nachrichten und OLE 2-Objekte.</span><span class="sxs-lookup"><span data-stu-id="df055-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="df055-124">Legen **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) fest, um die grafische Darstellung der Anlage für Datei- oder binäre Anlagen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="df055-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="df055-125">Legen Sie sie nicht für OLE-Objekte fest, die die Renderinginformationen intern speichern, oder für angefügte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="df055-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="df055-126">Legen **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) fest, um anzugeben, wo die Anlage angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="df055-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="df055-127">**PR_RENDERING_POSITION** gilt nur für Clients, die die PR_BODY **festlegen.**</span><span class="sxs-lookup"><span data-stu-id="df055-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="df055-128">Wenn Sie nur **PR_RTF_COMPRESSED** unterstützen, platzieren Sie die folgenden Platzhalterinformationen im komprimierten Datenstrom:</span><span class="sxs-lookup"><span data-stu-id="df055-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="df055-129">Weisen Sie zum Festlegen von **PR_RENDERING_POSITION** entweder eine Zahl zu, die einen Ordnungsversatz in Zeichen darstellt, wobei das erste Zeichen von **PR_BODY** 0 ist, wenn Sie wissen müssen, wo in der Nachricht die Anlage gerendert wird, oder 0xFFFFFFFF, wenn Sie Anlagen nicht innerhalb von **PR_BODY rendern.**</span><span class="sxs-lookup"><span data-stu-id="df055-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="df055-130">Legen Sie **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) fest, um den kurzen Namen der Datei für eine Dateianlage und **PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) anzugeben, um den Namen der Datei anzugeben, der auf einer Plattform unterstützt wird, die das lange Dateinamenformat verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="df055-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="df055-131">Beide Eigenschaften sind optional.</span><span class="sxs-lookup"><span data-stu-id="df055-131">Both properties are optional.</span></span> <span data-ttu-id="df055-132">Wenn Sie jedoch **PR_ATTACH_LONG_FILENAME** festlegen, legen Sie auch **PR_ATTACH_FILENAME.**</span><span class="sxs-lookup"><span data-stu-id="df055-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="df055-133">Legen **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) fest, um den Namen der Anlage anzugeben, die in einem Dialogfeld angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="df055-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="df055-134">PR_DISPLAY_NAME ist optional.</span><span class="sxs-lookup"><span data-stu-id="df055-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-pr_attach_data_bin"></a><span data-ttu-id="df055-135">Festlegen PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="df055-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="df055-136">Rufen [Sie IMAPIProp::OpenProperty auf,](imapiprop-openproperty.md) um die Eigenschaft mit der **IStream-Schnittstelle zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="df055-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="df055-137">Wenn eine Datei die Daten enthält und geöffnet ist oder Wenn Sie explizite Kontrolle über die Puffergröße benötigen, rufen Sie **IStream::Write** in einer Schleife auf, um die Daten in den Datenstrom zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="df055-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="df055-138">Eine weitere Option ist das Aufrufen von **OpenStreamOnFile** zum Erstellen eines Datenstroms für den Zugriff auf die Datendatei und anschließendes Aufrufen der **IStream::CopyTo-Methode** dieses Datenstroms, um die Daten in den von **OpenProperty** zurückgegebenen Datenstrom zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="df055-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="df055-139">Rufen Sie die **IStream::Commit-Methode des neuen Datenstroms** auf.</span><span class="sxs-lookup"><span data-stu-id="df055-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-pr_attach_data_obj"></a><span data-ttu-id="df055-140">Festlegen PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="df055-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="df055-141">Rufen **Sie IMAPIProp::OpenProperty auf,** um die Eigenschaft mit der **IStreamDocfile-Schnittstelle** zu öffnen, um einen Datenstrom zu erstellen, der mit strukturiertem Speicher funktioniert.</span><span class="sxs-lookup"><span data-stu-id="df055-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="df055-142">**IStreamDocfile** wird von Nachrichtenspeicheranbietern implementiert, um Clients eine bessere Leistung zum Speichern und Abrufen von strukturiertem Speicher zu bieten.</span><span class="sxs-lookup"><span data-stu-id="df055-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="df055-143">Die **IStreamDocfile-Schnittstelle** ist mit **IStream** identisch, aber der Inhalt des Datenstroms wird garantiert als strukturierter Speicher formatiert.</span><span class="sxs-lookup"><span data-stu-id="df055-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="df055-144">Wenn dieser Aufruf erfolgreich ist, erstellen Sie den Datenstrom mit den gleichen Schritten, die für das Festlegen von **PR_ATTACH_DATA_BIN.**</span><span class="sxs-lookup"><span data-stu-id="df055-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="df055-145">Wenn **OpenProperty fehlschlägt:**</span><span class="sxs-lookup"><span data-stu-id="df055-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="df055-146">Rufen **Sie OpenProperty** erneut auf, und fordern **Sie IStorage an.**</span><span class="sxs-lookup"><span data-stu-id="df055-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="df055-147">Rufen **Sie StgOpenStorage auf,** um das OLE-Objekt zu öffnen und ein Speicherobjekt zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="df055-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="df055-148">Rufen Sie die **IStorage::CopyTo-Methode** des zurückgegebenen Speicherobjekts auf, um in das von OpenProperty zurückgegebene **Speicherobjekt zu kopieren.**</span><span class="sxs-lookup"><span data-stu-id="df055-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="df055-149">Rufen Sie die **IStorage::Commit-Methode** des neuen Speicherobjekts auf.</span><span class="sxs-lookup"><span data-stu-id="df055-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-pr_attach_pathname"></a><span data-ttu-id="df055-150">Festlegen PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="df055-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="df055-151">Weisen Sie [eine SPropValue-Struktur](spropvalue.md) zu, und setzen Sie das **element ulPropTag** auf **PR_ATTACH_PATHNAME** und das **Value.LPSZ-Element** auf die Zeichenzeichenfolge, die den Dateinamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="df055-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="df055-152">Rufen Sie die [IMAPIProp::SetProps-Methode der Anlage](imapiprop-setprops.md) auf.</span><span class="sxs-lookup"><span data-stu-id="df055-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="df055-153">Wenn Ihre Plattform lange Dateinamen unterstützt, legen Sie sowohl PR_ATTACH_PATHNAME **als** auch **PR_ATTACH_LONG_PATHNAME.**</span><span class="sxs-lookup"><span data-stu-id="df055-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="df055-154">Möglicherweise muss ein Betriebssystemaufruf ausgeführt werden, um den kurzen Dateinamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="df055-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df055-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df055-155">See also</span></span>

- [<span data-ttu-id="df055-156">MAPI-Anlagen</span><span class="sxs-lookup"><span data-stu-id="df055-156">MAPI Attachments</span></span>](mapi-attachments.md)

