---
title: AngeFügte Dateien und Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c4dbe1a761a753bef77168aec8d2674a1b2b100e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436839"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="8b3b6-103">AngeFügte Dateien und Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8b3b6-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="8b3b6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b3b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b3b6-105">Wenn MIME mit TNEF während der Codierung des Nachrichteninhalts verwendet wird, befinden sich alle Anlageneigenschaften und Inhalte im TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="8b3b6-106">Die TNEF selbst ist eine einzelne, binäre angefügte Datei mit dem Namen Winmail. dat, codiert gemäß der Beschreibung für MIME ohne TNEF.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="8b3b6-107">Wenn MIME ohne TNEF verwendet wird, werden angefügte Dateien als MIME-Nachrichteninhalts Teile gesendet.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="8b3b6-108">Der Dateiname wird im *Content-Type-* Header der Anlage im *Name* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="8b3b6-109">Der Zeichensatz für die Anlage wird im Parameter *CharSet* in den *Content-Type* ; Sie und die Inhaltsübertragungscodierung werden durch Überprüfen des gesamten Anlageninhalts bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="8b3b6-110">URL-Anhänge werden speziell behandelt:</span><span class="sxs-lookup"><span data-stu-id="8b3b6-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="8b3b6-111">Bei der Anlage handelt es sich um eine URL (eine angefügte Datei mit der Erweiterung. URL), und der darin definierte Zugriffsmodus ist anonymer FTP, er wird als externe Nachricht codiert, und der Inhalt der Datei (die URL) wird in den Header der externen Nachricht kopiert.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="8b3b6-112">*Inhaltstyp: Message/External-Body; Access-Type = anon-FTP*  (Content-Transfer-Encoding: 7bit wird angenommen.)</span><span class="sxs-lookup"><span data-stu-id="8b3b6-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="8b3b6-113">Wenn nur 7-Bit-Zeichen gefunden werden und keine Zeile mehr als 140 Zeichen lang ist, ist die Anlage ASCII-Text.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="8b3b6-114">*Inhaltstyp: Text/Plain; charset = US-ASCII Content-Transfer-Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="8b3b6-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="8b3b6-115">Wenn lange Zeilen oder bis zu 25% 8-Bit-Zeichen gefunden werden, handelt es sich beim Anlageninhalt um Text, und der Zeichensatz wird vom Gebietsschema bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="8b3b6-116">Sie sollte aus den vom ISO-Standard 8859 definierten Zeichensätzen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="8b3b6-117">*Inhaltstyp: text/plain; charset = ISO-8859-1*  (zum Beispiel)</span><span class="sxs-lookup"><span data-stu-id="8b3b6-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="8b3b6-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="8b3b6-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="8b3b6-119">Wenn 25% oder mehr der Zeichen das hohe Bit festgelegt haben, ist die Anlage binär.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="8b3b6-120">Es wird mit dem Base64-Algorithmus codiert.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="8b3b6-121">*Inhaltstyp: Application/Oktett-Stream*  (standardmäßig, basierend auf der Dateierweiterung)</span><span class="sxs-lookup"><span data-stu-id="8b3b6-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="8b3b6-122">Content-Transfer-Encoding: Base64 \*</span><span class="sxs-lookup"><span data-stu-id="8b3b6-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="8b3b6-123">Bei ausgehenden Nachrichten sollte der Inhaltstyp von der Erweiterung mit drei Buchstaben des Datei namens abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="8b3b6-124">Diese Zuordnung ist in der Systemregistrierung vorhanden; unter gibt es einen String-Wert mit dem Namen "Inhaltstyp", der den MIME-Inhaltstyp gibt, wenn einer definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="8b3b6-125">Dieses Beispiel ist für eine TIFF-Bilddatei:</span><span class="sxs-lookup"><span data-stu-id="8b3b6-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="8b3b6-126">HKEY_LOCAL_MACHINE \\</span><span class="sxs-lookup"><span data-stu-id="8b3b6-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="8b3b6-127">Software</span><span class="sxs-lookup"><span data-stu-id="8b3b6-127">Software\\</span></span>
  
<span data-ttu-id="8b3b6-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="8b3b6-128">Microsoft\\</span></span>
  
<span data-ttu-id="8b3b6-129">Klassen</span><span class="sxs-lookup"><span data-stu-id="8b3b6-129">Classes\\</span></span>
  
