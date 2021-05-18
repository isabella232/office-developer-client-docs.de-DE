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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412086"
---
# <a name="mapi-message-classes"></a>MAPI-Nachrichtenklassen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jede Nachricht verfügt über eine Nachrichtenklasseneigenschaft, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), die den Typ, den Zweck oder den Inhalt der Nachricht identifiziert. **PR_MESSAGE_CLASS** ist eine erforderliche Eigenschaft für alle neuen Nachrichten. Die Klasse einer Nachricht bestimmt das Formular, mit dem die Nachricht dem Benutzer angezeigt wird, und den Ordner zum Platzieren eingehender Nachrichten. 
  
Nachrichtenklassen sind zeichensensitive Zeichenfolgen, die ASCII-Zeichen 32 bis 127 enthalten und durch Punkte getrennt sind, aber sie können nicht mit einem Punkt enden. Jede Zeichenfolge stellt eine Ebene der Unterklasse dar, und es gibt keine Beschränkung für die Anzahl der zulässigen Ebenen. 
  
Die meisten Nachrichten, die Clientanwendungen senden  und empfangen, fallen beispielsweise in die IPM-Nachrichtenklasse, eine breite Kategorie, die alle zwischenmenschlichen Nachrichten beschreibt (d. h. Nachrichten, die von einem menschlichen Benutzer gelesen werden sollen, anstatt programmgesteuert von einem Computer). Nachrichtenspeicheranbieter beschreiben eine IPM-Nachricht genauer, indem sie eine **IPM-Unterklasse** erstellen. Die **IPM-Unterklasse** erbt die Eigenschaften der **IPM-Nachrichtenklasse.** Unterklassen der **IPM-Klasse** werden durch Verketten anderer Zeichenzeichenfolgen mit dem IPM-Bezeichner benannt, z. B. **IPM. Beachten** Sie, dass Sie eine Notiznachricht und **IPM beschreiben. Kontakt,** um eine Kontaktnachricht zu beschreiben. 
  
Um die Anzeige und Verwaltung von IPM-Nachrichten zu verarbeiten, können Clients ein Standardformular verwenden, das MAPI zur Verfügung stellt. Um die Anzeige und Verwaltung neuer Nachrichtenklassen zu verarbeiten, haben Sie als Clientanwendungsentwickler zwei Optionen:
  
1. Sie können ein neues Formular mithilfe der von MAPI definierten Formularschnittstellen erstellen, die von einem Standardclient verwendet werden können.
    
2. Sie können Einen eigenen Client schreiben, indem Sie eine vollständige, eigenständige Anwendung implementieren. 
    
Clients sollten zwar die **PR_MESSAGE_CLASS** für jede ausgehende Nachricht auf eine Unterklasse von **IPM** oder **IPC** festlegen, aber der Anbieter des Nachrichtenspeichers ist letztendlich für das Festlegen verantwortlich. Wenn also ein Client eine Nachricht sendet, ohne seine Nachrichtenklasse festlegen zu müssen, legt der Nachrichtenspeicheranbieter sie auf den entsprechenden Standardwert für den entsprechenden Clienttyp fest. Die Standardnachrichtenklasse für zwischenpersönliche Messagingclients ist **IPM**; Die Standardnachrichtenklasse für Zwischenverarbeitungskommunikationsclients ist **IPC**. 
  
Nachrichtenklassen haben eine Längeneinschränkung von 255 Zeichen. Nachrichtenklassen sollten jedoch nicht länger als 127 Zeichen sein, um die nachrichtenklassen zu unterstützen, die in Berichten verwendet werden. Berichtsnachrichtenklassen basieren auf der Klasse der ursprünglichen Nachricht mit zwei Ergänzungen: einem Präfix und einem Suffix. Das Präfix REPORT gibt an, dass es sich bei der Nachricht um einen Bericht handelt, und das Suffix gibt den Typ des Berichts an: DR (Zustellungsbericht), NDR (Unzustellbarkeitsbericht), IPNRN (Lesebericht) oder IPNNRN (ungelesener Bericht). Beachten Sie, dass diese Längeneinschränkungen in Zeichen angegeben sind. Auf Plattformen, die einen Doppel-Byte-Zeichensatz verwenden, kann die tatsächliche Byteanzahl höher sein. 
  
Nachrichtenspeicheranbieter sollten MAPI_E_INVALID_PARAMETER von ihren [IMAPIProp::SetProps-Methodenimplementierung](imapiprop-setprops.md) zurückgeben, wenn ein Client versucht, eine Zeichenfolge zuzuordnen, die den zulässigen Grenzwert für ihre Nachrichtenklasse überschreitet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

