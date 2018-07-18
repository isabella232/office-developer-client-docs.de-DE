---
title: Speichern von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795418"
---
# <a name="saving-mapi-properties"></a>Speichern von MAPI-Eigenschaften

  
  
**Betrifft**: Outlook 
  
Viele Objekte unterstützen eine Transaktionsmodell der Verarbeitung bei dem Eigenschaften nicht permanent geändert werden, bis sie zu einem späteren Zeitpunkt übernommen werden. Während die Änderungen an Eigenschaften von den Methoden [IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) behandelt werden, wird der Schritt Commit von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)behandelt. Es ist nicht erst nach einem erfolgreichen Aufruf von **SaveChanges** , dass die aktuellste Version von Eigenschaften eines Objekts zugegriffen werden kann. 
  
Wenn **SaveChanges** den Fehlerwert MAPI_E_OBJECT_CHANGED zurückgegeben wird, ist dies eine Warnung, dass ein anderer Client gleichzeitig Änderungen auf das Objekt übergeben wird. Es ist möglich, und öffnen je nach der Anbieter das Objekt erfolgreich für mehrere Clients zum Implementieren eines Objekts durch Aufrufen seiner **OpenEntry** -Methode mit der MAPI_MODIFY-Flag, Gewähren von Lese-/Schreibzugriff. Das Objekt, das solcher zurückgegeben wird, dass ein Anruf **OpenEntry** eine Momentaufnahme der Speicherdaten ist. Jedem nachfolgenden Versuch, diese Daten ändern kann vorherige Versuch zu überschreiben. 
  
Beimkontakt MAPI_E_OBJECT_CHANGED aus **SaveChanges**, muss der Client die Option aus, um: 
  
- Erstellen Sie eine Kopie des Objekts, um die Änderungen zu halten.
    
- Stellen Sie einen weiteren Anruf zu **SaveChanges**, FORCE_SAVE angeben. 
    
Durch den Aufruf von **SaveChanges** das Flag FORCE_SAVE überschreibt das vorherige speichern ein und ändert ein Client dauerhaft entfernt. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

