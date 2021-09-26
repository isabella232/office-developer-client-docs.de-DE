---
title: TNEF-Datenstromstruktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f4898c6bfab4ee93c70455999f3e95e47be6bd23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619624"
---
# <a name="tnef-stream-structure"></a>TNEF-Datenstromstruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein TNEF-Stream beginnt mit einer 32-Bit-Signatur, die den Datenstrom als TNEF-Stream identifiziert. Nach der Signatur folgt eine 16-Bit-Ganzzahl ohne Vorzeichen, die als Schlüssel verwendet wird, um Anlagen auf ihre Position im markierten Nachrichtentext zu verweisen. Der Rest des Datenstroms ist eine Sequenz von TNEF-Attributen. Nachrichtenattribute werden zuerst im TNEF-Stream angezeigt, und Anlagenattribute folgen. Attribute, die zu einer bestimmten Anlage gehören, werden gruppiert, beginnend mit dem **attribut attAttachRenddata.** 
  
Die meisten der in TNEF-Datenströmen verwendeten Konstantenwerte sind im TNEF definiert. H-Headerdatei. In dieser Datei sind **TNEF_SIGNATURE,** **LVL_MESSAGE,** **LVL_ATTACHMENT** und alle TNEF-Attributbezeichner definiert. Andere Konstanten weisen die Werte auf, die durch ihre Interpretation für einen C-Sprachcompiler angegeben werden. In der Regel werden solche Konstanten verwendet, um die Größen des folgenden Elements zu erhalten. Beispielsweise gibt **sizeof(ULONG)** in der Definition eines Elements an, dass an dieser Stelle im TNEF-Datenstrom eine ganze Zahl auftreten soll, die die Größe der folgenden nicht signierten langen ganzzahl darstellt. 
  
Alle ganzzahligen Zahlen in einem TNEF-Datenstrom werden in binärer Little-Endian-Form gespeichert, werden jedoch in diesem Abschnitt hexadezimal dargestellt. Prüfsummenwerte sind einfach 16-Bit-Ganzzahlen ohne Vorzeichen, die die Summe (Modulo 65536) der Datenbytes sind, auf die die Prüfsumme angewendet wird. Alle Attributlängen sind unsignierte lange ganze Zahlen, einschließlich aller endenden NULL-Zeichen.
  
Der Schlüssel ist eine 16-Bit-Ganzzahl ohne Vorzeichen ungleich Null, die den Anfangswert der Anlagenreferenzschlüssel angibt. Die Anlagenverweisschlüssel werden jeder Anlage sequenziell zugewiesen, beginnend mit dem Anfangswert, der von dem Dienstanbieter, der TNEF verwendet, an die [OpenTnefStream-Funktion](opentnefstream.md) übergeben wird. Der Dienstanbieter sollte einen zufälligen Anfangswert für den Schlüssel generieren, um die Wahrscheinlichkeit zu minimieren, dass zwei Nachrichten denselben Schlüssel verwenden. 
  
Die TNEF-Implementierung verwendet Attributbezeichner, um Attribute ihren entsprechenden MAPI-Eigenschaften zuzuordnen. Ein Attributbezeichner ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die aus zwei Wortwerten besteht. Das Wort in hoher Reihenfolge gibt den Datentyp an, z. B. Zeichenfolge oder Binärdatei, und das Wort in niedriger Reihenfolge identifiziert das jeweilige Attribut. Die Datentypen im Hochreihenfolge-Wort sind:
  
|**Typ**|**Wert**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpString  <br/> |0x0001  <br/> |
|atpText  <br/> |0x0002  <br/> |
|atpDate  <br/> |0x0003  <br/> |
|atpShort  <br/> |0x0004  <br/> |
|atpLong  <br/> |0x0005  <br/> |
|atpByte  <br/> |0x0006  <br/> |
|atpWord  <br/> |0x0007  <br/> |
|atpDword  <br/> |0x0008  <br/> |
|atpMax  <br/> |0x0009  <br/> |
   
Die Wortwerte in niedriger Reihenfolge für jedes Attribut werden im TNEF definiert. H-Headerdatei.
  

