---
title: TNEF-Streamstruktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0fcd1c79d1c0debfb18d270dc0e40de42842c6d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795746"
---
# <a name="tnef-stream-structure"></a>TNEF-Streamstruktur

  
  
**Betrifft**: Outlook 
  
TNEF-Stream beginnt mit einer 32-Bit-Signatur, die den Stream als TNEF Stream identifiziert. Befolgen die Signatur ist eine 16-Bit-Ganzzahl ohne Vorzeichen, die als Schlüssel zum Querverweis Anlagen auf ihrem Speicherort im markierten Text verwendet wird. Der Rest des Stream-Objekts ist eine Folge von TNEF-Attribute. Nachrichtenattribute im Datenstrom TNEF zuerst angezeigt, und führen Sie die Anlagenattribute. Attribute, die eine bestimmte Anlage angehören, werden gruppiert, beginnend mit dem **AttAttachRenddata** -Attribut. 
  
Die meisten Konstanten Werte, die in TNEF-Streams verwendet werden in die TNEF definiert. H-Headerdatei. In dieser Datei werden vor allem, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**und alle Bezeichner der TNEF-Attribut definiert. Andere Konstanten, die Werte, die durch ihre Interpretation einem C Sprache Compiler angegeben haben. In der Regel werden solche Konstanten verwendet, die Größe des folgenden Artikels. **Sizeof(ULONG)** in der Definition eines Elements gibt beispielsweise an, dass eine ganze Zahl, der die Größe des folgenden lange ganze Zahl ohne Vorzeichen an dieser Stelle im Datenstrom TNEF erfolgen soll. 
  
Alle Zahlen in einem TNEF-Stream im Binärformat little-Endian-gespeichert sind, jedoch werden hexadezimal in diesem Abschnitt angezeigt. Prüfsummenwerte sind einfach 16-Bit-Ganzzahlen ohne Vorzeichen, die die Summe modulo 65536 Bytes Daten, denen sind für die Prüfsumme gilt. Alle sind Attribute lange ganze Zahlen ohne Vorzeichen, einschließlich Abbruch Null Zeichen.
  
Der Schlüssel ist eine ungleich NULL, 16-Bit-Ganzzahl ohne Vorzeichen, die den Anfangswert der Anlage Verweis Schlüssel angibt. Die Anlage Verweis Schlüssel zugewiesenen jede Anlage sequenziell beginnend mit dem ersten Wert, der an die Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) vom Dienstanbieter übergeben wird, die die TNEF verwendet. Der Dienstanbieter sollte einen zufälligen Anfangswert für die Taste, um das Risiko zu minimieren, dass zwei Nachrichten mit demselben Schlüssel verwenden generieren. 
  
Die TNEF-Implementierung verwendet Attribut Bezeichner zuordnen Attribute zu ihren entsprechenden MAPI-Eigenschaften. Ein Attributbezeichner ist eine 32-Bit-Ganzzahl ohne Vorzeichen, bestehend aus zwei Word-Werte. Das hohe Word gibt den Datentyp, z. B. String oder binär, und das Wort niederwertige bestimmte Attribut identifiziert. Die Datentypen in das hohe Word sind:
  
|**Typ**|**Wert**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpString  <br/> |0x0001  <br/> |
|atpText  <br/> |0x0002  <br/> |
|atpDate  <br/> |0 x 0003  <br/> |
|atpShort  <br/> |0x0004  <br/> |
|atpLong  <br/> |0 x 0005  <br/> |
|atpByte  <br/> |0 x 0006  <br/> |
|atpWord  <br/> |0 x 0007  <br/> |
|atpDword  <br/> |0x0008  <br/> |
|atpMax  <br/> |0 x 0009  <br/> |
   
Die niederwertige Word Werte für jedes Attribut sind in der TNEF definiert. H-Headerdatei.
  

