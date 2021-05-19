---
title: Speichern von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425890"
---
# <a name="saving-mapi-properties"></a>Speichern von MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Objekte unterstützen ein Transaktionsmodell der Verarbeitung, bei dem Änderungen an Eigenschaften erst dann dauerhaft vorgenommen werden, wenn sie zu einem späteren Zeitpunkt ausgeführt werden. Während Änderungen an Eigenschaften von den [Methoden IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) behandelt werden, wird der Commitschritt von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)verarbeitet. Erst nach einem erfolgreichen Aufruf von **SaveChanges** kann auf die neueste Version der Eigenschaften eines Objekts zugegriffen werden. 
  
Wenn **SaveChanges** den Fehlerwert MAPI_E_OBJECT_CHANGED, ist dies eine Warnung, dass ein anderer Client gleichzeitig Änderungen am Objekt übergibt. Je nach Anbieter, der das Objekt implementieren kann, können mehrere Clients ein Objekt erfolgreich öffnen, indem sie die **OpenEntry-Methode** mit dem MAPI_MODIFY-Flag-Set aufrufen und ihnen Lese-/Schreibzugriff geben. Das Objekt, das von einem solchen **OpenEntry-Aufruf** zurückgegeben wird, ist eine Momentaufnahme der Speicherdaten. Jeder nachfolgende Versuch, diese Daten zu ändern, kann den vorherigen Versuch überschreiben. 
  
Nach dem MAPI_E_OBJECT_CHANGED **von SaveChanges** hat ein Client die Möglichkeit, 
  
- Erstellen Sie eine Kopie des Objekts, um die Änderungen zu speichern.
    
- Rufen Sie **SaveChanges erneut auf,** und geben Sie FORCE_SAVE. 
    
Durch das Aufrufen von **SaveChanges** mit FORCE_SAVE-Flag wird das vorherige Speichern überschrieben, und die Änderungen eines Clients werden dauerhaft. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

