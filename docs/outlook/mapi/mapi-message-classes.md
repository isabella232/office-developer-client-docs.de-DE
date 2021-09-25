---
title: MAPI-Nachrichtenklassen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a6e78051b095643b49bc8386364904618105467a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579600"
---
# <a name="mapi-message-classes"></a>MAPI-Nachrichtenklassen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jede Nachricht verfügt über eine Nachrichtenklasseneigenschaft, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), die den Typ, den Zweck oder den Inhalt der Nachricht identifiziert. **PR_MESSAGE_CLASS** ist eine erforderliche Eigenschaft für alle neuen Nachrichten. Die Klasse einer Nachricht bestimmt das Formular, mit dem die Nachricht dem Benutzer angezeigt wird, und den Ordner zum Platzieren eingehender Nachrichten. 
  
Bei Nachrichtenklassen handelt es sich um Zeichenzeichenfolgen mit Groß-/Kleinschreibung, die ASCII-Zeichen 32 bis 127 enthalten und durch Punkte getrennt sind, jedoch nicht mit einem Punkt enden können. Jede Zeichenfolge stellt eine Unterklassenebene dar, und es gibt keine Beschränkung für die Anzahl der zulässigen Ebenen. 
  
Die meisten Nachrichten, die Clientanwendungen senden und empfangen, fallen beispielsweise in die **IPM-Nachrichtenklasse,** eine allgemeine Kategorie, die alle zwischenmenschlichen Nachrichten beschreibt (d. a. Nachrichten, die von einem menschlichen Benutzer gelesen werden sollen, anstatt programmgesteuert von einem Computer). Nachrichtenspeicheranbieter beschreiben eine IPM-Nachricht genauer, indem sie eine **IPM-Unterklasse** erstellen. Die **IPM-Unterklasse** erbt die Eigenschaften der **IPM-Nachrichtenklasse.** Unterklassen der **IPM-Klasse** werden benannt, indem andere Zeichenfolgen mit dem IPM-Bezeichner wie **IPM verkettet werden. Notieren Sie** sich eine Notiznachricht und **IPM. Kontakt,** um eine Kontaktnachricht zu beschreiben. 
  
Zum Behandeln der Anzeige und Verwaltung von IPM-Nachrichten können Clients ein Standardformular verwenden, das mapi bereitstellt. Um die Anzeige und Verwaltung neuer Nachrichtenklassen zu verwalten, stehen Ihnen als Clientanwendungsentwickler zwei Optionen zur Verfügung:
  
1. Sie können ein neues Formular mithilfe der MAPI-definierten Formularschnittstellen erstellen, die ein Standardclient verwenden kann.
    
2. Sie können Ihren eigenen Client schreiben, indem Sie eine vollständige eigenständige Anwendung implementieren. 
    
Obwohl Clients die **eigenschaft PR_MESSAGE_CLASS** für jede ausgehende Nachricht auf eine Unterklasse von **IPM** oder **IPC** festlegen sollten, hat der Nachrichtenspeicheranbieter letztendlich die Verantwortung für die Festlegung. Wenn ein Client eine Nachricht sendet, ohne seine Nachrichtenklasse festzulegen, legt der Nachrichtenspeicheranbieter sie daher auf den entsprechenden Standardwert für den entsprechenden Clienttyp fest. Die Standardnachrichtenklasse für zwischenmenschliche Messaging-Clients ist **IPM;** Die Standardnachrichtenklasse für Interprocess-Kommunikationsclients ist **IPC.** 
  
Nachrichtenklassen haben eine Längeneinschränkung von 255 Zeichen. Nachrichtenklassen dürfen jedoch 127 Zeichen nicht überschreiten, um die in Berichten verwendeten Nachrichtenklassen zu unterstützen. Berichtsnachrichtenklassen basieren auf der Klasse der ursprünglichen Nachricht mit zwei Ergänzungen: einem Präfix und einem Suffix. Das Präfix REPORT gibt an, dass die Nachricht ein Bericht ist, und das Suffix gibt den Typ des Berichts an: DR (Übermittlungsbericht), NDR (Nicht-Bericht), IPNRN (Lesebericht) oder IPNNRN (nicht gelesener Bericht). Beachten Sie, dass diese Längeneinschränkungen in Zeichen angegeben sind. Auf Plattformen, die einen Doppelbyte-Zeichensatz verwenden, ist die tatsächliche Byteanzahl möglicherweise höher. 
  
Nachrichtenspeicheranbieter sollten MAPI_E_INVALID_PARAMETER aus ihren [IMAPIProp::SetProps-Methodenimplementierungen](imapiprop-setprops.md) zurückgeben, wenn ein Client versucht, eine Zeichenfolge zuzuweisen, die den zulässigen Grenzwert für ihre Nachrichtenklasse überschreitet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Nachrichten](mapi-messages.md)

