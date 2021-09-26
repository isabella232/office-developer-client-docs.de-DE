---
title: Speichern von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2db022929516caa6b0aaad96d8e1997b70249546
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599081"
---
# <a name="saving-mapi-properties"></a>Speichern von MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Objekte unterstützen ein Transaktionsmodell der Verarbeitung, bei dem Änderungen an Eigenschaften erst dauerhaft vorgenommen werden, wenn zu einem späteren Zeitpunkt ein Commit ausgeführt wird. Während Änderungen an Eigenschaften von den Methoden [IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) verarbeitet werden, wird der Commitschritt von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)behandelt. Erst nach einem erfolgreichen Aufruf von **SaveChanges** kann auf die neueste Version der Eigenschaften eines Objekts zugegriffen werden. 
  
Wenn **SaveChanges** den Fehlerwert MAPI_E_OBJECT_CHANGED zurückgibt, ist dies eine Warnung, dass ein anderer Client gleichzeitig einen Commit für Änderungen an dem Objekt vorgibt. Abhängig vom Anbieter, der das Objekt implementiert, ist es möglich, dass mehrere Clients ein Objekt erfolgreich öffnen, indem sie seine **OpenEntry-Methode** aufrufen, wobei das MAPI_MODIFY-Kennzeichen festgelegt ist, sodass sie Lese-/Schreibzugriff erhalten. Das Objekt, das von einem solchen **OpenEntry-Aufruf** zurückgegeben wird, ist eine Momentaufnahme der Speicherdaten. Jeder nachfolgende Versuch, diese Daten zu ändern, kann den vorherigen Versuch überschreiben. 
  
Wenn ein Client MAPI_E_OBJECT_CHANGED von **SaveChanges empfängt,** hat er folgende Optionen: 
  
- Erstellen Sie eine Kopie des Objekts, um die Änderungen zu speichern.
    
- Führen Sie einen weiteren Aufruf von **SaveChanges** durch, und geben Sie FORCE_SAVE an. 
    
Durch Aufrufen von **SaveChanges** mit dem flag FORCE_SAVE wird das vorherige Speichern überschrieben, und die Änderungen eines Clients werden dauerhaft. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

