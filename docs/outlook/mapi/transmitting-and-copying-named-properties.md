---
title: Übertragen und Kopieren von benannten Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c225712e354d72b79313ee4c3f36da55f11b0a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587516"
---
# <a name="transmitting-and-copying-named-properties"></a>Übertragen und Kopieren von benannten Eigenschaften

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn eine benannte Eigenschaft gesendet wird, verschoben oder kopiert haben, der Namen bleibt konstant, aber der Bezeichner muss ändern, um die Zuordnung der Zielobjekt entsprechen. Die einzige Ausnahme zu dieser Regel ist, wenn die Quell- und die gleiche Zuordnung Signatur haben Neuzuordnen unnötige vornehmen.
  
Es ist der Verantwortung der Adressbuchhierarchie, die Namen der übertragenen benannten Eigenschaften auf die entsprechende Bezeichner neu zuzuordnen, die an das Ziel arbeiten. Der sendenden Adressbuchhierarchie kann nicht wissen, was die korrekte Zuordnung am Ziel ist; Es muss die Namen übermitteln und hängen von der empfangenden Adressbuchhierarchie zu Bezeichner zuordnen, die funktionieren. Die MAPI-Implementierung von TNEF verarbeitet Neuzuordnen des benannten Eigenschaften für Transportanbieter. Transportanbieter können entweder behandeln Neuzuordnen manuell oder verwenden Sie die TNEF-Implementierung. 
  
Eine ähnliche Neuzuordnen des benannten Eigenschaften muss auftreten, wenn diese Eigenschaften zwischen Nachrichtenspeicher kopiert werden. Da Nachricht-Anbieter den Namen Bezeichner-Zuordnung, der das Ziel abrufen können, können sie jedoch dann sofort neu zuordnen die Eigenschaften und nicht auf dem Ziel-Nachrichtenspeicher verlassen haben. 
  
## <a name="see-also"></a>Siehe auch



[Benannte Eigenschaften MAPI](mapi-named-properties.md)

