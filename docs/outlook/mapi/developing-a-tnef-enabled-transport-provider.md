---
title: Entwickeln eines TNEF-fähigen Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4d4f7ed75bb1144b7cd4a813b0d093246a30cca5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588349"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Entwickeln eines TNEF-fähigen Transportanbieters

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Um Interoperabilität zwischen Messagingsystemen zu fördern, die unterschiedliche Gruppen von MAPI-Funktionen zu unterstützen, stellt MAPI Transport Neutral Encapsulation Format (TNEF) als standard Möglichkeit zum Übertragen von Daten an. Dieses Format kapselt MAPI-Eigenschaften, die von einem zugrunde liegenden Messagingsystem in einen binären Datenstrom, der beim Senden eines Transportdienstes zusammen mit der Nachricht übertragen werden nicht unterstützt. Der Adressbuchhierarchie, die die Nachricht empfängt kann dann decodieren den binären Stream zum Abrufen aller Eigenschaften der ursprünglichen Nachricht und deren Clientanwendungen zur Verfügung zu stellen. Das betriebliche Modell für TNEF wird:
  
- Messaging-Clients senden und Empfangen von Nachrichten in einem TNEF Transport wie gewohnt.
    
- Das Übertragungsprotokoll trennt die Eigenschaften für ausgehende Nachrichten in zwei Kategorien:, die das zugrunde liegenden Nachrichtensystem unterstützt und Prozeduren, die es nicht der Fall ist. Die Werte der Eigenschaften, die von der zugrunde liegenden messaging-System unterstützt werden, werden in das erforderliche Format übersetzt.
    
- Der Transport verwendet die MAPI TNEF-Methoden zum Codieren von nicht unterstützten Eigenschaften in einen einzelnen Datenstrom. Das Übertragungsprotokoll verwandelt klicken Sie dann diesen Datenstrom Daten in eine spezielle Anlage die ausgehende Nachricht, die mithilfe des Objektmodells für die zugrunde liegenden messaging-System-Anlage, vor dem Senden der Nachricht.
    
- Ein Transport TNEF aktiviert, der eine solche Nachricht empfängt hat zwei Funktionen. Erstens übersetzt es der eingehenden Nachricht Eigenschaften – unterstützt werden vom zugrunde liegenden Nachrichtensystem – in MAPI-Eigenschaften. Zweitens Wenn spezielle Anlage vorhanden ist, verwendet er die MAPI TNEF-Methoden zum Abrufen von zusätzlicher MAPI-Eigenschaften aus der Anlage vor dem übermitteln der Nachricht an eine Clientanwendung.
    
MAPI stellt eine Implementierung der **ITnef** -Schnittstelle für die Verwendung von MAPI-Transport-Anbietern beim Arbeiten mit TNEF-Objekten. Die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion wird verwendet, um TNEF-Objekte erstellen und Zuordnen einer Nachricht. TNEF-Streams basieren auf der Basis der OLE- **IStream** -Schnittstelle 
  
> [!NOTE]
> Verwenden Sie **OpenTnefStreamEx** zum Erstellen von TNEF-Objekten. Die alte **OpenTNEFStream nicht ausgeführt werden** -Funktion noch vorhanden ist, für die Kompatibilität mit alten Quellcode und sollte nicht verwendet werden in einem anderen Element neu. 
  
Die **ITnef** -Schnittstelle stellt die folgenden Methoden bereit: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
Das Implementierungsmodell MAPI TNEF unterstützt:
  
- Alle MAPI-Eigenschaften wirkt sich weitere Nachrichteneigenschaften. In der Reihenfolge für MAPI-Nachrichten über einem messaging-System Transport überstehen müssen alle Eigenschaften, die als Eigenschaften des Messagingsystems codiert wird, können nicht gekapselte werden. Da fast nie zum Zeitpunkt bekannt ist, die eine Nachricht gesendet wird, unabhängig davon, ob ein MAPI-kompatibles Client die Meldung angezeigt wird, kann das Schema Kapselung ein Transportdienstes nur MAPI-Nachrichteneigenschaften zu codieren, die das messaging-System nicht der Fall ist systemintern unterstützt. Dies bedeutet, dass Nachrichten, die TNEF verwenden nicht "transparent" messaging-Systemen, die nicht auf MAPI wie UNIX SMTP-basierte messaging-Systeme. Diese Systeme erhalten die Eigenschaften, die sie unterstützen, in welcher Weise typisch ist für diese und andere Eigenschaften als eine codierte TNEF-Datenstrom empfangen werden. Der Transportdienst TNEF ist verantwortlich für die Unterscheidung zwischen diesen zwei Sätze von Eigenschaften und senden die unterstützte Gruppe in der richtigen Form für die messaging-System. TNEF Annahmen keine über die Ebene der Unterstützung von einem messaging-System aus. Jedoch ist in den Beispielen in diesem Abschnitt enthalten TNEF-Auslastung der Annahme ausgegangen, dass das messaging-System abgesehen davon, dass die Nachricht mindestens eine Anlage unterstützt. In einigen Fällen kann die Anlage nur über einen Datenstrom UUENCODE unterstützt und als Teil des Nachrichtentexts übertragen werden. Nur in seltenen Fällen müssen das messaging-System so wenig Unterstützung für Nachrichteneigenschaften, vollständige TNEF-Codierung alle Eigenschaften erforderlich ist.
    
- Ein Mechanismus zum Bestimmen basierend, ob ein TNEF-Stream auf eine eingehende Nachricht an die Nachricht gehört auf der MAPI-Eigenschaft **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Diese Eigenschaft sollte sowohl in der TNEF-Stream eine entsprechende Meldung-Kopfzeile gefunden werden. Wenn die-Eigenschaft denselben Wert an beiden Stellen hat oder an beiden Stellen fehlt, wird angenommen, dass der TNEF-Stream an die Nachricht gehören. Andernfalls wird der TNEF-Stream ignoriert. TNEF aktiviert Transporten sind verantwortlich für die Auswahl eines Wertes für diese Eigenschaft für ausgehende Nachrichten und codiert ihn in eine entsprechende Meldung-Kopfzeile (beispielsweise der Nachrichten-ID: Kopfzeile für SMTP-Nachrichten) und in der TNEF-Stream.
    

