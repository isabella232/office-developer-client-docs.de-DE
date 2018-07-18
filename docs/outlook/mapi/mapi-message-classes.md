---
title: MAPI-Nachrichtenklassen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 27b81c0939aa3e880f3998d33f4717c51bdbe681
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793024"
---
# <a name="mapi-message-classes"></a>MAPI-Nachrichtenklassen

  
  
**Betrifft**: Outlook 
  
Jede Nachricht weist eine Nachricht Class-Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), die den Typ, der Zweck oder der Inhalt der Nachricht identifiziert. **PR_MESSAGE_CLASS** ist eine erforderliche Eigenschaft für alle neuen Nachrichten. Klasse für eine Nachricht bestimmt die Form, die zur Darstellung der Nachricht auf den Benutzer und den Ordner für die Platzierung der eingehender Nachrichten verwendet wird. 
  
Nachrichtenklassen Groß-/Kleinschreibung beachtet Zeichenfolgen, die ASCII-Zeichen 32 bis 127 enthalten und werden durch einen Punkt getrennt werden, aber sie können nicht mit einem Punkt enden. Jede Zeichenfolge stellt eine Ebene von Unterklassen, und es gibt keine Beschränkung der Anzahl der Ebenen zulässig. 
  
Beispielsweise die meisten Nachrichten, die Clientanwendungen senden und empfangen werden, die in die Nachricht **IPM** Klasse, eine umfassende Kategorie, die alle Nachrichten zwischen Personen beschreibt (d. h., Nachrichten, die von einem Benutzer human, statt programmgesteuert durch gelesen werden soll ein Computer). Nachricht-Anbieter wird eine Nachricht IPM präziser durch Erstellen einer Unterklasse **IPM** beschrieben. Die **IPM** Unterklasse erbt die Eigenschaften der Nachrichtenklasse **IPM** . Unterklassen der Klasse **IPM** heißen durch andere Zeichenfolgen auf den Bezeichner IPM wie **IPM verketten. Hinweis** eine entsprechende Meldung und **IPM beschreiben. Wenden Sie sich an** zum Beschreiben von Kontakt Nachrichten. 
  
Behandeln Sie die Anzeige und Verwaltung von IPM-Nachrichten können Clients einem Standardformular simulieren, die MAPI bereitstellt. Um die Anzeige und Verwaltung von neuen Nachrichtenklassen zu behandeln, müssen Sie als Cliententwickler Anwendung zwei Optionen:
  
1. Sie können ein neues Formular erstellen, indem Sie mit der Gruppe von MAPI-defined Formular Schnittstellen, die ein standard-Client verwenden können.
    
2. Sie können einen eigene Client schreiben, durch die Implementierung einer vollständigen, eigenständige Anwendung. 
    
Obwohl Clients die **PR_MESSAGE_CLASS** -Eigenschaft für alle ausgehenden Nachrichten an eine Unterklasse der **IPM** oder **IPK**festgelegt werden sollte, hat der Nachricht Speicheranbieter die ultimative Verantwortung für das Festlegen der Steuerelementvorlage. Aus diesem Grund, wenn ein Client eine Nachricht sendet, ohne dass deren Nachrichtenklasse festgelegt, wird der Nachricht Speicheranbieter auf den entsprechenden Standardwert für den betreffenden Typ des Clients. Die Standardnachrichtenklasse für zwischen Personen Messagingclients ist **IPM**. Die Standardnachrichtenklasse für Clients prozessübergreifenden Kommunikation ist **IPK**. 
  
Nachrichtenklassen haben eine Einschränkung Länge von 255 Zeichen. Jedoch sollten Nachrichtenklassen zur Unterstützung der Nachrichtenklassen in Berichten verwendet 127 Zeichen nicht überschreiten. Report-Nachrichtenklassen basieren auf die Klasse von der ursprünglichen Nachricht, wobei zwei Ergänzungen: ein Präfix und ein Suffix. Das Präfix Bericht gibt an, dass die Nachricht ein Bericht ist, und das Suffix den Typ des Berichts gibt: DR (Übermittlungsbericht), Unzustellbarkeitsbericht (Unzustellbarkeitsbericht), IPNRN (Bericht lesen) oder IPNNRN (nonread Report). Beachten Sie, dass diese längenbeschränkungen in Zeichen angegeben werden. auf Plattformen, die einen Double-Byte-Zeichensatz verwenden, kann die tatsächliche Byteanzahl höher sein. 
  
Nachricht Anbieter sollte ihre [IMAPIProp::SetProps](imapiprop-setprops.md) -methodenimplementierungen MAPI_E_INVALID_PARAMETER zurückgeben, wenn ein Client versucht, eine Zeichenfolge zuweisen, die den zulässigen Grenzwert für die Nachrichtenklasse überschreitet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

