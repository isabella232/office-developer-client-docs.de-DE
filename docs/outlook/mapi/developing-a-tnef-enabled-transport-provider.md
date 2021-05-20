---
title: Entwickeln eines TNEF-Enabled-Transportanbieters
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
# <a name="developing-a-tnef-enabled-transport-provider"></a>Entwickeln eines TNEF-Enabled-Transportanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um die Interoperabilität zwischen Messagingsystemen zu fördern, die unterschiedliche Sätze von MAPI-Features unterstützen, bietet MAPI das Transport Neutral Encapsulation Format (TNEF) als Standard für die Übertragung von Daten. Dieses Format kapselt MAPI-Eigenschaften, die von einem zugrunde liegenden Messagingsystem nicht unterstützt werden, in einen binären Datenstrom, der zusammen mit der Nachricht übertragen werden kann, wenn ein Transportanbieter sie sendet. Der Transportanbieter, der die Nachricht empfängt, kann dann den binären Datenstrom decodieren, um alle Eigenschaften der ursprünglichen Nachricht abzurufen und sie clientanwendungen zur Verfügung zu stellen. Das Betriebsmodell für TNEF ist:
  
- Messagingclients senden und empfangen Nachrichten wie gewohnt an einen TNEF-Transport.
    
- Der Transport trennt die Eigenschaften ausgehender Nachrichten in zwei Kategorien: die Eigenschaften, die vom zugrunde liegenden Nachrichtensystem unterstützt werden, und die Eigenschaften, die nicht unterstützt werden. Die Werte der Eigenschaften, die vom zugrunde liegenden Messagingsystem unterstützt werden, werden in das erforderliche Format übersetzt.
    
- Der Transport verwendet die MAPI-TNEF-Methoden, um nicht unterstützte Eigenschaften in einen einzelnen Datenstrom zu codieren. Der Transport wandelt diesen Datenstrom dann mithilfe des Anlagenmodells des zugrunde liegenden Messagingsystems in eine spezielle Anlage für die ausgehende Nachricht um, bevor die Nachricht gesendet wird.
    
- Ein TNEF-aktivierter Transport, der eine solche Nachricht empfängt, führt zwei Dinge aus. Zunächst werden die Eigenschaften der eingehenden Nachricht – die vom zugrunde liegenden Nachrichtensystem unterstützten – in MAPI-Eigenschaften übersetzt. Wenn die spezielle Anlage vorhanden ist, verwendet sie die MAPI-TNEF-Methoden, um zusätzliche MAPI-Eigenschaften aus der Anlage abzurufen, bevor die Nachricht an eine Clientanwendung gesendet wird.
    
MAPI stellt eine Implementierung der **ITnef-Schnittstelle** für die Verwendung durch MAPI-Transportanbieter bei der Arbeit mit TNEF-Objekten bereit. Die [OpenTnefStreamEx-Funktion](opentnefstreamex.md) wird verwendet, um TNEF-Objekte zu erstellen und sie einer Nachricht zuzuordnen. TNEF-Datenströme sind auf der OLE **IStream-Schnittstelle** aufgebaut 
  
> [!NOTE]
> Sie verwenden **OpenTnefStreamEx zum** Erstellen von TNEF-Objekten. Die alte **OpenTnefStream-Funktion** ist aus Kompatibilität mit dem alten Quellcode noch vorhanden und sollte nicht in neu verwendet werden. 
  
Die **ITnef-Schnittstelle** bietet die folgenden Methoden: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
Das MAPI-TNEF-Implementierungsmodell unterstützt:
  
- Alle MAPI-Eigenschaften ohne Auswirkungen auf andere Nachrichteneigenschaften. Damit MAPI-Nachrichten den Transport über ein Messagingsystem überstehen können, müssen alle Eigenschaften, die nicht als Eigenschaften des Messagingsystems codiert werden können, gekapselt werden. Da zum Zeitpunkt des Sendens einer Nachricht fast nie bekannt ist, ob ein MAPI-kompatibler Client die Nachricht erhält, ermöglicht das Kapselungsschema einem Transportanbieter, nur die MAPI-Nachrichteneigenschaften zu codieren, die vom Messagingsystem nicht nativ unterstützt werden. Dies bedeutet, dass Nachrichten, die TNEF verwenden, nicht "undurchsichtig" für Messagingsysteme sind, die nicht auf MAPI basieren, z. B. SMTP-basierte UNIX Messagingsysteme. Diese Systeme erhalten die von ihnen unterstützten Eigenschaften auf die für sie typische Art und Weise, und andere Eigenschaften werden als codierter TNEF-Datenstrom empfangen. Der TNEF-Transportanbieter ist dafür verantwortlich, zwischen diesen beiden Eigenschaftensätzen zu unterscheiden und den unterstützten Satz ordnungsgemäß für das Messagingsystem zu senden. TNEF geht nicht davon aus, wie viel Unterstützung von einem Messagingsystem bereitgestellt wird. In den Beispielen für die TNEF-Verwendung in diesem Abschnitt wird jedoch davon ausgegangen, dass das Messagingsystem neben der Nachricht mindestens eine anlage unterstützt. In einigen Fällen kann die Anlage nur über einen uuencoded stream unterstützt und als Teil des Nachrichtentexts übertragen werden. Nur in sehr seltenen Fällen hat das Messagingsystem so wenig Unterstützung für Nachrichteneigenschaften, dass eine vollständige TNEF-Codierung aller Eigenschaften erforderlich ist.
    
- Ein Mechanismus zum Bestimmen, ob ein #A0 für eine eingehende Nachricht zur Nachricht gehört, basierend auf der **#A1 PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Diese Eigenschaft sollte sowohl im TNEF-Stream als auch in einem entsprechenden Nachrichtenkopf gefunden werden. Wenn die Eigenschaft an beiden Stellen denselben Wert hat oder an beiden Stellen fehlt, wird davon ausgegangen, dass der TNEF-Stream zur Nachricht gehört. Andernfalls wird der TNEF-Stream ignoriert. TNEF-aktivierte Transporte sind für die Auswahl eines Werts für diese Eigenschaft für ausgehende Nachrichten und die Codierung in einem entsprechenden Nachrichtenkopf (z. B. der Message-ID: -Kopfzeile für SMTP-Nachrichten) und im TNEF-Stream verantwortlich.
    

