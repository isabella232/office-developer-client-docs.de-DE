---
title: Angefügte Dateien und Nachrichten
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
# <a name="attached-files-and-messages"></a><span data-ttu-id="622fb-103">Angefügte Dateien und Nachrichten</span><span class="sxs-lookup"><span data-stu-id="622fb-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="622fb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="622fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="622fb-105">Wenn MIME mit TNEF beim Codieren von Nachrichteninhalten verwendet wird, befinden sich alle Anlageneigenschaften und Inhalte im TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="622fb-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="622fb-106">Der TNEF selbst ist eine einzelne binäre angefügte Datei mit dem Namen Winmail.dat, die wie für MIME ohne TNEF beschrieben codiert wird.</span><span class="sxs-lookup"><span data-stu-id="622fb-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="622fb-107">Wenn MIME ohne TNEF verwendet wird, werden angefügte Dateien als MIME-Nachrichteninhaltsteile gesendet.</span><span class="sxs-lookup"><span data-stu-id="622fb-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="622fb-108">Der Dateiname wird im  *Name-Parameter*  im  *Inhaltstypheader*  für die Anlage platziert.</span><span class="sxs-lookup"><span data-stu-id="622fb-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="622fb-109">Der Zeichensatz für die Anlage wird im  *charset-Parameter*  für den  *Inhaltstyp platziert.*  sie und die Inhaltsübertragungscodierung werden durch Das Scannen des gesamten Anlageninhalts bestimmt.</span><span class="sxs-lookup"><span data-stu-id="622fb-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="622fb-110">URL-Anlagen werden speziell behandelt:</span><span class="sxs-lookup"><span data-stu-id="622fb-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="622fb-111">Wenn es sich bei der Anlage um eine URL (eine angefügte Datei mit Erweiterung) handelt. URL), und der in ihr definierte Zugriffsmodus ist anonymes FTP, wird als externe Nachricht codiert, und der Inhalt der Datei (die URL) wird in die Kopfzeile der externen Nachricht kopiert.</span><span class="sxs-lookup"><span data-stu-id="622fb-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="622fb-112">*Inhaltstyp: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit wird vorausgesetzt).)</span><span class="sxs-lookup"><span data-stu-id="622fb-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="622fb-113">Wenn nur 7-Bit-Zeichen gefunden werden und keine Zeile mehr als 140 Zeichen lang ist, ist die Anlage ASCII-Text.</span><span class="sxs-lookup"><span data-stu-id="622fb-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="622fb-114">*Inhaltstyp: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="622fb-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="622fb-115">Wenn lange Zeilen oder bis zu 25 % 8-Bit-Zeichen gefunden werden, ist der Anlageninhalt Text, und der Zeichensatz wird vom Locale bestimmt.</span><span class="sxs-lookup"><span data-stu-id="622fb-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="622fb-116">Sie sollte aus den Zeichensätzen ausgewählt werden, die durch den ISO-Standard 8859 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="622fb-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="622fb-117">*Inhaltstyp: text/plain; charset=ISO-8859-1*  (z. B.)</span><span class="sxs-lookup"><span data-stu-id="622fb-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="622fb-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="622fb-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="622fb-119">Wenn für 25 % oder mehr zeichen das High-Bit festgelegt ist, ist die Anlage binär.</span><span class="sxs-lookup"><span data-stu-id="622fb-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="622fb-120">Sie wird mithilfe des Base64-Algorithmus codiert.</span><span class="sxs-lookup"><span data-stu-id="622fb-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="622fb-121">*Inhaltstyp: Anwendung/Oktett-Stream*  (standardmäßig; basierend auf der Dateierweiterung)</span><span class="sxs-lookup"><span data-stu-id="622fb-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="622fb-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="622fb-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="622fb-123">Bei ausgehenden Nachrichten sollte der Inhaltstyp von der Drei-Buchstaben-Erweiterung des Dateinamens abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="622fb-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="622fb-124">Diese Zuordnung ist in der Systemregistrierung vorhanden. unter befindet sich ein Zeichenfolgenwert namens "Content Type", der den MIME-Inhaltstyp angibt, wenn einer definiert ist.</span><span class="sxs-lookup"><span data-stu-id="622fb-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="622fb-125">Dieses Beispiel gilt für eine TIFF-Bilddatei:</span><span class="sxs-lookup"><span data-stu-id="622fb-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="622fb-126">HKEY_LOCAL_MACHINE</span><span class="sxs-lookup"><span data-stu-id="622fb-126">HKEY_LOCAL_MACHINE</span></span>\
  
