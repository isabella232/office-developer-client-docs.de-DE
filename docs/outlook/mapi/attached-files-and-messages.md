---
title: Anlagen und Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 489930b35d24d2691c9b9fbb59b0fa95707a0618
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791298"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="952ce-103">Anlagen und Nachrichten</span><span class="sxs-lookup"><span data-stu-id="952ce-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="952ce-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="952ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="952ce-105">Wenn beim Codieren Nachrichteninhalt MIME mit TNEF verwendet wird, werden alle Eigenschaften für Dateianlage und Inhalte in die TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="952ce-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="952ce-106">Das TNEF selbst ist eine einzelne, binary angefügte Datei mit dem Namen "Winmail.dat" gemäß MIME ohne TNEF-codierte.</span><span class="sxs-lookup"><span data-stu-id="952ce-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="952ce-107">Wenn MIME ohne TNEF verwendet wird, werden als MIME-Nachricht Inhaltssuche-Webparts Anlagen gesendet.</span><span class="sxs-lookup"><span data-stu-id="952ce-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="952ce-108">Der Dateiname wird in der *Name* -Parameter für die Header *Content-Type* für die Anlage platziert.</span><span class="sxs-lookup"><span data-stu-id="952ce-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="952ce-109">Der Zeichensatz für die Anlage ist der *Charset* -Parameter auf den *Inhaltstyp* angeordnet. Sie und der Content-Transfer-encoding werden durch die Überprüfung der gesamte Anlageninhalt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="952ce-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="952ce-110">URL-Anhänge werden besonders behandelt:</span><span class="sxs-lookup"><span data-stu-id="952ce-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="952ce-111">Die Anlage ist eine URL (eine angefügte Datei mit der Erweiterung. URL), und der Zugriffsmodus definiert ist, anonyme FTP, wird es als externe Nachricht codiert und der Inhalt der Datei (URL) in der Kopfzeile der externe Nachricht kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="952ce-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="952ce-112">*Content-Type: Message/External-Body; Zugriffstyp anon ftp =*  (Content-Transfer-Encoding: 7-Bit wird davon ausgegangen, dass.)</span><span class="sxs-lookup"><span data-stu-id="952ce-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="952ce-113">Wenn nur 7-Bit-Zeichen gefunden werden, und keine Linie 140 Zeichen Länge überschreitet, wird die Anlage ASCII-Text.</span><span class="sxs-lookup"><span data-stu-id="952ce-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="952ce-114">*Content-Type: Text/Plain; Charset = us-Ascii-Content-Transfer-Encoding: 7-Bit*</span><span class="sxs-lookup"><span data-stu-id="952ce-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="952ce-115">Wenn lange Zeilen oder oben auf 25 % 8-Bit-Zeichen gefunden werden, gescannt um Text handelt und der Zeichensatz wird durch das Gebietsschema bestimmt.</span><span class="sxs-lookup"><span data-stu-id="952ce-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="952ce-116">Es sollte aus der ISO-8859 standard definierten Zeichensätze ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="952ce-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="952ce-117">*Content-Type: Text/Plain; Charset = ISO-8859-1*  (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="952ce-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="952ce-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="952ce-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="952ce-119">Wenn 25 % oder mehr Zeichen das hohe Bit festgelegt ist, ist die Anlage binary.</span><span class="sxs-lookup"><span data-stu-id="952ce-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="952ce-120">Es wird die mit den Base64-Algorithmus codiert.</span><span class="sxs-lookup"><span data-stu-id="952ce-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="952ce-121">*Content-Type: Anwendung/Oktett-Stream*  (standardmäßig; basierend auf Erweiterung)</span><span class="sxs-lookup"><span data-stu-id="952ce-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="952ce-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="952ce-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="952ce-123">Für ausgehende Nachrichten sollte der Dateiname aus drei Buchstaben bestehende Erweiterung des Inhaltstyps abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="952ce-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="952ce-124">Diese Zuordnung ist in der Registrierung vorhanden. unter dort ist ein String-Wert mit dem Namen "Inhaltstyp", die den MIME-Inhaltstyp erhalten, sofern eine definiert ist.</span><span class="sxs-lookup"><span data-stu-id="952ce-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="952ce-125">In diesem Beispiel wird für eine TIFF-Bilddatei:</span><span class="sxs-lookup"><span data-stu-id="952ce-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="952ce-126">HKEY_LOCAL_MACHINE\\</span><span class="sxs-lookup"><span data-stu-id="952ce-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="952ce-127">Software\\</span><span class="sxs-lookup"><span data-stu-id="952ce-127">Software\\</span></span>
  
<span data-ttu-id="952ce-128">Microsoft\\</span><span class="sxs-lookup"><span data-stu-id="952ce-128">Microsoft\\</span></span>
  
<span data-ttu-id="952ce-129">Classes\\</span><span class="sxs-lookup"><span data-stu-id="952ce-129">Classes\\</span></span>
  
<span data-ttu-id="952ce-130">TIF</span><span class="sxs-lookup"><span data-stu-id="952ce-130">.tif</span></span>
  
<span data-ttu-id="952ce-131">Content-Type = "Image/Tiff"</span><span class="sxs-lookup"><span data-stu-id="952ce-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="952ce-132">Wenn keine Zuordnung für die Erweiterung vorhanden ist, sollte der *Anwendung/Oktett* Standarddatenstrom verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="952ce-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="952ce-133">Für eingehende Nachrichten sollte der Inhaltstyp für eine Anlage immer der MAPI-Eigenschaft **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="952ce-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="952ce-134">Auch wenn Sie ein Dateinamen für eine angefügte Datei definiert ist, sollte die Erweiterung zugeordnet, indem Sie den Inhaltstyp in die **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) und **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) Eigenschaften verwendet werden .</span><span class="sxs-lookup"><span data-stu-id="952ce-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="952ce-135">Der Parameter *Name* ist offiziell RFC 821 veraltet.</span><span class="sxs-lookup"><span data-stu-id="952ce-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="952ce-136">Weiterentwicklung von Standards berücksichtigt Microsoft eine alternative Zuordnung für angefügte Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="952ce-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="952ce-137">Ausgehende angefügte Nachrichten als * Content-Type: Message/rfc822 * Nachrichten innerhalb der angehängten Nachrichten werden codierte rekursiv, in ihrer richtigen Position.</span><span class="sxs-lookup"><span data-stu-id="952ce-137">Outbound attached messages are sent as * Content-type: message/rfc822 *  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="952ce-138">Eingehende Nachricht Inhaltssuche-Webparts mit *Content-Type: Multipart/Digest* auch eingebettete Nachrichten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="952ce-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="952ce-139">Wenn beim Codieren Nachrichteninhalt Uuencode mit TNEF verwendet wird, werden alle Eigenschaften für Dateianlage und Inhalte in die TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="952ce-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="952ce-140">Das TNEF selbst ist einer einzelnen, binary angefügte Datei mit dem Namen "Winmail.dat" codiert wie für Uuencode ohne TNEF beschrieben.</span><span class="sxs-lookup"><span data-stu-id="952ce-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="952ce-141">Wenn Uuencode ohne TNEF verwendet wird, werden alle verbundenen Dateien als Binär und UUENCODE, folgen den Nachrichtentext behandelt.</span><span class="sxs-lookup"><span data-stu-id="952ce-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="952ce-142">Der Dateiname ist im Uuencode-Header vorhanden:</span><span class="sxs-lookup"><span data-stu-id="952ce-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="952ce-143">"Winmail.dat" 0755 beginnen</span><span class="sxs-lookup"><span data-stu-id="952ce-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="952ce-144">... Daten...</span><span class="sxs-lookup"><span data-stu-id="952ce-144">... data ...</span></span> 
  
 <span data-ttu-id="952ce-145">end</span><span class="sxs-lookup"><span data-stu-id="952ce-145">end</span></span> 
  
<span data-ttu-id="952ce-146">Angefügte Nachrichten werden in den Nachrichtentext textized.</span><span class="sxs-lookup"><span data-stu-id="952ce-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="952ce-147">Die Hierarchie der angehängten Nachrichten wird immer reduziert; d. h., werden Nachrichten innerhalb der angehängten Nachrichten auf die oberste Ebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="952ce-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="952ce-148">Eingebettete OLE-Objekte werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="952ce-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="952ce-149">Anlage Rendering Positionen werden als solcher übertragen mithilfe der Eigenschaft **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in die TNEF.</span><span class="sxs-lookup"><span data-stu-id="952ce-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="952ce-150">Wenn TNEF nicht verwendet wird, werden sie verloren.</span><span class="sxs-lookup"><span data-stu-id="952ce-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="952ce-151">Eingehende Anlagen mit keine Renderingposition (einschließlich vorhanden ist keine TNEF) haben ihre Renderingposition auf 0xFFFFFFFF, d. h., keine Position im Nachrichtentext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="952ce-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="952ce-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="952ce-152">See also</span></span>



[<span data-ttu-id="952ce-153">Zuordnung von Internet Mail-Attributen zu MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="952ce-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

