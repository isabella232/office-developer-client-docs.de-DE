---
title: Erstellen von e-Mail-Anlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eef42a8c7d19af313316bea68624ac67fb1ab4e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791489"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="68be0-103">Erstellen von e-Mail-Anlagen</span><span class="sxs-lookup"><span data-stu-id="68be0-103">Creating a message attachment</span></span>
  
<span data-ttu-id="68be0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68be0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68be0-105">E-Mail-Anlagen ist einige zusätzlichen Daten enthält, wie eine Datei, eine andere Nachricht oder ein OLE-Objekt, die zusammen mit einer Nachricht speichern oder senden können.</span><span class="sxs-lookup"><span data-stu-id="68be0-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="68be0-106">Jede Anlage ist eine Auflistung von Eigenschaften, die diese identifiziert und beschreibt dieses Typs und wie es gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="68be0-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="68be0-107">Wie Empfänger können e-Mail-Anlagen nur über die Nachricht zugegriffen werden, die sie angehören.</span><span class="sxs-lookup"><span data-stu-id="68be0-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="68be0-108">Aus diesem Grund muss für die Anlage verwendet werden, dessen Nachricht geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="68be0-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="68be0-109">Erstellen von e-Mail-Anlagen</span><span class="sxs-lookup"><span data-stu-id="68be0-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="68be0-110">Rufen Sie die Nachricht [IMessage::CreateAttach](imessage-createattach.md) -Methode, und übergeben Sie NULL als Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="68be0-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="68be0-111">**CreateAttach** gibt eine Zahl, die die neue Anlage in der Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="68be0-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="68be0-112">Die Anzahl der Anlage wird in der Eigenschaft **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) gespeichert und gilt nur, solange die Nachricht mit Anlage geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="68be0-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="68be0-113">Rufen Sie [IMAPIProp::SetProps](imapiprop-setprops.md) , um **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), um anzugeben, wie Sie Zugriff auf die Anlage festzulegen.</span><span class="sxs-lookup"><span data-stu-id="68be0-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="68be0-114">**PR_ATTACH_METHOD** ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="68be0-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="68be0-115">Legen Sie es auf:</span><span class="sxs-lookup"><span data-stu-id="68be0-115">Set it to:</span></span> 
    
   - <span data-ttu-id="68be0-116">ATTACH_BY_VALUE, wenn die Anlage Binärdaten ist.</span><span class="sxs-lookup"><span data-stu-id="68be0-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="68be0-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE oder ATTACH_BY_REF_ONLY, wenn die Anlage eine Datei ist.</span><span class="sxs-lookup"><span data-stu-id="68be0-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="68be0-118">ATTACH_EMBEDDED_MSG, wenn die Anlage einer Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="68be0-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="68be0-119">ATTACH_OLE, wenn die Anlage ein OLE-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="68be0-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="68be0-120">Legen Sie die entsprechende Anlage Data-Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="68be0-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="68be0-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) für binäre Daten und OLE-1-Objekte.</span><span class="sxs-lookup"><span data-stu-id="68be0-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="68be0-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) für Dateien.</span><span class="sxs-lookup"><span data-stu-id="68be0-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="68be0-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) für Nachrichten und OLE-2-Objekte.</span><span class="sxs-lookup"><span data-stu-id="68be0-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="68be0-124">Legen Sie **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)), die die Grafik Darstellung der Anlage für Datei oder binäre Anlagen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="68be0-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="68be0-125">Legen Sie sie nicht für OLE-Objekte, die intern die Renderinginformationen gespeichert werden sollen, oder für angefügte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="68be0-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="68be0-126">Legen Sie **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)), um anzugeben, wo die Anlage angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="68be0-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="68be0-127">**PR_RENDERING_POSITION** gilt nur für Clients, die die **PR_BODY** -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="68be0-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="68be0-128">Wenn Sie nur **PR_RTF_COMPRESSED**unterstützen, platzieren Sie die folgenden für Platzhalterinformationen in den komprimierten Stream:</span><span class="sxs-lookup"><span data-stu-id="68be0-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="68be0-129">Wenn **PR_RENDERING_POSITION**festlegen möchten, weisen Sie entweder eine Zahl, die einen Ordnungszahlen Offset in Zeichen, mit dem ersten Zeichen des **PR_BODY** 0 ist, wird, wenn Sie müssen in der Nachricht Where kennen, die die Anlage gerendert wird, oder 0xFFFFFFFF, darstellt, wenn Sie nicht Anlagen in **PR_BODY**zu rendern.</span><span class="sxs-lookup"><span data-stu-id="68be0-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="68be0-130">Legen Sie **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)), um den kurzen Namen der Datei für eine Dateianlage anzugeben und **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)), um den Namen der Datei anzugeben, wie unterstützt auf einer Plattform, die das Format langer Dateiname behandelt.</span><span class="sxs-lookup"><span data-stu-id="68be0-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="68be0-131">Beide Eigenschaften sind optional.</span><span class="sxs-lookup"><span data-stu-id="68be0-131">Both properties are optional.</span></span> <span data-ttu-id="68be0-132">Jedoch, wenn Sie **PR_ATTACH_LONG_FILENAME**festgelegt wird, legen Sie auch **PR_ATTACH_FILENAME**.</span><span class="sxs-lookup"><span data-stu-id="68be0-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="68be0-133">Legen Sie **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), um den Namen für die Anlage anzugeben, die in einem Dialogfeld angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="68be0-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="68be0-134">PR_DISPLAY_NAME ist optional.</span><span class="sxs-lookup"><span data-stu-id="68be0-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="68be0-135">PR_ATTACH_DATA_BIN festlegen</span><span class="sxs-lookup"><span data-stu-id="68be0-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="68be0-136">Rufen Sie [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , um die Eigenschaft mit der **IStream** -Schnittstelle zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="68be0-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="68be0-137">Rufen Sie Wenn eine Datei die Daten enthält, und es geöffnet wird, oder wenn Sie explizite Kontrolle über Puffergröße benötigen, **IStream::Write** in einer Schleife, um die Daten im Stream-Objekt zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="68be0-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="68be0-138">Eine weitere Option besteht Aufrufen **OpenStreamOnFile nicht ausgeführt werden** , um Zugriff auf die Datendatei, und rufen Sie dann diesen Datenstrom **:: CopyTo** -Methode, um die Daten in das Stream-Objekt zurückgegebene **OpenProperty**Kopieren eines Stream-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="68be0-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="68be0-139">Der neue Stream **IStream:: Commit** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="68be0-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="68be0-140">PR_ATTACH_DATA_OBJ festlegen</span><span class="sxs-lookup"><span data-stu-id="68be0-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="68be0-141">Rufen Sie **IMAPIProp::OpenProperty** zum Öffnen die-Eigenschaft mit der **IStreamDocfile** -Schnittstelle ein Stream-Objekt zu erstellen, die mit strukturierten Speicher funktioniert.</span><span class="sxs-lookup"><span data-stu-id="68be0-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="68be0-142">**IStreamDocfile** ist Zeichenfolgeneigenschaften Nachricht Clients geben eine höhere Leistung Möglichkeit zum Speichern und Abrufen von strukturierten Speicher implementiert.</span><span class="sxs-lookup"><span data-stu-id="68be0-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="68be0-143">Die **IStreamDocfile** -Schnittstelle ist identisch mit **IStream**, jedoch ist sichergestellt, dass des Inhalts des Datenstroms wird als strukturierter Speicher formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="68be0-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="68be0-144">Wenn dieser Aufruf erfolgreich ist, erstellen Sie den Stream mit die gleichen Schritte zum Festlegen von **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="68be0-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="68be0-145">Wenn **OpenProperty** ein Fehler auftritt:</span><span class="sxs-lookup"><span data-stu-id="68be0-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="68be0-146">Rufen Sie **OpenProperty** erneut für **IStorage**aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="68be0-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="68be0-147">Rufen Sie **StgOpenStorage** , um das OLE-Objekt zu öffnen und ein Speicherobjekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="68be0-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="68be0-148">Rufen Sie das zurückgegebene Speicherobjekt **IStorage::CopyTo** -Methode zum Kopieren von auf das Speicherobjekt von **OpenProperty**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68be0-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="68be0-149">Rufen Sie das neue Speicherobjekt **IStorage::Commit** -Methode.</span><span class="sxs-lookup"><span data-stu-id="68be0-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="68be0-150">PR_ATTACH_PATHNAME festlegen</span><span class="sxs-lookup"><span data-stu-id="68be0-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="68be0-151">Reservieren Sie eine [SPropValue](spropvalue.md) -Struktur, Festlegen des Members **UlPropTag** **PR_ATTACH_PATHNAME** und dem **Value.LPSZ** Mitglied in der Zeichenfolge, die den Dateinamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="68be0-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="68be0-152">Rufen Sie die Anlage [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="68be0-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="68be0-153">Wenn Ihre Plattform lange Dateinamen unterstützt, legen Sie **PR_ATTACH_PATHNAME** und **PR_ATTACH_LONG_PATHNAME**.</span><span class="sxs-lookup"><span data-stu-id="68be0-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="68be0-154">Möglicherweise müssen, stellen Sie ein Betriebssystem aufrufen Kurzname abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="68be0-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68be0-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68be0-155">See also</span></span>

- [<span data-ttu-id="68be0-156">MAPI-Anlagen</span><span class="sxs-lookup"><span data-stu-id="68be0-156">MAPI Attachments</span></span>](mapi-attachments.md)

