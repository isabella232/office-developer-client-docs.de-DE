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
ms.openlocfilehash: d5b37ea2e254e05ada3214309f58147e92f46393
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566831"
---
# <a name="attached-files-and-messages"></a>Angefügte Dateien und Nachrichten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn beim Codieren Nachrichteninhalt MIME mit TNEF verwendet wird, werden alle Eigenschaften für Dateianlage und Inhalte in die TNEF-Stream. Das TNEF selbst ist eine einzelne, binary angefügte Datei mit dem Namen "Winmail.dat" gemäß MIME ohne TNEF-codierte. 
  
Wenn MIME ohne TNEF verwendet wird, werden als MIME-Nachricht Inhaltssuche-Webparts Anlagen gesendet. Der Dateiname wird in der *Name* -Parameter für die Header *Content-Type* für die Anlage platziert. Der Zeichensatz für die Anlage ist der *Charset* -Parameter auf den *Inhaltstyp* angeordnet. Sie und der Content-Transfer-encoding werden durch die Überprüfung der gesamte Anlageninhalt festgelegt. URL-Anhänge werden besonders behandelt: 
  
- Die Anlage ist eine URL (eine angefügte Datei mit der Erweiterung. URL), und der Zugriffsmodus definiert ist, anonyme FTP, wird es als externe Nachricht codiert und der Inhalt der Datei (URL) in der Kopfzeile der externe Nachricht kopiert wird. *Content-Type: Message/External-Body; Zugriffstyp anon ftp =*  (Content-Transfer-Encoding: 7-Bit wird davon ausgegangen, dass.) 
    
- Wenn nur 7-Bit-Zeichen gefunden werden, und keine Linie 140 Zeichen Länge überschreitet, wird die Anlage ASCII-Text. *Content-Type: Text/Plain; Charset = us-Ascii-Content-Transfer-Encoding: 7-Bit* 
    
- Wenn lange Zeilen oder oben auf 25 % 8-Bit-Zeichen gefunden werden, gescannt um Text handelt und der Zeichensatz wird durch das Gebietsschema bestimmt. Es sollte aus der ISO-8859 standard definierten Zeichensätze ausgewählt werden. *Content-Type: Text/Plain; Charset = ISO-8859-1*  (Beispiel) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Wenn 25 % oder mehr Zeichen das hohe Bit festgelegt ist, ist die Anlage binary. Es wird die mit den Base64-Algorithmus codiert. *Content-Type: Anwendung/Oktett-Stream*  (standardmäßig; basierend auf Erweiterung) 
    
     * Content-Transfer-Encoding: base64 * 
    
Für ausgehende Nachrichten sollte der Dateiname aus drei Buchstaben bestehende Erweiterung des Inhaltstyps abgeleitet werden. Diese Zuordnung ist in der Registrierung vorhanden. unter dort ist ein String-Wert mit dem Namen "Inhaltstyp", die den MIME-Inhaltstyp erhalten, sofern eine definiert ist. In diesem Beispiel wird für eine TIFF-Bilddatei:
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
Classes\
  
TIF
  
Content-Type = "Image/Tiff"
  
Wenn keine Zuordnung für die Erweiterung vorhanden ist, sollte der *Anwendung/Oktett* Standarddatenstrom verwendet werden. 
  
Für eingehende Nachrichten sollte der Inhaltstyp für eine Anlage immer der MAPI-Eigenschaft **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) kopiert werden. Auch wenn Sie ein Dateinamen für eine angefügte Datei definiert ist, sollte die Erweiterung zugeordnet, indem Sie den Inhaltstyp in die **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) und **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) Eigenschaften verwendet werden .
  
Der Parameter *Name* ist offiziell RFC 821 veraltet. Weiterentwicklung von Standards berücksichtigt Microsoft eine alternative Zuordnung für angefügte Dateinamen angeben. 
  
Ausgehende angefügte Nachrichten als * Content-Type: Message/rfc822 * Nachrichten innerhalb der angehängten Nachrichten werden codierte rekursiv, in ihrer richtigen Position. Eingehende Nachricht Inhaltssuche-Webparts mit *Content-Type: Multipart/Digest* auch eingebettete Nachrichten zugeordnet sind. 
  
Wenn beim Codieren Nachrichteninhalt Uuencode mit TNEF verwendet wird, werden alle Eigenschaften für Dateianlage und Inhalte in die TNEF-Stream. Das TNEF selbst ist einer einzelnen, binary angefügte Datei mit dem Namen "Winmail.dat" codiert wie für Uuencode ohne TNEF beschrieben.
  
Wenn Uuencode ohne TNEF verwendet wird, werden alle verbundenen Dateien als Binär und UUENCODE, folgen den Nachrichtentext behandelt. Der Dateiname ist im Uuencode-Header vorhanden:
  
 "Winmail.dat" 0755 beginnen 
  
 ... Daten... 
  
 end 
  
Angefügte Nachrichten werden in den Nachrichtentext textized. Die Hierarchie der angehängten Nachrichten wird immer reduziert; d. h., werden Nachrichten innerhalb der angehängten Nachrichten auf die oberste Ebene abgerufen.
  
Eingebettete OLE-Objekte werden verworfen.
  
Anlage Rendering Positionen werden als solcher übertragen mithilfe der Eigenschaft **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in die TNEF. Wenn TNEF nicht verwendet wird, werden sie verloren. Eingehende Anlagen mit keine Renderingposition (einschließlich vorhanden ist keine TNEF) haben ihre Renderingposition auf 0xFFFFFFFF, d. h., keine Position im Nachrichtentext festgelegt.
  
## <a name="see-also"></a>Siehe auch



[Zuordnen von Internet-Mail-Attributen zu MAPI-Eigenschaften](mapping-of-internet-mail-attributes-to-mapi-properties.md)

