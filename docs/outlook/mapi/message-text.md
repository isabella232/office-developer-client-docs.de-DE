---
title: Nachrichtentext
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 12811f40d94bc08d57874a380fd4e9a3e822f1e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595665"
---
# <a name="message-text"></a>Nachrichtentext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei ausgehenden Nachrichten im MIME-Modus hängt der Inhaltstyp davon ab, ob Anlagen vorhanden sind und wie der Nachrichtentext aussieht. Wenn Anlagen vorhanden sind, ist der Inhaltstyp  _mehrteiliger/gemischter Inhaltstyp._ Der Nachrichtentext und jede Anlage werden zu einem separaten Teil des Nachrichteninhalts, jeder mit seinem eigenen Inhaltstyp. Wenn keine Anlagen vorhanden sind, ist der Inhaltstyp der Nachricht  _text/unformatiert,_ und es gibt nur einen Teil. 
  
Der Nachrichtentext ist nur zeilenumbrochen, wenn eine Zeile mehr als 140 Zeichen lang ist. Andernfalls wird der gesamte Text in 76 Spalten umbrochen, und die Codierung mit  _Anführungszeichen_ wird verwendet, um Zeilenumbrüche beizubehalten. Der Inhaltstyp hängt wie folgt davon ab, welche Zeichen im Nachrichtentext zu finden sind: 
  
- Wenn nur 7-Bit-Zeichen gefunden werden und keine Zeile mehr als 140 Zeichen lang ist, ist die Nachricht ASCII-Text. _Inhaltstyp: text/plain; charset=us-ascii_ (Content-Transfer-Encoding=7bit wird angenommen.) 
    
- Wenn lange Zeilen oder 8-Bit-Zeichen gefunden werden, ist die Meldung Text, und der Zeichensatz wird durch das Gebietsschema bestimmt. Sie sollte aus den Zeichensätzen ausgewählt werden, die durch den ISO-Standard 8859 definiert sind. _Inhaltstyp: text/plain; charset=iso-8859-1_ (oder ein anderer gültiger Zeichensatz) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Wenn der erste Nachrichteninhaltsteil für eingehende _MIME-Nachrichten \* den folgenden Inhaltstyp aufweist: text/(d._ a. ein beliebiger Texttyp) und dessen Zeichensatz erkannt wird, wird er **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) zugeordnet. Ein Teil des Inhalts einer ersten Nachricht, der dieses Kriterium nicht erfüllt, wird zu einer Anlage. Alle nachfolgenden Teile werden ebenfalls zu Anlagen.
  
Im uuencode-Modus ist Nachrichtentext in ausgehenden Nachrichten zeilenumschlossen in 78 Spalten, wie bei MS Mail 3.x. Der Inhaltstyp ist "text/plain". Um die Absatzumbrüche der ursprünglichen Nachricht unter diesen Umständen beizubehalten, beachten Sie die folgenden Konventionen im umschlossenen Text. Es gibt drei mögliche Gründe für das Beenden einer Textzeile mit jeweils einer eigenen Zeichenfolge:
  
- Zeilenumbruch. Der ursprüngliche Text enthielt eine vom Benutzer eingegebene Zeilenumbruchlinie (Absatzmarke). Beim Transport wird dies einer Neulinie ohne vorangehende Leerzeichen zugeordnet. Wenn der Benutzer eine Neueinleitung eingibt, der Leerzeichen vorangestellt sind, sollten die Leerstellen entfernt werden.
    
- Zeilenumbruch. Der ursprüngliche Text enthielt ein Wort, das zu lang war, um in eine einzelne Zeile der Nachricht zu passen. Beim Transport wird dies einer Neulinie zugeordnet, der zwei Leerstellen vorangestellt sind.
    
- Zeilenumbruch. Der ursprüngliche Text enthielt keine Neueinschrift, der Text ist zu lang, um in eine einzelne Zeile der Nachricht einzupassen, kann jedoch zwischen zwei Wörtern unterbrochen werden. Beim Transport wird dies einer Neuleitung zugeordnet, der ein einzelner Leertext vorangestellt ist.
    

