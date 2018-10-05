---
title: Herunterfahren eines Nachrichtenspeicheranbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386054"
---
# <a name="shutting-down-a-message-store-provider"></a>Herunterfahren eines Nachrichtenspeicheranbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn der Anbieter einen Anbieter für die Nachricht Anmelden ist, kann es in einem der folgenden Methoden heruntergefahren werden:
  
- Wenn ein Client oder die MAPI-Warteschlange [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)aufruft. Beenden einer Nachricht Store-Anbieters mit **StoreLogoff** bewirkt, dass das Herunterfahren ein ordnungsgemäßes und gesteuerte Weise erfolgen. 
    
- Wenn ein Client [IMAPISession::Logoff](imapisession-logoff.md)aufruft. 
    
Durch Aufrufen von [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) um MAPI zu informieren, dass es heruntergefahren wird, der angibt, dass alle verknüpften Transportanbieter sollen, deaktivieren protokolliert werden, sollte die Implementierung von **IMsgStore::StoreLogoff** beginnen. Wenn **IMsgStore::StoreLogoff** zurückgegeben wird, wird der Aufrufer des Nachrichtenspeichers [IUnknown](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode aufgerufen. Implementieren Sie diese **Version** -Methode, durch die des Unterstützungsobjekts **IUnknown** -Methode aufrufen. 
  
MAPI führt die folgenden Aufgaben bei der Implementierung der **IUnknown** für Nachrichtenspeicher: 
  
1. Entfernt alle der [MAPIUID](mapiuid.md) Strukturen vom Anbieter Store Nachricht registriert. 
    
2. Entfernt die Nachricht Speicheranbieter Zeile aus der Tabelle "Status".
    
3. Ruft die [IMSLogon::Logoff](imslogon-logoff.md) , um alle geöffneten Objekte, Unterobjekte und Status Objekte freizugeben. 
    
4. Ruft die [IUnknown](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , um die Nachricht Speicheranbieter Anmeldung-Objekt freizugeben. 
    
Einige Clients können ausgelassen werden, den Anruf an **IMsgStore::StoreLogoff**, das Herunterfahren des Anbieters Ihrer Nachricht mit dem Aufruf der Nachrichtenspeicher **IUnknown** -Methode. Ein Herunterfahren unter diesen Umständen ohne den Aufruf von **StoreLogoff** ist kleiner ordnungsgemäßes und kontrolliert. Schreiben des Nachrichtenspeichers **Release** -Methode, um diese Möglichkeit behandeln und Nachverfolgen der unabhängig davon, ob ein Aufruf von **IMAPISupport::StoreLogoffTransports** aufgetreten ist. **StoreLogoffTransports** muss einmal während des Herunterfahrens aufgerufen werden. Wenn Sie in der **Version** -Methode erkennen, dass **StoreLogoffTransports** noch nicht aufgerufen wurde, können rufen sie mit dem LOGOFF_ABORT-Flag auf. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md)