<span data-ttu-id="8b3b6-130">. TIF</span><span class="sxs-lookup"><span data-stu-id="8b3b6-130">.tif</span></span>
  
<span data-ttu-id="8b3b6-131">Inhaltstyp = "Bild/TIFF"</span><span class="sxs-lookup"><span data-stu-id="8b3b6-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="8b3b6-132">Wenn es keine Zuordnung für die Dateierweiterung gibt, sollte der standardmäßige *Application/Oktett* -Stream verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="8b3b6-133">Bei eingehenden Nachrichten sollte der Inhaltstyp für eine Anlage immer in die MAPI-Eigenschaft **PR_ATTACH_MIME_TAG** ([pidtagattachmimetag (](pidtagattachmimetag-canonical-property.md)) kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="8b3b6-134">Auch wenn ein Dateiname für eine angefügte Datei definiert ist, sollte die vom Inhaltstyp zugeordnete Erweiterung in den Eigenschaften **PR_ATTACH_FILENAME** ([Pidtagattachfilename (](pidtagattachfilename-canonical-property.md)) und **PR_ATTACH_EXTENSION** ([pidtagattachextension (](pidtagattachextension-canonical-property.md)) verwendet werden. .</span><span class="sxs-lookup"><span data-stu-id="8b3b6-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="8b3b6-135">Der *Name* -Parameter wird offiziell durch RFC 821 veraltet.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="8b3b6-136">Bei der Entwicklung von Standards wird Microsoft erwägen, eine alternative Zuordnung für angefügte Dateinamen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="8b3b6-137">Ausgehende angefügte Nachrichten werden als \* Content-Type: Message/RFC822 \*-Nachrichten in angefügten Nachrichten werden rekursiv an der richtigen Stelle verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="8b3b6-138">Inhaltsteile für eingehende Nachrichten mit dem *Inhaltstyp: multipart/Digest* werden auch eingebetteten Nachrichten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="8b3b6-139">Wenn UUEncode mit TNEF während der Codierung des Nachrichteninhalts verwendet wird, befinden sich alle Anlageneigenschaften und Inhalte im TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="8b3b6-140">Die TNEF selbst ist eine einzelne, binäre angefügte Datei mit dem Namen Winmail. dat, codiert, wie für UUEncode ohne TNEF beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="8b3b6-141">Wenn UUEncode ohne TNEF verwendet wird, werden alle angefügten Dateien nach dem Nachrichtentext als Binär und UUEncode behandelt.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="8b3b6-142">Der Dateiname ist im UUEncode-Header vorhanden:</span><span class="sxs-lookup"><span data-stu-id="8b3b6-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="8b3b6-143">BEGIN 0755 Winmail. dat</span><span class="sxs-lookup"><span data-stu-id="8b3b6-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="8b3b6-144">... Data...</span><span class="sxs-lookup"><span data-stu-id="8b3b6-144">... data ...</span></span> 
  
 <span data-ttu-id="8b3b6-145">end</span><span class="sxs-lookup"><span data-stu-id="8b3b6-145">end</span></span> 
  
<span data-ttu-id="8b3b6-146">AngeFügte Nachrichten werden in den Nachrichtentext übersetzt.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="8b3b6-147">Die Hierarchie der angefügten Nachrichten wird immer abgeflacht; Das heißt, Nachrichten in angefügten Nachrichten werden auf die oberste Ebene gezogen.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="8b3b6-148">Eingebettete OLE-Objekte werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="8b3b6-149">Anlagen Wiedergabepositionen werden buchstäblich mithilfe der Eigenschaft **PR_ATTACH_RENDERING** ([PIDTAGATTACHRENDERING (](pidtagattachrendering-canonical-property.md)) im TNEF übertragen.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="8b3b6-150">Wenn TNEF nicht verwendet wird, gehen Sie verloren.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="8b3b6-151">Eingehende Anlagen ohne Wiedergabeposition (einschließlich, wenn kein TNEF vorhanden ist) haben ihre Renderingposition auf 0xFFFFFFFF, also keine Position im Nachrichtentext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b3b6-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b3b6-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b3b6-152">See also</span></span>



[<span data-ttu-id="8b3b6-153">Zuordnen von Internet-e-Mail-Attributen zu MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b3b6-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

