---
title: Übertragen und Kopieren benannter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437777"
---
# <a name="transmitting-and-copying-named-properties"></a>Übertragen und Kopieren benannter Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine benannte Eigenschaft gesendet, verschoben oder kopiert wird, bleibt der Name konstant, aber der Bezeichner muss geändert werden, um der Zuordnung des Zielobjekts zuzuordnen. Die einzige Ausnahme von dieser Regel ist, wenn Die Quelle und das Ziel dieselbe Zuordnungssignatur haben, wodurch die Neuzuordnung nicht erforderlich ist.
  
Es liegt in der Verantwortung des Transportanbieters, die Namen der übertragenen benannten Eigenschaften den entsprechenden Bezeichnern neu zu karten, die am Ziel funktionieren. Der sendende Transportanbieter kann nicht wissen, was die richtige Zuordnung am Ziel ist. Sie muss die Namen übertragen und sich auf den empfangenden Transportanbieter verlassen, um sie den bezeichnern zu zuordnungen, die funktionieren. Die MAPI-Implementierung von TNEF behandelt die Neuzuordnung benannter Eigenschaften für Transportanbieter. Transportanbieter können die Neuanweisung entweder manuell verarbeiten oder die TNEF-Implementierung verwenden. 
  
Eine ähnliche Neuappierung benannter Eigenschaften muss auftreten, wenn diese Eigenschaften zwischen Nachrichtenspeichern kopiert werden. Da Nachrichtenspeicheranbieter jedoch die Zuordnung des Namens zum Bezeichner des Ziels abrufen können, können sie die Eigenschaften sofort neu zuordnen und müssen sich nicht auf den Zielnachrichtenspeicher verlassen. 
  
## <a name="see-also"></a>Siehe auch



[Benannte Eigenschaften MAPI](mapi-named-properties.md)

