---
title: TNEF Stream Structure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430203"
---
# <a name="tnef-stream-structure"></a>TNEF Stream Structure

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein TNEF-Stream beginnt mit einer 32-Bit-Signatur, die den Datenstrom als TNEF-Stream identifiziert. Nach der Signatur folgt eine 16-Bit-Ganzzahl ohne Vorzeichen, die als Schlüssel zum Querverweisen von Anlagen auf ihren Speicherort im markierten Nachrichtentext verwendet wird. Der Rest des Datenstroms ist eine Sequenz von TNEF-Attributen. Nachrichtenattribute werden zuerst im TNEF-Stream angezeigt, und Anlagenattribute folgen. Attribute, die zu einer bestimmten Anlage gehören, werden zusammengehören, beginnend mit dem **attAttachRenddata-Attribut.** 
  
Die meisten konstanten Werte, die in TNEF-Datenströmen verwendet werden, sind im TNEF definiert. H-Headerdatei. Insbesondere werden **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT** und alle TNEF-Attributbezeichner in dieser Datei definiert. Andere Konstanten haben die Werte, die durch ihre Interpretation für einen C-Sprachcompiler angegeben werden. In der Regel werden solche Konstanten verwendet, um die Größen des folgenden Elements zu erhalten. Beispielsweise gibt **sizeof(ULONG)** in der Definition eines Elements an, dass eine ganze Zahl, die die Größe der folgenden nicht signierten langen ganzzahligen Zahl darstellt, an dieser Stelle im TNEF-Stream auftreten sollte. 
  
Alle ganzzahligen Zahlen in einem TNEF-Datenstrom werden in binärer Klein-End-Form gespeichert, werden aber in diesem Abschnitt hexadezimal angezeigt. Prüfsummenwerte sind einfach 16-Bit-Ganzzahlen ohne Vorzeichen, die die Summe ( modulo 65536 ) der Bytes von Daten sind, auf die die Prüfsumme angewendet wird. Alle Attributlängen sind nicht signierte ganze Zahlen, einschließlich aller endenden Nullzeichen.
  
Der Schlüssel ist eine 16-Bit-Ganzzahl ohne Vorzeichen, die den Anfangswert der Anlagenreferenzschlüssel darstellt. Die Anlagenreferenzschlüssel werden jeder Anlage sequenziell zugewiesen, beginnend mit dem Anfangswert, der vom Dienstanbieter, der TNEF verwendet, an die [OpenTnefStream-Funktion](opentnefstream.md) übergeben wird. Der Dienstanbieter sollte einen zufälligen Anfangswert für den Schlüssel generieren, um die Wahrscheinlichkeit zu minimieren, dass zwei Nachrichten denselben Schlüssel verwenden. 
  
Die TNEF-Implementierung verwendet Attributbezeichner, um Attribute ihren entsprechenden MAPI-Eigenschaften zu zuordnungen. Ein Attributbezeichner ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die aus zwei Wortwerten besteht. Das Wort in hoher Reihenfolge gibt den Datentyp an, z. B. Zeichenfolge oder Binärdatei, und das Wort mit niedriger Reihenfolge identifiziert das bestimmte Attribut. Die Datentypen im Wort in hoher Reihenfolge sind:
  
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
   
Die Wörterwerte niedriger Reihenfolge für jedes Attribut werden im TNEF definiert. H-Headerdatei.
  

