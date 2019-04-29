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
ms.openlocfilehash: fcbdec5adcb47ffac431a832cbb851ee4ebe16d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418547"
---
# <a name="message-text"></a>Nachrichtentext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei ausgehenden Nachrichten im MIME-Modus hängt der Inhaltstyp davon ab, ob Anlagen vorhanden sind und wie der Nachrichtentext aussieht. Wenn es Anlagen gibt, ist der Inhaltstyp multipart _/mixed;_ der Nachrichtentext und jede Anlage werden ein separater Teil des Nachrichteninhalts, jeder mit seinem eigenen Inhaltstyp. Wenn keine Anlagen vorhanden sind, ist der Inhaltstyp der Nachricht _Text/Plain_ , und es gibt nur einen Teil. 
  
Der Nachrichtentext ist nicht mit einer Zeile umschlossen, es sei denn, eine Zeile überschreitet 140 Zeichen. Wenn dies der Fall ist, wird der gesamte Text in 76 Spalten umbrochen, und die _angegebene-druckbare_ Codierung wird verwendet, um Zeilenumbrüche beizubehalten. Der Inhaltstyp hängt wie folgt von den Zeichen im Nachrichtentext ab: 
  
- Wenn nur 7-Bit-Zeichen gefunden werden und keine Zeile mehr als 140 Zeichen lang ist, handelt es sich bei der Nachricht um ASCII-Text. _Inhaltstyp: text/plain; charset = US-ASCII_ (Content-Transfer-Encoding = 7bit wird angenommen.) 
    
- Wenn lange Zeilen oder 8-Bit-Zeichen gefunden werden, ist die Nachricht Text, und der Zeichensatz wird vom Gebietsschema bestimmt. Sie sollte aus den vom ISO-Standard 8859 definierten Zeichensätzen ausgewählt werden. _Inhaltstyp: text/plain; charset = ISO-8859-1_ (oder ein anderer gültiger Zeichensatz) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Bei eingehenden MIME-Nachrichten, wenn der erste Nachrichteninhalts Bereich _Content-Type:\* Text/_ (also ein beliebiger Texttyp) und dessen Zeichensatz erkannt wird, wird er **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) zugeordnet. Ein erster Nachrichteninhalts Teil, der dieses Kriterium nicht erfüllt, wird zu einer Anlage. Alle nachfolgenden Teile werden auch zu Anlagen.
  
Im UUEncode-Modus ist der Nachrichtentext in ausgehenden Nachrichten in 78 Spalten Zeilenumbruch, wie bei MS Mail 3. x. Der Inhaltstyp ist "Text/Plain". Wenn Sie die Absatzumbrüche der ursprünglichen Nachricht unter diesen Umständen beibehalten möchten, beachten Sie die folgenden Konventionen im eingebundenen Text. Es gibt drei mögliche Gründe, um eine Textzeile mit einer eigenen Zeichenfolge zu beenden:
  
- Linien Umbruch. Der ursprüngliche Text enthielt einen vom Benutzer eingegebenen Zeilenumbruch (Absatzmarke). Im Transport wird dieser einem Zeilenumbruch ohne vorstehende Leerzeichen zugeordnet. Wenn der Benutzer eine Zeile mit Leerzeichen vorangestellt wird, sollten die Leerzeichen entfernt werden.
    
- Linien NOBREAK. Der ursprüngliche Text enthielt ein Wort zu lang, um in eine einzelne Zeile der Nachricht einzufügen. Im Transport wird eine Zeile mit zwei Leerzeichen vorangestellt.
    
- Zeilenumbruch. Der ursprüngliche Text enthielt keinen Zeilenumbruch, der Text ist zu lang für eine einzelne Zeile der Nachricht, er kann jedoch zwischen zwei Wörtern unterbrochen werden. Im Transport wird dieser einem Zeilenumbruch, der mit einem einzelnen Leerzeichen vorangestellt ist, zugeordnet.
    

