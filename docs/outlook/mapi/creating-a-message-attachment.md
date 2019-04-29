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
# <a name="creating-a-message-attachment"></a><span data-ttu-id="bc919-103">Erstellen einer Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="bc919-103">Creating a message attachment</span></span>
  
<span data-ttu-id="bc919-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc919-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc919-105">Bei einer Nachrichtenanlage handelt es sich um zusätzliche Daten wie eine Datei, eine andere Nachricht oder ein OLE-Objekt, die Sie zusammen mit einer Nachricht senden oder speichern können.</span><span class="sxs-lookup"><span data-stu-id="bc919-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="bc919-106">Jede Anlage verfügt über eine Auflistung von Eigenschaften, die Sie identifiziert und ihren Typ und ihre Darstellung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bc919-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="bc919-107">Wie Empfänger kann nur auf Nachrichtenanlagen über die Nachricht zugegriffen werden, zu der Sie gehören.</span><span class="sxs-lookup"><span data-stu-id="bc919-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="bc919-108">Damit eine Anlage verwendet werden kann, muss daher Ihre Nachricht geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="bc919-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="bc919-109">Erstellen einer Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="bc919-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="bc919-110">Rufen Sie die [IMessage:: createattach](imessage-createattach.md) -Methode der Nachricht auf, und führen Sie NULL als Schnittstellenbezeichner aus.</span><span class="sxs-lookup"><span data-stu-id="bc919-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="bc919-111">**Createattach** gibt eine Zahl zurück, die die neue Anlage in der Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bc919-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="bc919-112">Die Anlagennummer wird in der **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft gespeichert und ist nur gültig, solange die Nachricht, die die Anlage enthält, geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="bc919-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="bc919-113">Rufen Sie [IMAPIProp::](imapiprop-setprops.md) SetProps auf, um **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md)) festzulegen, um anzugeben, wie auf die Anlage zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="bc919-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="bc919-114">**PR_ATTACH_METHOD** ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc919-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="bc919-115">Legen Sie den folgenden Wert fest:</span><span class="sxs-lookup"><span data-stu-id="bc919-115">Set it to:</span></span> 
    
   - <span data-ttu-id="bc919-116">ATTACH_BY_VALUE, wenn die Anlage Binärdaten ist.</span><span class="sxs-lookup"><span data-stu-id="bc919-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="bc919-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE oder ATTACH_BY_REF_ONLY, wenn es sich bei der Anlage um eine Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="bc919-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="bc919-118">ATTACH_EMBEDDED_MSG, wenn die Anlage eine Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="bc919-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="bc919-119">ATTACH_OLE, wenn die Anlage ein OLE-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="bc919-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="bc919-120">Legen Sie die entsprechende Eigenschaft für Anlagendaten fest:</span><span class="sxs-lookup"><span data-stu-id="bc919-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="bc919-121">**PR_ATTACH_DATA_BIN** ([Pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md)) für binäre Daten und OLE 1-Objekte.</span><span class="sxs-lookup"><span data-stu-id="bc919-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="bc919-122">**PR_ATTACH_PATHNAME** ([Pidtagattachpathname (](pidtagattachpathname-canonical-property.md)) für Dateien.</span><span class="sxs-lookup"><span data-stu-id="bc919-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="bc919-123">**PR_ATTACH_DATA_OBJ** ([Pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md)) für Nachrichten und OLE 2-Objekte.</span><span class="sxs-lookup"><span data-stu-id="bc919-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="bc919-124">Legen Sie **PR_ATTACH_RENDERING** ([pidtagattachrendering (](pidtagattachrendering-canonical-property.md)) fest, um die grafische Darstellung der Anlage für Datei-oder Binäranlagen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="bc919-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="bc919-125">Legen Sie Sie nicht für OLE-Objekte fest, die die Renderinginformationen intern oder für angefügte Nachrichten speichern.</span><span class="sxs-lookup"><span data-stu-id="bc919-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="bc919-126">Legen Sie **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md)) fest, um anzugeben, wo die Anlage angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc919-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="bc919-127">**PR_RENDERING_POSITION** gilt nur für Clients, die die **PR_BODY** -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="bc919-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="bc919-128">Wenn Sie **PR_RTF_COMPRESSED**nur unterstützen, fügen Sie die folgenden Platzhalterinformationen in den komprimierten Stream ein:</span><span class="sxs-lookup"><span data-stu-id="bc919-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="bc919-129">Um **PR_RENDERING_POSITION**festzulegen, weisen Sie eine Zahl, die einen ordinalen Offset in Zeichen darstellt, wobei das erste Zeichen von **PR_BODY** 0 ist, wenn Sie wissen möchten, wo in der Nachricht die Anlage gerendert wird, oder 0xFFFFFFFF, wenn Sie nicht Render Attachments in **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="bc919-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="bc919-130">Legen Sie **PR_ATTACH_FILENAME** ([pidtagattachfilename (](pidtagattachfilename-canonical-property.md)) fest, um den Kurznamen der Datei für eine Dateianlage und eine **PR\_-ATTACH_LONG_FILENAME** ([pidtagattachlongfilename (](pidtagattachlongfilename-canonical-property.md)) anzugeben, um den Namen der unterstützten Datei anzugeben. auf einer Plattform, die das Format für lange Dateinamen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bc919-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="bc919-131">Beide Eigenschaften sind optional.</span><span class="sxs-lookup"><span data-stu-id="bc919-131">Both properties are optional.</span></span> <span data-ttu-id="bc919-132">Wenn Sie jedoch **PR_ATTACH_LONG_FILENAME**festlegen, legen Sie auch **PR_ATTACH_FILENAME**fest.</span><span class="sxs-lookup"><span data-stu-id="bc919-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="bc919-133">Legen Sie **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) fest, um den Namen für die Anlage anzugeben, die in einem Dialogfeld angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc919-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="bc919-134">PR_DISPLAY_NAME ist optional.</span><span class="sxs-lookup"><span data-stu-id="bc919-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="bc919-135">PR_ATTACH_DATA_BIN festlegen</span><span class="sxs-lookup"><span data-stu-id="bc919-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="bc919-136">Rufen Sie [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) auf, um die Eigenschaft mit der **IStream** -Schnittstelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bc919-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="bc919-137">Wenn eine Datei die Daten enthält und Sie geöffnet ist oder wenn Sie eine explizite Kontrolle über die Puffergröße benötigen, rufen Sie **IStream:: Write** in einer Schleife auf, um die Daten im Stream zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="bc919-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="bc919-138">Eine weitere Möglichkeit besteht darin, **OpenStreamOnFile** aufzurufen, um einen Stream für den Zugriff auf die Datendatei zu erstellen und dann die **IStream:: CopyTo** -Methode dieses Streams aufzurufen, um die Daten in den von **OpenProperty**zurückgegebenen Stream zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="bc919-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="bc919-139">Rufen Sie die **IStream:: Commit** -Methode des neuen Streams auf.</span><span class="sxs-lookup"><span data-stu-id="bc919-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="bc919-140">PR_ATTACH_DATA_OBJ festlegen</span><span class="sxs-lookup"><span data-stu-id="bc919-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="bc919-141">Rufen Sie **IMAPIProp:: OpenProperty** auf, um die Eigenschaft mit der **IStreamDocfile** -Schnittstelle zu öffnen, um einen Datenstrom zu erstellen, der mit strukturiertem Speicher funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bc919-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="bc919-142">**IStreamDocfile** wird von Nachrichtenspeicher Anbietern implementiert, um Clients eine leistungsstärkere Methode zum Speichern und Abrufen strukturierter Speicher bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bc919-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="bc919-143">Die **IStreamDocfile** -Schnittstelle ist mit **IStream**identisch, aber der Inhalt des Streams wird garantiert als strukturierter Speicher formatiert.</span><span class="sxs-lookup"><span data-stu-id="bc919-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="bc919-144">Wenn dieser Aufruf erfolgreich ist, erstellen Sie den Stream mit den gleichen Schritten zum Festlegen von **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="bc919-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="bc919-145">Wenn **OpenProperty** fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="bc919-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="bc919-146">Rufen \*\*\*\* Sie OpenProperty erneut an, um **IStorage**zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="bc919-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="bc919-147">Rufen Sie **StgOpenStorage** auf, um das OLE-Objekt zu öffnen und ein Storage-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc919-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="bc919-148">Rufen Sie die **IStorage:: CopyTo** -Methode des zurückgegebenen Speicherobjekts auf, um das von **OpenProperty**zurückgegebene Speicherobjekt zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="bc919-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="bc919-149">Rufen Sie die **IStorage:: Commit** -Methode des neuen Speicherobjekts auf.</span><span class="sxs-lookup"><span data-stu-id="bc919-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="bc919-150">PR_ATTACH_PATHNAME festlegen</span><span class="sxs-lookup"><span data-stu-id="bc919-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="bc919-151">Reservieren Sie eine [SPropValue](spropvalue.md) -Struktur, indem Sie das **ulPropTag** -Element auf **PR_ATTACH_PATHNAME** und den **Wert. LPSZ** -Member auf die Zeichenfolge festlegen, die den Dateinamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc919-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="bc919-152">Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Anlage auf.</span><span class="sxs-lookup"><span data-stu-id="bc919-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="bc919-153">Wenn Ihre Plattform lange Dateinamen unterstützt, legen Sie sowohl **PR_ATTACH_PATHNAME** als auch **PR_ATTACH_LONG_PATHNAME**fest.</span><span class="sxs-lookup"><span data-stu-id="bc919-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="bc919-154">Möglicherweise müssen Sie einen Betriebssystemaufruf ausführen, um den kurzen Dateinamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc919-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc919-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc919-155">See also</span></span>

- [<span data-ttu-id="bc919-156">MAPI-Anlagen</span><span class="sxs-lookup"><span data-stu-id="bc919-156">MAPI Attachments</span></span>](mapi-attachments.md)

