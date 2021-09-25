---
title: Entwickeln eines TNEF-Enabled-Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30b61b1cd8645aa0fa0bc67e89507f1827ea8e95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584605"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Entwickeln eines TNEF-Enabled-Transportanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um die Interoperabilität zwischen Messagingsystemen zu fördern, die unterschiedliche MAPI-Features unterstützen, stellt MAPI das transportneutrale Kapselungsformat (Transport Neutral Encapsulation Format, TNEF) als Standardmethode zum Übertragen von Daten bereit. Dieses Format kapselt MAPI-Eigenschaften, die von einem zugrunde liegenden Messagingsystem nicht unterstützt werden, in einen binären Datenstrom, der zusammen mit der Nachricht übertragen werden kann, wenn sie von einem Transportanbieter gesendet wird. Der Transportanbieter, der die Nachricht empfängt, kann dann den binären Datenstrom decodieren, um alle Eigenschaften der ursprünglichen Nachricht abzurufen und für Clientanwendungen verfügbar zu machen. Das Betriebsmodell für TNEF lautet:
  
- Nachrichtenclients senden und empfangen Nachrichten wie gewohnt an einen TNEF-Transport.
    
- Durch den Transport werden die Eigenschaften für ausgehende Nachrichten in zwei Kategorien unterteilt: die Eigenschaften, die das zugrunde liegende Nachrichtensystem unterstützt, und die Eigenschaften, die nicht vom zugrunde liegenden Nachrichtensystem unterstützt werden. Die Werte der Eigenschaften, die vom zugrunde liegenden Messagingsystem unterstützt werden, werden in das erforderliche Format übersetzt.
    
- Der Transport verwendet die MAPI-TNEF-Methoden, um alle nicht unterstützten Eigenschaften in einem einzelnen Datenstrom zu codieren. Durch den Transport wird dieser Datenstrom dann mithilfe des Anlagenmodells des zugrunde liegenden Messagingsystems in eine spezielle Anlage für die ausgehende Nachricht umgewandelt, bevor die Nachricht gesendet wird.
    
- Ein TNEF-aktivierter Transport, der eine solche Nachricht empfängt, führt zwei Dinge aus. Zunächst werden die Eigenschaften der eingehenden Nachricht – diejenigen, die vom zugrunde liegenden Nachrichtensystem unterstützt werden – in MAPI-Eigenschaften übersetzt. Zweitens: Wenn die spezielle Anlage vorhanden ist, werden die MAPI-TNEF-Methoden verwendet, um zusätzliche MAPI-Eigenschaften aus der Anlage abzurufen, bevor die Nachricht an eine Clientanwendung bereitgestellt wird.
    
MAPI stellt eine Implementierung der **ITnef-Schnittstelle** für die Verwendung durch MAPI-Transportanbieter bei der Arbeit mit TNEF-Objekten bereit. Die [OpenTnefStreamEx-Funktion](opentnefstreamex.md) wird verwendet, um TNEF-Objekte zu erstellen und sie einer Nachricht zuzuordnen. TNEF-Datenströme basieren auf der OLE **IStream-Schnittstelle** 
  
> [!NOTE]
> Sie verwenden **OpenTnefStreamEx,** um TNEF-Objekte zu erstellen. Die alte **OpenTnefStream-Funktion** ist aus Gründen der Kompatibilität mit altem Quellcode weiterhin vorhanden und sollte in nichts Neuem verwendet werden. 
  
Die **ITnef-Schnittstelle** stellt die folgenden Methoden bereit: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
Das MAPI-TNEF-Implementierungsmodell unterstützt:
  
- Alle MAPI-Eigenschaften ohne Auswirkung auf andere Nachrichteneigenschaften. Damit MAPI-Nachrichten den Transport über ein Messagingsystem bestehen können, müssen alle Eigenschaften, die nicht als Eigenschaften des Messagingsystems codiert werden können, gekapselt werden. Da zu dem Zeitpunkt, zu dem eine Nachricht gesendet wird, fast nie bekannt ist, ob ein MAPI-kompatibler Client die Nachricht empfängt, ermöglicht das Kapselungsschema einem Transportanbieter, nur die MAPI-Nachrichteneigenschaften zu codieren, die das Messagingsystem nicht nativ unterstützt. Dies bedeutet, dass Nachrichten, die TNEF verwenden, für Messagingsysteme, die nicht auf MAPI basieren, nicht "undurchsichtig" sind, z. B. SMTP-basierte UNIX Messagingsysteme. Diese Systeme erhalten die von ihnen unterstützten Eigenschaften auf die für sie typische Weise, und andere Eigenschaften werden als codierter TNEF-Datenstrom empfangen. Der TNEF-Transportanbieter ist für die Unterscheidung zwischen diesen beiden Eigenschaftengruppen und das Senden des unterstützten Satzes auf die richtige Weise für das Messagingsystem verantwortlich. TNEF geht nicht davon aus, wie viel Unterstützung von einem Messagingsystem bereitgestellt wird. In den Beispielen für die TNEF-Verwendung in diesem Abschnitt wird jedoch davon ausgegangen, dass das Messagingsystem neben der Nachricht mindestens eine einzelne Anlage unterstützt. In einigen Fällen kann die Anlage nur über einen uu-codierten Datenstrom unterstützt und als Teil des Nachrichtentexts übertragen werden. Nur in sehr seltenen Fällen wird das Messagingsystem so wenig Unterstützung für Nachrichteneigenschaften haben, dass eine vollständige TNEF-Codierung aller Eigenschaften erforderlich ist.
    
- Ein Mechanismus zum Bestimmen, ob ein TNEF-Datenstrom für eine eingehende Nachricht zur Nachricht gehört, basierend auf der MAPI-Eigenschaft **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Diese Eigenschaft sollte sowohl im TNEF-Stream als auch in einem entsprechenden Nachrichtenkopf gefunden werden. Wenn die Eigenschaft an beiden Stellen denselben Wert aufweist oder an beiden Stellen fehlt, wird angenommen, dass der TNEF-Datenstrom zur Nachricht gehört. Andernfalls wird der TNEF-Stream ignoriert. TNEF-aktivierte Transporte sind dafür verantwortlich, einen Wert für diese Eigenschaft für ausgehende Nachrichten auszuwählen und in einem entsprechenden Nachrichtenkopf (z. B. der Nachrichten-ID: Header für SMTP-Nachrichten) und im TNEF-Stream zu codieren.
    

