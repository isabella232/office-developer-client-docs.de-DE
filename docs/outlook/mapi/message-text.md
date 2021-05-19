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
  
Für ausgehende Nachrichten im MIME-Modus hängt der Inhaltstyp davon ab, ob Anlagen enthalten sind und wie der Nachrichtentext aussieht. Wenn Anlagen enthalten sind, ist der Inhaltstyp  _mehrteilig/gemischt._ Der Nachrichtentext und jede Anlage werden zu einem separaten Teil des Nachrichteninhalts, jeweils mit einem eigenen Inhaltstyp. Wenn keine Anlagen enthalten sind, ist der Inhaltstyp der Nachricht  _text/plain,_ und es gibt nur einen Teil. 
  
Der Nachrichtentext ist nur dann zeilengepackt, wenn eine Zeile mehr als 140 Zeichen lang ist. Wenn dies der Derb ist, wird der gesamte Text in 76 Spalten umbrochen, und die  _quoted-printable-Codierung_ wird verwendet, um Zeilenumbrüche zu erhalten. Der Inhaltstyp hängt davon ab, welche Zeichen im Nachrichtentext wie folgt gefunden werden: 
  
- Wenn nur 7-Bit-Zeichen gefunden werden und keine Zeile mehr als 140 Zeichen lang ist, ist die Nachricht ASCII-Text. _Inhaltstyp: text/plain; charset=us-ascii_ (Content-Transfer-Encoding=7bit wird angenommen.) 
    
- Wenn lange Zeilen oder 8-Bit-Zeichen gefunden werden, ist die Nachricht Text, und der Zeichensatz wird durch das Locale bestimmt. Sie sollte aus den Zeichensätzen ausgewählt werden, die durch den ISO-Standard 8859 definiert sind. _Inhaltstyp: text/plain; charset=iso-8859-1_ (oder ein anderer gültiger Zeichensatz) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Wenn der erste Nachrichteninhaltsteil für eingehende #A0 den Inhaltstyp _"Content": Text/ \*_ (d. h. einen beliebigen Texttyp) hat und dessen Zeichensatz erkannt wird, wird er **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) zugeordnet. Ein erster Nachrichteninhaltsteil, der diesem Kriterium nicht entspricht, wird zu einer Anlage. Alle nachfolgenden Teile werden auch zu Anlagen.
  
Im uuencode-Modus wird Nachrichtentext in ausgehenden Nachrichten wie bei MS Mail 3.x in 78 Spalten umschlossen. Der Inhaltstyp ist "text/plain". Beachten Sie die folgenden Konventionen im umschlossenen Text, um die Absatzumbrüche der ursprünglichen Nachricht unter diesen Umständen zu erhalten. Es gibt drei mögliche Gründe für das Beenden einer Textzeile mit jeweils einer eigenen Zeichensequenz:
  
- Zeilenbruch. Der ursprüngliche Text enthielt eine vom Benutzer eingegebene Newline (Absatzmarke). Im Transport wird dies einer Newline ohne vorangehende Leerstellen zuordnungen. Wenn der Benutzer eine Newline einbetritt, der Leerzeichen vorangehen, sollten die Leerstellen entfernt werden.
    
- Line-nobreak. Der ursprüngliche Text enthielt ein Wort, das zu lang war, um in eine einzelne Zeile der Nachricht zu passen. Im Transport wird dies einer Newline mit zwei Leerzeichen voranstellen.
    
- Zeilenumbruch. Der ursprüngliche Text enthielt keine Newline, der Text ist zu lang, um in eine einzelne Zeile der Nachricht zu passen, er kann jedoch zwischen zwei Wörtern unterbrochen werden. Im Transport wird dies einer Newline mit einem einzigen Leeren voranstellen.
    

