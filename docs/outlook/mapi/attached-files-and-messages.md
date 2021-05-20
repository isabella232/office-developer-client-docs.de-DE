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
# <a name="attached-files-and-messages"></a>Angefügte Dateien und Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn MIME mit TNEF beim Codieren von Nachrichteninhalten verwendet wird, befinden sich alle Anlageneigenschaften und Inhalte im TNEF-Stream. Der TNEF selbst ist eine einzelne binäre angefügte Datei mit dem Namen Winmail.dat, die wie für MIME ohne TNEF beschrieben codiert wird. 
  
Wenn MIME ohne TNEF verwendet wird, werden angefügte Dateien als MIME-Nachrichteninhaltsteile gesendet. Der Dateiname wird im  *Name-Parameter*  im  *Inhaltstypheader*  für die Anlage platziert. Der Zeichensatz für die Anlage wird im  *charset-Parameter*  für den  *Inhaltstyp platziert.*  sie und die Inhaltsübertragungscodierung werden durch Das Scannen des gesamten Anlageninhalts bestimmt. URL-Anlagen werden speziell behandelt: 
  
- Wenn es sich bei der Anlage um eine URL (eine angefügte Datei mit Erweiterung) handelt. URL), und der in ihr definierte Zugriffsmodus ist anonymes FTP, wird als externe Nachricht codiert, und der Inhalt der Datei (die URL) wird in die Kopfzeile der externen Nachricht kopiert. *Inhaltstyp: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit wird vorausgesetzt).) 
    
- Wenn nur 7-Bit-Zeichen gefunden werden und keine Zeile mehr als 140 Zeichen lang ist, ist die Anlage ASCII-Text. *Inhaltstyp: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit* 
    
- Wenn lange Zeilen oder bis zu 25 % 8-Bit-Zeichen gefunden werden, ist der Anlageninhalt Text, und der Zeichensatz wird vom Locale bestimmt. Sie sollte aus den Zeichensätzen ausgewählt werden, die durch den ISO-Standard 8859 definiert sind. *Inhaltstyp: text/plain; charset=ISO-8859-1*  (z. B.) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Wenn für 25 % oder mehr zeichen das High-Bit festgelegt ist, ist die Anlage binär. Sie wird mithilfe des Base64-Algorithmus codiert. *Inhaltstyp: Anwendung/Oktett-Stream*  (standardmäßig; basierend auf der Dateierweiterung) 
    
     * Content-Transfer-Encoding: base64 * 
    
Bei ausgehenden Nachrichten sollte der Inhaltstyp von der Drei-Buchstaben-Erweiterung des Dateinamens abgeleitet werden. Diese Zuordnung ist in der Systemregistrierung vorhanden. unter befindet sich ein Zeichenfolgenwert namens "Content Type", der den MIME-Inhaltstyp angibt, wenn einer definiert ist. Dieses Beispiel gilt für eine TIFF-Bilddatei:
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
Klassen\
  
.tif
  
Inhaltstyp = "image/tiff"
  
Wenn keine Zuordnung für die Dateierweiterung besteht, sollte der  *Standardanwendungs-/Oktettdatenstrom*  verwendet werden. 
  
Bei eingehenden Nachrichten sollte der Inhaltstyp für eine Anlage immer in die #A0 **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) kopiert werden. Auch wenn ein Dateiname für eine angefügte Datei definiert ist, sollte die durch den Inhaltstyp zugeordnete Erweiterung in den Eigenschaften **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) und **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) verwendet werden.
  
Der  *Name-Parameter*  ist von RFC 821 offiziell veraltet. Bei der Weiterentwicklung der Standards wird Microsoft erwägen, eine alternative Zuordnung für angefügte Dateinamen anzugeben. 
  
Ausgehende angefügte Nachrichten werden als * Inhaltstyp gesendet: message/rfc822 * Nachrichten innerhalb angefügter Nachrichten werden rekursiv an der richtigen Stelle codiert. Eingehende Nachrichteninhaltsteile mit  *Content-Type: Multipart/Digest*  werden auch eingebetteten Nachrichten zugeordnet. 
  
Wenn uuencode mit TNEF beim Codieren von Nachrichteninhalten verwendet wird, befinden sich alle Anlageneigenschaften und -inhalte im TNEF-Stream. Der TNEF selbst ist eine einzelne binäre angefügte Datei mit dem Namen Winmail.dat, codiert wie für Uuencode ohne TNEF beschrieben.
  
Wenn uuencode ohne TNEF verwendet wird, werden alle angefügten Dateien nach dem Nachrichtentext als binär und uuencoded behandelt. Der Dateiname ist im uuencode-Header vorhanden:
  
 begin 0755 Winmail.dat 
  
 ... data ... 
  
 end 
  
Angefügte Nachrichten werden in den Nachrichtentext textisiert. Die Hierarchie der angefügten Nachrichten wird immer abgeflachte. Das heißt, Nachrichten innerhalb angefügter Nachrichten werden auf die oberste Ebene gezogen.
  
Eingebettete OLE-Objekte werden verworfen.
  
Anlagenrenderingpositionen werden mithilfe der Eigenschaft **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) im TNEF übertragen. Wenn TNEF nicht verwendet wird, gehen sie verloren. Eingehende Anlagen ohne Renderingposition (einschließlich, wenn kein TNEF besteht) haben ihre Renderingposition auf 0xFFFFFFFF festgelegt, d. h. keine Position im Nachrichtentext.
  
## <a name="see-also"></a>Siehe auch



[Zuordnung von Internet-Mail-Attributen zu MAPI-Eigenschaften](mapping-of-internet-mail-attributes-to-mapi-properties.md)

