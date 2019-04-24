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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283086"
---
# <a name="saving-mapi-properties"></a>Speichern von MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Objekte unterstützen ein Transaktionsmodell der Verarbeitung, wodurch Änderungen an Eigenschaften nicht dauerhaft vorgenommen werden, bis Sie zu einem späteren Zeitpunkt ein Commit ausgeführt werden. Während Änderungen an Eigenschaften von den [IMAPIProp::](imapiprop-setprops.md) SetProps-und [IMAPIProp::D-eleteprops](imapiprop-deleteprops.md) -Methoden verarbeitet werden, wird der Commit-Schritt von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)verarbeitet. Erst nach einem erfolgreichen Aufruf von SaveChanges **** kann auf die neueste Version der Eigenschaften eines Objekts zugegriffen werden. 
  
Wenn **SaveChanges** den Fehlerwert MAPI_E_OBJECT_CHANGED zurückgibt, ist dies eine Warnung, dass ein anderer Client gleichzeitig Änderungen an dem Objekt ausführt. Abhängig vom Anbieter, der das Objekt implementiert, ist es möglich, dass mehrere Clients ein Objekt erfolgreich öffnen, indem Sie die **OpenEntry** -Methode mit dem MAPI_MODIFY-Flag-Satz aufrufen, um Ihnen Lese-/Schreibzugriff zu erteilen. Das Objekt, das von einem solchen **OpenEntry** -Aufruf zurückgegeben wird, ist eine Momentaufnahme der Speicherdaten. Jeder nachfolgende Versuch, diese Daten zu ändern, kann den vorherigen Versuch überschreiben. 
  
Wenn Sie MAPI_E_OBJECT_CHANGED von **SaveChanges**empfangen, hat der Client folgende Möglichkeiten: 
  
- Erstellen Sie eine Kopie des Objekts, um die Änderungen zu speichern.
    
- Führen Sie einen weiteren **** Aufruf von SaveChanges aus, und geben Sie FORCE_SAVE. 
    
Das **** Aufrufen von SaveChanges mit dem FORCE_SAVE-Flag überschreibt den vorherigen Speicher und macht die Änderungen eines Clients dauerhaft. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