<span data-ttu-id="622fb-127">Software</span><span class="sxs-lookup"><span data-stu-id="622fb-127">Software</span></span>\
  
<span data-ttu-id="622fb-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="622fb-128">Microsoft</span></span>\
  
<span data-ttu-id="622fb-129">Klassen</span><span class="sxs-lookup"><span data-stu-id="622fb-129">Classes</span></span>\
  
<span data-ttu-id="622fb-130">.tif</span><span class="sxs-lookup"><span data-stu-id="622fb-130">.tif</span></span>
  
<span data-ttu-id="622fb-131">Inhaltstyp = "image/tiff"</span><span class="sxs-lookup"><span data-stu-id="622fb-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="622fb-132">Wenn keine Zuordnung für die Dateierweiterung besteht, sollte der  *Standardanwendungs-/Oktettdatenstrom*  verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="622fb-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="622fb-133">Bei eingehenden Nachrichten sollte der Inhaltstyp für eine Anlage immer in die #A0 **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="622fb-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="622fb-134">Auch wenn ein Dateiname für eine angefügte Datei definiert ist, sollte die durch den Inhaltstyp zugeordnete Erweiterung in den Eigenschaften **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) und **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="622fb-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="622fb-135">Der  *Name-Parameter*  ist von RFC 821 offiziell veraltet.</span><span class="sxs-lookup"><span data-stu-id="622fb-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="622fb-136">Bei der Weiterentwicklung der Standards wird Microsoft erwägen, eine alternative Zuordnung für angefügte Dateinamen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="622fb-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="622fb-137">Ausgehende angefügte Nachrichten werden als \* Inhaltstyp gesendet: message/rfc822 \* Nachrichten innerhalb angefügter Nachrichten werden rekursiv an der richtigen Stelle codiert.</span><span class="sxs-lookup"><span data-stu-id="622fb-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="622fb-138">Eingehende Nachrichteninhaltsteile mit  *Content-Type: Multipart/Digest*  werden auch eingebetteten Nachrichten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="622fb-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="622fb-139">Wenn uuencode mit TNEF beim Codieren von Nachrichteninhalten verwendet wird, befinden sich alle Anlageneigenschaften und -inhalte im TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="622fb-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="622fb-140">Der TNEF selbst ist eine einzelne binäre angefügte Datei mit dem Namen Winmail.dat, codiert wie für Uuencode ohne TNEF beschrieben.</span><span class="sxs-lookup"><span data-stu-id="622fb-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="622fb-141">Wenn uuencode ohne TNEF verwendet wird, werden alle angefügten Dateien nach dem Nachrichtentext als binär und uuencoded behandelt.</span><span class="sxs-lookup"><span data-stu-id="622fb-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="622fb-142">Der Dateiname ist im uuencode-Header vorhanden:</span><span class="sxs-lookup"><span data-stu-id="622fb-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="622fb-143">begin 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="622fb-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="622fb-144">... data ...</span><span class="sxs-lookup"><span data-stu-id="622fb-144">... data ...</span></span> 
  
 <span data-ttu-id="622fb-145">end</span><span class="sxs-lookup"><span data-stu-id="622fb-145">end</span></span> 
  
<span data-ttu-id="622fb-146">Angefügte Nachrichten werden in den Nachrichtentext textisiert.</span><span class="sxs-lookup"><span data-stu-id="622fb-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="622fb-147">Die Hierarchie der angefügten Nachrichten wird immer abgeflachte. Das heißt, Nachrichten innerhalb angefügter Nachrichten werden auf die oberste Ebene gezogen.</span><span class="sxs-lookup"><span data-stu-id="622fb-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="622fb-148">Eingebettete OLE-Objekte werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="622fb-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="622fb-149">Anlagenrenderingpositionen werden mithilfe der Eigenschaft **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) im TNEF übertragen.</span><span class="sxs-lookup"><span data-stu-id="622fb-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="622fb-150">Wenn TNEF nicht verwendet wird, gehen sie verloren.</span><span class="sxs-lookup"><span data-stu-id="622fb-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="622fb-151">Eingehende Anlagen ohne Renderingposition (einschließlich, wenn kein TNEF besteht) haben ihre Renderingposition auf 0xFFFFFFFF festgelegt, d. h. keine Position im Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="622fb-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="622fb-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="622fb-152">See also</span></span>



[<span data-ttu-id="622fb-153">Zuordnung von Internet-Mail-Attributen zu MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="622fb-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

