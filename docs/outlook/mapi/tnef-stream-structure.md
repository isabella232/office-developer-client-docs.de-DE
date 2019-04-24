---
title: TNEF-Datenstrom Struktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327384"
---
# <a name="tnef-stream-structure"></a>TNEF-Datenstrom Struktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein TNEF-Datenstrom beginnt mit einer 32-Bit-Signatur, die den Stream als TNEF-Stream identifiziert. Nach der Signatur handelt es sich um eine 16-Bit-Ganzzahl ohne Vorzeichen, die als Schlüssel für die Querverweis Anlagen an Ihre Position im markierten Nachrichtentext verwendet wird. Der Rest des Streams ist eine Sequenz von TNEF-Attributen. Nachrichtenattribute werden zuerst im TNEF-Datenstrom angezeigt, und die Anlagenattribute folgen. Attribute, die zu einer bestimmten Anlage gehören, werden beginnend mit dem **attAttachRenddata** -Attribut gruppiert. 
  
Die meisten der Konstanten Werte, die in TNEF-Streams verwendet werden, sind im TNEF definiert. H-Headerdatei. In dieser Datei sind insbesondere **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**und alle TNEF-Attributbezeichner definiert. Andere Konstanten haben die Werte, die durch ihre Interpretation zu einem C-Sprachcompiler angezeigt werden. In der Regel werden solche Konstanten verwendet, um die Größen des folgenden Elements anzugeben. Beispielsweise gibt **sizeof (ULONG)** in der Definition eines Elements an, dass eine ganze Zahl, die die Größe der folgenden nicht signierten Long-Ganzzahl darstellt, an dieser Stelle im TNEF-Stream auftreten sollte. 
  
Alle Ganzzahlen in einem TNEF-Datenstrom werden in Little-Endian-Binärform gespeichert, werden jedoch in diesem Abschnitt in Hexadezimalschreibweise angezeigt. Prüfsummenwerte sind einfach 16-Bit-Ganzzahlen ohne Vorzeichen, die die Summe, Modulo 65536, der Datenbytes sind, auf die die Prüfsumme angewendet wird. Alle Attribut Längen sind nicht signierte lange ganze Zahlen, einschließlich aller abschließenden NULL-Zeichen.
  
Der Schlüssel ist eine ungleich NULL, 16-Bit-Ganzzahl ohne Vorzeichen, die den Anfangswert der Anlagen Referenzschlüssel angibt. Die Anlagen Referenzschlüssel werden jeder Anlage sequenziell beginnend mit dem Anfangswert zugewiesen, der von dem Dienstanbieter, der TNEF verwendet, an die [OpenTnefStream](opentnefstream.md) -Funktion übergeben wird. Der Dienstanbieter sollte einen Zufalls Anfangswert für den Schlüssel generieren, um die Wahrscheinlichkeit zu minimieren, dass zwei Nachrichten denselben Schlüssel verwenden. 
  
Die TNEF-Implementierung verwendet Attribut-IDs, um Attribute ihren entsprechenden MAPI-Eigenschaften zuzuordnen. Eine Attribut-ID ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die aus zwei Wort Werten besteht. Das hochwertige Wort gibt den Datentyp an, beispielsweise String oder Binary, und das niederwertige Wort identifiziert das jeweilige Attribut. Die Datentypen im hochwertigen Wort sind:
  
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
   
Die niedrigwertigen Word-Werte für jedes Attribut werden im TNEF definiert. H-Headerdatei.
  

