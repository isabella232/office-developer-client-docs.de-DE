---
title: Angefügte Dateien und Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eb60d55732c0ba91aca3a6bfce03f45dab069b93
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631090"
---
# <a name="attached-files-and-messages"></a>Angefügte Dateien und Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn MIME mit TNEF beim Codieren von Nachrichteninhalten verwendet wird, befinden sich alle Anlageneigenschaften und -inhalte im TNEF-Stream. Der TNEF selbst ist eine einzelne, binäre angefügte Datei mit dem Namen "Winmail.dat", die wie für MIME ohne TNEF beschrieben codiert ist. 
  
Wenn MIME ohne TNEF verwendet wird, werden angefügte Dateien als MIME-Nachrichteninhaltsteile gesendet. Der Dateiname wird im  *Namensparameter*  in die Kopfzeile des  *Inhaltstyps*  für die Anlage eingefügt. Der Zeichensatz für die Anlage wird im  *Charset-Parameter*  des  *Inhaltstyps*  platziert; sie und die Codierung der Inhaltsübertragung werden durch Scannen des gesamten Anlageninhalts bestimmt. URL-Anlagen werden speziell behandelt: 
  
- Wenn die Anlage eine URL ist (eine angefügte Datei mit der Erweiterung . URL), und der darin definierte Zugriffsmodus ist anonymer FTP-Modus, wird als externe Nachricht codiert, und der Inhalt der Datei (die URL) wird in den Header der externen Nachricht kopiert. *Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.) 
    
- Wenn nur 7-Bit-Zeichen gefunden werden und keine Zeile 140 Zeichen überschreitet, ist die Anlage ASCII-Text. *Inhaltstyp: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit* 
    
- Wenn lange Zeilen oder bis zu 25 % 8-Bit-Zeichen gefunden werden, ist der Anlageninhalt Text, und der Zeichensatz wird durch das Gebietsschema bestimmt. Sie sollte aus den Zeichensätzen ausgewählt werden, die durch den ISO-Standard 8859 definiert sind. *Inhaltstyp: text/plain; charset=ISO-8859-1*  (z. B.) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Wenn 25 % oder mehr der Zeichen den High-Bit-Satz aufweisen, ist die Anlage binär. Sie wird mithilfe des Base64-Algorithmus codiert. *Inhaltstyp: application/octet-stream*  (standardmäßig; basierend auf der Dateierweiterung) 
    
     * Content-Transfer-Encoding: base64 * 
    
Bei ausgehenden Nachrichten sollte der Inhaltstyp von der Drei-Buchstaben-Erweiterung des Dateinamens abgeleitet werden. Diese Zuordnung ist in der Systemregistrierung vorhanden. darunter befindet sich ein Zeichenfolgenwert mit dem Namen "Content Type", der den MIME-Inhaltstyp angibt, wenn einer definiert ist. Dieses Beispiel gilt für eine TIFF-Bilddatei:
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
Classes\
  
TIF
  
Inhaltstyp = "image/tiff"
  
Wenn keine Zuordnung für die Dateierweiterung vorhanden ist, sollte der  *Standardmäßige Anwendungs-/Oktettdatenstrom*  verwendet werden. 
  
Bei eingehenden Nachrichten sollte der Inhaltstyp für eine Anlage immer in die MAPI-Eigenschaft **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) kopiert werden. Auch wenn ein Dateiname für eine angefügte Datei definiert ist, sollte die durch den Inhaltstyp zugeordnete Erweiterung in den Eigenschaften **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) und **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) verwendet werden.
  
Der  *Name-Parameter*  ist von RFC 821 offiziell veraltet. Bei der Weiterentwicklung von Standards wird Microsoft erwägen, eine alternative Zuordnung für angefügte Dateinamen anzugeben. 
  
Ausgehende angefügte Nachrichten werden als * Inhaltstyp: Message/rfc822 * Nachrichten innerhalb angefügter Nachrichten rekursiv an ihrem richtigen Ort codiert. Inhaltsteile für eingehende Nachrichten mit  *Inhaltstyp: Multipart/Digest*  werden auch eingebetteten Nachrichten zugeordnet. 
  
Wenn uuencode mit TNEF beim Codieren von Nachrichteninhalten verwendet wird, befinden sich alle Anlageneigenschaften und -inhalte im TNEF-Stream. Der TNEF selbst ist eine einzelne, binäre angefügte Datei mit dem Namen "Winmail.dat", die wie für Uuencode ohne TNEF beschrieben codiert ist.
  
Wenn uuencode ohne TNEF verwendet wird, werden alle angefügten Dateien als binär und uuencoded behandelt und folgen dem Nachrichtentext. Der Dateiname ist im uuencode-Header vorhanden:
  
 begin 0755 Winmail.dat 
  
 ... Daten... 
  
 end 
  
Angefügte Nachrichten werden in den Nachrichtentext textisiert. Die Hierarchie der angefügten Nachrichten wird immer vereinfacht. d. h., Nachrichten in angefügten Nachrichten werden auf die oberste Ebene gezogen.
  
Eingebettete OLE-Objekte werden verworfen.
  
Anlagenrenderingpositionen werden mithilfe der Eigenschaft **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) im TNEF wortwörtlich übertragen. Wenn TNEF nicht verwendet wird, gehen sie verloren. Bei eingehenden Anlagen ohne Renderingposition (auch wenn kein TNEF vorhanden ist) wird ihre Renderingposition auf 0xFFFFFFFF festgelegt, d. h. keine Position im Nachrichtentext.
  
## <a name="see-also"></a>Siehe auch



[Zuordnen von Internet-Mail-Attributen zu MAPI-Eigenschaften](mapping-of-internet-mail-attributes-to-mapi-properties.md)

