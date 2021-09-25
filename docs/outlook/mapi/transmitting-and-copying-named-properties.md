---
title: Übertragen und Kopieren benannter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9e040277b82c0a946fbb55907ce823301351c44f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578459"
---
# <a name="transmitting-and-copying-named-properties"></a>Übertragen und Kopieren benannter Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine benannte Eigenschaft gesendet, verschoben oder kopiert wird, bleibt der Name konstant, aber der Bezeichner muss geändert werden, um die Zuordnung des Zielobjekts einzuhalten. Die einzige Ausnahme von dieser Regel ist, wenn Die Quelle und das Ziel über die gleiche Zuordnungssignatur verfügen, sodass keine erneute Zuordnung erforderlich ist.
  
Es liegt in der Verantwortung des Transportanbieters, die Namen der übertragenen benannten Eigenschaften den entsprechenden Bezeichnern zuzuordnen, die am Ziel funktionieren. Der sendende Transportanbieter kann nicht wissen, was die richtige Zuordnung am Ziel ist. Er muss die Namen übertragen und sich darauf verlassen, dass der empfangende Transportanbieter diese Bezeichnern zuweist, die funktionieren. Die MAPI-Implementierung von TNEF übernimmt die Neuzuordnung benannter Eigenschaften für Transportanbieter. Transportanbieter können die Neuzuordnung manuell verarbeiten oder die TNEF-Implementierung verwenden. 
  
Eine ähnliche Neuzuordnung benannter Eigenschaften muss auftreten, wenn diese Eigenschaften zwischen Nachrichtenspeichern kopiert werden. Da Nachrichtenspeicheranbieter jedoch den Namen der Id-Zuordnung des Ziels abrufen können, können sie die Eigenschaften sofort neu zuordnen und müssen sich nicht auf den Zielnachrichtenspeicher verlassen. 
  
## <a name="see-also"></a>Siehe auch



[Benannte Eigenschaften MAPI](mapi-named-properties.md)

