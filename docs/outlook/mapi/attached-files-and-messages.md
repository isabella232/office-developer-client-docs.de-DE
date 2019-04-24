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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318130"
---
# <a name="attached-files-and-messages"></a>AngeFügte Dateien und Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn MIME mit TNEF während der Codierung des Nachrichteninhalts verwendet wird, befinden sich alle Anlageneigenschaften und Inhalte im TNEF-Stream. Die TNEF selbst ist eine einzelne, binäre angefügte Datei mit dem Namen Winmail. dat, codiert gemäß der Beschreibung für MIME ohne TNEF. 
  
Wenn MIME ohne TNEF verwendet wird, werden angefügte Dateien als MIME-Nachrichteninhalts Teile gesendet. Der Dateiname wird im *Content-Type-* Header der Anlage im *Name* -Parameter angegeben. Der Zeichensatz für die Anlage wird im Parameter *CharSet* in den *Content-Type* ; Sie und die Inhaltsübertragungscodierung werden durch Überprüfen des gesamten Anlageninhalts bestimmt. URL-Anhänge werden speziell behandelt: 
  
- Bei der Anlage handelt es sich um eine URL (eine angefügte Datei mit der Erweiterung. URL), und der darin definierte Zugriffsmodus ist anonymer FTP, er wird als externe Nachricht codiert, und der Inhalt der Datei (die URL) wird in den Header der externen Nachricht kopiert. *Inhaltstyp: Message/External-Body; Access-Type = anon-FTP*  (Content-Transfer-Encoding: 7bit wird angenommen.) 
    
- Wenn nur 7-Bit-Zeichen gefunden werden und keine Zeile mehr als 140 Zeichen lang ist, ist die Anlage ASCII-Text. *Inhaltstyp: Text/Plain; charset = US-ASCII Content-Transfer-Encoding: 7bit* 
    
- Wenn lange Zeilen oder bis zu 25% 8-Bit-Zeichen gefunden werden, handelt es sich beim Anlageninhalt um Text, und der Zeichensatz wird vom Gebietsschema bestimmt. Sie sollte aus den vom ISO-Standard 8859 definierten Zeichensätzen ausgewählt werden. *Inhaltstyp: text/plain; charset = ISO-8859-1*  (zum Beispiel) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Wenn 25% oder mehr der Zeichen das hohe Bit festgelegt haben, ist die Anlage binär. Es wird mit dem Base64-Algorithmus codiert. *Inhaltstyp: Application/Oktett-Stream*  (standardmäßig, basierend auf der Dateierweiterung) 
    
     * Content-Transfer-Encoding: Base64 * 
    
Bei ausgehenden Nachrichten sollte der Inhaltstyp von der Erweiterung mit drei Buchstaben des Datei namens abgeleitet werden. Diese Zuordnung ist in der Systemregistrierung vorhanden; unter gibt es einen String-Wert mit dem Namen "Inhaltstyp", der den MIME-Inhaltstyp gibt, wenn einer definiert ist. Dieses Beispiel ist für eine TIFF-Bilddatei:
  
HKEY_LOCAL_MACHINE \
  
Software
  
Microsoft
  
Klassen
  
. TIF
  
Inhaltstyp = "Bild/TIFF"
  
Wenn es keine Zuordnung für die Dateierweiterung gibt, sollte der standardmäßige *Application/Oktett* -Stream verwendet werden. 
  
Bei eingehenden Nachrichten sollte der Inhaltstyp für eine Anlage immer in die MAPI-Eigenschaft **PR_ATTACH_MIME_TAG** ([pidtagattachmimetag (](pidtagattachmimetag-canonical-property.md)) kopiert werden. Auch wenn ein Dateiname für eine angefügte Datei definiert ist, sollte die vom Inhaltstyp zugeordnete Erweiterung in den Eigenschaften **PR_ATTACH_FILENAME** ([Pidtagattachfilename (](pidtagattachfilename-canonical-property.md)) und **PR_ATTACH_EXTENSION** ([pidtagattachextension (](pidtagattachextension-canonical-property.md)) verwendet werden. .
  
Der *Name* -Parameter wird offiziell durch RFC 821 veraltet. Bei der Entwicklung von Standards wird Microsoft erwägen, eine alternative Zuordnung für angefügte Dateinamen anzugeben. 
  
Ausgehende angefügte Nachrichten werden als * Content-Type: Message/RFC822 *-Nachrichten in angefügten Nachrichten werden rekursiv an der richtigen Stelle verschlüsselt. Inhaltsteile für eingehende Nachrichten mit dem *Inhaltstyp: multipart/Digest* werden auch eingebetteten Nachrichten zugeordnet. 
  
Wenn UUEncode mit TNEF während der Codierung des Nachrichteninhalts verwendet wird, befinden sich alle Anlageneigenschaften und Inhalte im TNEF-Stream. Die TNEF selbst ist eine einzelne, binäre angefügte Datei mit dem Namen Winmail. dat, codiert, wie für UUEncode ohne TNEF beschrieben.
  
Wenn UUEncode ohne TNEF verwendet wird, werden alle angefügten Dateien nach dem Nachrichtentext als Binär und UUEncode behandelt. Der Dateiname ist im UUEncode-Header vorhanden:
  
 BEGIN 0755 Winmail. dat 
  
 ... Data... 
  
 end 
  
AngeFügte Nachrichten werden in den Nachrichtentext übersetzt. Die Hierarchie der angefügten Nachrichten wird immer abgeflacht; Das heißt, Nachrichten in angefügten Nachrichten werden auf die oberste Ebene gezogen.
  
Eingebettete OLE-Objekte werden verworfen.
  
Anlagen Wiedergabepositionen werden buchstäblich mithilfe der Eigenschaft **PR_ATTACH_RENDERING** ([PIDTAGATTACHRENDERING (](pidtagattachrendering-canonical-property.md)) im TNEF übertragen. Wenn TNEF nicht verwendet wird, gehen Sie verloren. Eingehende Anlagen ohne Wiedergabeposition (einschließlich, wenn kein TNEF vorhanden ist) haben ihre Renderingposition auf 0xFFFFFFFF, also keine Position im Nachrichtentext festgelegt.
  
## <a name="see-also"></a>Siehe auch



[Zuordnen von Internet-e-Mail-Attributen zu MAPI-Eigenschaften](mapping-of-internet-mail-attributes-to-mapi-properties.md)

