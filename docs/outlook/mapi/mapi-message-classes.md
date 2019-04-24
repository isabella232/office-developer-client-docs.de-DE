---
title: MAPI-Nachrichtenklassen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b2ab5d56c53216152a83ca207ff5ba1d53c9049d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345894"
---
# <a name="mapi-message-classes"></a>MAPI-Nachrichtenklassen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jede Nachricht verfügt über eine Nachrichtenklassen Eigenschaft, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), die den Typ, Zweck oder Inhalt der Nachricht identifiziert. **PR_MESSAGE_CLASS** ist eine erforderliche Eigenschaft für alle neuen Nachrichten. Die Klasse einer Nachricht bestimmt das Formular, das verwendet wird, um die Nachricht dem Benutzer und dem Ordner zum Platzieren eingehender Nachrichten zu übertragen. 
  
Nachrichtenklassen sind Zeichenfolgen mit Berücksichtigung der Groß-/Kleinschreibung, die ASCII-Zeichen 32 bis 127 enthalten und durch Punkte getrennt sind, jedoch nicht mit einem Punkt enden können. Jede Zeichenfolge stellt eine Ebene der Unterklasse dar, und es gibt keine Begrenzung für die Anzahl der zulässigen Ebenen. 
  
Die meisten Nachrichten, die von Clientanwendungen gesendet und empfangen werden, fallen beispielsweise in die **IPM** -Nachrichtenklasse, eine allgemeine Kategorie, die alle zwischenmenschlichen Nachrichten beschreibt (also Nachrichten, die von einem Benutzer des Benutzers gelesen werden sollen, statt programmgesteuert durch eine Computer). Nachrichtenspeicher Anbieter beschreiben eine IPM-Nachricht präziser, indem Sie eine **IPM** -Unterklasse erstellen. Die **IPM** -Unterklasse erbt die Eigenschaften der **IPM** -Nachrichtenklasse. Unterklassen der **IPM** -Klasse werden durch die Verkettung anderer Zeichenfolgen mit dem IPM-Bezeichner (beispielsweise **IPM) benannt. Hinweis** zur Beschreibung einer Note-Meldung und **IPM. Kontakt** zur Beschreibung einer Kontakt Nachricht. 
  
Um die Anzeige und Verwaltung von IPM-Nachrichten zu behandeln, können Clients ein Standardformular verwenden, das MAPI bereitstellt. Um die Anzeige und Verwaltung neuer Nachrichtenklassen zu behandeln, haben Sie als Client Anwendungsentwickler zwei Optionen:
  
1. Sie können ein neues Formular mithilfe der MAPI-definierten Formular Schnittstellen erstellen, die ein Standard Client verwenden kann.
    
2. Sie können einen eigenen Client schreiben, indem Sie eine vollständige, eigenständige Anwendung implementieren. 
    
Obwohl Clients die **PR_MESSAGE_CLASS** -Eigenschaft für jede ausgehende Nachricht auf eine Unterklasse von entweder **IPM** oder **IPC**festlegen sollten, hat der Nachrichtenspeicher Anbieter die ultimative Verantwortung für die Festlegung. Wenn also ein Client eine Nachricht sendet, ohne die Nachrichtenklasse festzulegen, wird Sie vom Nachrichtenspeicher Anbieter auf den entsprechenden Standardwert für den entsprechenden Clienttyp festgelegt. Die Standardnachrichtenklasse für zwischenmenschliche Messagingclients ist **IPM**; die Standardnachrichtenklasse für Interprocess-Kommunikations Clients ist **IPC**. 
  
Nachrichtenklassen haben eine Längenbeschränkung von 255 Zeichen. Nachrichtenklassen sollten jedoch 127 Zeichen nicht überschreiten, um die in Berichten verwendeten Nachrichtenklassen zu unterstützen. Berichtsnachrichten Klassen basieren auf der Klasse der ursprünglichen Nachricht mit zwei Ergänzungen: einem Präfix und einem Suffix. Der Präfix Bericht gibt an, dass die Nachricht ein Bericht ist, und das Suffix gibt den Typ des Berichts an: DR (zugestellter Bericht), NDR (Unzustellbarkeitsbericht), IPNRN (Bericht lesen) oder IPNNRN (nonread Report). Beachten Sie, dass diese Längeneinschränkungen in Zeichen angegeben werden. auf Plattformen, die einen Double-Byte-Zeichensatz verwenden, ist die tatsächliche Bytezahl möglicherweise höher. 
  
Nachrichtenspeicher Anbieter sollten MAPI_E_INVALID_PARAMETER aus Ihren [IMAPIProp::](imapiprop-setprops.md) SetProps-Methodenimplementierungen zurückgeben, wenn ein Client versucht, eine Zeichenfolge zuzuweisen, die den zulässigen Grenzwert für die Nachrichtenklasse überschreitet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

