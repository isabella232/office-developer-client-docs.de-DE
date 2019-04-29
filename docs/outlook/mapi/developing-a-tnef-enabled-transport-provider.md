---
title: Entwickeln eines TNEF-fähigen Transport Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 282b1866699b695c647caedd130ce5abc1bcbc2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439002"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Entwickeln eines TNEF-fähigen Transport Anbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zur Förderung der Interoperabilität zwischen Messagingsystemen, die unterschiedliche MAPI-Funktionen unterstützen, stellt MAPI das Transport Neutral Encapsulation Format (TNEF) als Standardmethode zum Übertragen von Daten bereit. Dieses Format kapselt MAPI-Eigenschaften, die nicht von einem zugrunde liegenden Messagingsystem unterstützt werden, in einen binären Datenstrom, der zusammen mit der Nachricht übertragen werden kann, wenn ein Transportanbieter Sie sendet. Der Transportanbieter, der die Nachricht empfängt, kann dann den binären Datenstrom decodieren, um alle Eigenschaften der ursprünglichen Nachricht abzurufen und für Clientanwendungen zur Verfügung zu stellen. Das Betriebsmodell für TNEF lautet:
  
- Messaging-Clients senden und empfangen Nachrichten wie gewohnt an einen TNEF-Transport.
    
- Der Transport trennt die Eigenschaften von ausgehenden Nachrichten in zwei Kategorien: die, die vom zugrunde liegenden Nachrichtensystem unterstützt werden, und die nicht. Die Werte der Eigenschaften, die vom zugrunde liegenden Messagingsystem unterstützt werden, werden in das erforderliche Format übersetzt.
    
- Der Transport verwendet die MAPI-TNEF-Methoden, um alle nicht unterstützten Eigenschaften in einem einzelnen Datenstrom zu codieren. Der Transport wandelt dann diesen Datenstrom in eine spezielle Anlage der ausgehenden Nachricht um, wobei das Anlagenmodell des zugrunde liegenden Messagingsystems verwendet wird, bevor die Nachricht gesendet wird.
    
- Ein TNEF-fähiger Transport, der eine solche Nachricht empfängt, hat zwei Möglichkeiten. Zunächst werden die Eigenschaften der eingehenden Nachricht, die vom zugrunde liegenden Nachrichtensystem unterstützt werden, in MAPI-Eigenschaften übersetzt. Zweitens verwendet es die MAPI-TNEF-Methoden, um zusätzliche MAPI-Eigenschaften aus der Anlage abzurufen, bevor die Nachricht an eine Clientanwendung übermittelt wird.
    
MAPI stellt eine Implementierung der **ITnef** -Schnittstelle zur Verwendung durch MAPI-Transportanbieter beim Arbeiten mit TNEF-Objekten bereit. Die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion wird verwendet, um TNEF-Objekte zu erstellen und diese einer Nachricht zuzuordnen. TNEF-Streams basieren auf der OLE **IStream** -Schnittstelle. 
  
> [!NOTE]
> Verwenden Sie **OpenTnefStreamEx** zum Erstellen von TNEF-Objekten. Die alte **OpenTnefStream** -Funktion ist weiterhin zur Kompatibilität mit altem Quellcode vorhanden und sollte in nichts neuem verwendet werden. 
  
Die **ITnef** -Schnittstelle stellt die folgenden Methoden bereit: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
Das MAPI-TNEF-Implementierungsmodell unterstützt:
  
- Alle MAPI-Eigenschaften ohne Auswirkungen auf andere Nachrichteneigenschaften. Damit MAPI-Nachrichten den Transport über ein Messagingsystem überstehen, müssen alle Eigenschaften gekapselt werden, die nicht als Eigenschaften des Messagingsystems codiert werden können. Da es fast nie zu dem Zeitpunkt bekannt ist, zu dem eine Nachricht gesendet wird, unabhängig davon, ob ein MAPI-kompatibler Client die Nachricht empfängt, ermöglicht das Kapselungs Schema einem Transportanbieter, nur die MAPI-Nachrichteneigenschaften zu codieren, die das Messagingsystem nicht nativ unterstützt. Dies führt dazu, dass Nachrichten, die TNEF verwenden, nicht für Messagingsysteme, die nicht auf MAPI basieren, wie SMTP-basierte UNIX-Messagingsysteme, undurchsichtig sind. Diese Systeme erhalten die Eigenschaften, die Sie unterstützen, in welcher Weise auch immer, und andere Eigenschaften werden als codierter TNEF-Datenstrom empfangen. Der TNEF-Transportanbieter ist für die Differenzierung zwischen diesen beiden Eigenschaftensätzen und dem Senden der unterstützten Gruppe für das Messagingsystem verantwortlich. TNEF stellt keine Annahmen hinsichtlich der von einem Messagingsystem bereitgestellten Unterstützungsstufe dar. In den Beispielen für die TNEF-Verwendung in diesem Abschnitt wird jedoch davon ausgegangen, dass das Messagingsystem mindestens eine einzelne Anlage neben der Nachricht unterstützt. In einigen Fällen kann die Anlage nur über einen UUEncode-Stream unterstützt und als Teil des Nachrichtentexts übertragen werden. Nur in sehr seltenen Fällen wird das Messagingsystem so wenig Unterstützung für Nachrichteneigenschaften haben, dass die vollständige TNEF-Codierung aller Eigenschaften erforderlich ist.
    
- Ein Mechanismus zum bestimmen, ob ein TNEF-Stream für eine eingehende Nachricht zu der Nachricht gehört, basierend auf der MAPI-Eigenschaft **PR_TNEF_CORRELATION_KEY** ([pidtagtnefcorrelationkey (](pidtagtnefcorrelationkey-canonical-property.md)). Diese Eigenschaft sollte sowohl im TNEF-Stream als auch in einem entsprechenden Nachrichtenkopf gefunden werden. Wenn die Eigenschaft an beiden Stellen denselben Wert aufweist oder fehlt, wird davon ausgegangen, dass der TNEF-Stream zur Nachricht gehört. Andernfalls wird der TNEF-Stream ignoriert. TNEF-aktivierte Übertragungen sind für die Auswahl eines Werts für diese Eigenschaft in ausgehenden Nachrichten und die Codierung in einem entsprechenden Nachrichtenkopf (beispielsweise der Message-ID:-Kopfzeile für SMTP-Nachrichten) und im TNEF-Datenstrom verantwortlich.
    

