---
title: Nachrichtentext
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d74c9d5632e81e5b98cd1a4a02d5646cf3f6300
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592311"
---
# <a name="message-text"></a>Nachrichtentext

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Für ausgehende Nachrichten in MIME-Modus, der Inhaltstyp davon abhängig, ob Anlagen und der Nachrichtentext aussieht vorhanden sind. Wenn Anlagen vorhanden sind, der Inhaltstyp _Multipart/mixed;_ den Nachrichtentext und jede Anlage werden separate Teil des den Nachrichteninhalt, jeweils mit einem eigenen Inhaltstyp. Wenn keine Anhänge vorhanden sind, der Inhaltstyp der Nachricht ist _Text/Plain_ , und es ist nur ein Teil. 
  
E-Mail-Text wird nicht Zeile-umbrochen, wenn einige Zeile 140 Zeichen Länge überschreitet. Wenn eine Aktionen ausführt, wird der gesamte Text auf 76 Spalten umbrochen und die _quoted-printable-_ Codierung wird verwendet, um Zeilenumbrüche beibehalten. Content-Type, hängt davon ab, welche Zeichen im Nachrichtentext gefunden werden: 
  
- Wenn nur 7-Bit-Zeichen gefunden werden, und keine Linie 140 Zeichen Länge überschreitet, wird die Meldung ASCII-Text. _Content-Type: Text/Plain; Charset = us-Ascii-_ (Content-Transfer-Encoding = 7-Bit wird davon ausgegangen, dass.) 
    
- Wenn lange Zeilen oder 8-Bit-Zeichen gefunden werden, die Nachricht ist Text und der Zeichensatz wird durch das Gebietsschema bestimmt. Es sollte aus der ISO-8859 standard definierten Zeichensätze ausgewählt werden. _Content-Type: Text/Plain; Charset = Iso-8859-1_ (oder einem anderen gültigen Charset) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Für eingehenden MIME-Nachrichten, wenn die erste, Teil Nachrichteninhalt hat _Content-Type: Text /\* _ (d. h., alle Texttyp) und der Zeichensatz wird erkannt, **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) zugeordnet ist. Eine erste Content Nachrichtenteil diese Bedingung nicht erfüllt wird eine Anlage. Alle weiteren Verlauf werden auch Anlagen.
  
Im Uuencode-Modus des Nachrichtentexts in ausgehenden Nachrichten wird auf 78 Spalten, wie für MS Mail Zeile umbrochen 3.x. Content-Type ist "Text/Plain". Um die ursprüngliche Nachricht Absatzumbrüche unter diesen Umständen zu erhalten, beachten Sie die folgenden Konventionen in der umbrochenen Text. Es gibt drei mögliche Gründe für die Beendigung einer Textzeile, jeweils mit einem eigenen Zeichenfolge:
  
- Zeilenumbruch. Der ursprüngliche Text enthalten eine neue Zeile durch den Benutzer (Absatzmarke) eingegeben. In der Transport ordnet dies eine neue Zeile mit keine vorherigen Leerzeichen. Wenn der Benutzer eine neue Zeile vorangestellt Leerzeichen eingibt, sollte die Leerzeichen entfernt werden.
    
- Line-Nobreak. Der ursprüngliche Text, die ein Wort zu lang in einer einzelnen Zeile der Nachricht enthalten sind. In der Transport ordnet dies zwei Leerzeichen vorangestellt Zeilenvorschub.
    
- Zeilenumbruch. Der ursprüngliche Text enthalten keine neue Zeile, der Text ist zu lang in einer einzelnen Zeile der Nachricht, aber sie können zwischen zwei Wörtern umbrochen werden. In der Transport ordnet dies eine neue Zeile ein einzelnes Leerzeichen vorangestellt.
    

