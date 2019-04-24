---
title: Herunterfahren eines Nachrichtenspeicher Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339200"
---
# <a name="shutting-down-a-message-store-provider"></a>Herunterfahren eines Nachrichtenspeicher Anbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn es sich bei Ihrem Anbieter um einen Nachrichtenspeicher Anbieter handelt, kann er auf eine der folgenden Arten heruntergefahren werden:
  
- Wenn ein Client oder der MAPI-Spooler [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md)aufruft. Das Herunterfahren eines Nachrichtenspeicher Anbieters mit **StoreLogoff** bewirkt, dass das Herunterfahren auf geordnete und kontrollierte Weise erfolgt. 
    
- Wenn ein Client [IMAPISession:: Logoff](imapisession-logoff.md)aufruft. 
    
Die Implementierung von **IMsgStore:: StoreLogoff** sollte zunächst [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) aufrufen, um MAPI zu informieren, dass Sie heruntergefahren wird, was darauf hinweist, dass alle zugehörigen Transportanbieter abgemeldet werden sollen. Wenn **IMsgStore:: StoreLogoff** zurückgegeben wird, ruft der Aufrufer die [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode des Nachrichtenspeichers auf. Implementieren Sie diese **Release** -Methode, indem Sie die **IUnknown:: Release** -Methode des Support-Objekts aufrufen. 
  
MAPI führt die folgenden Aufgaben in der Implementierung von **IUnknown:: Release** für Nachrichtenspeicher aus: 
  
1. Entfernt alle vom Nachrichtenspeicher Anbieter registrierten [MAPIUID](mapiuid.md) -Strukturen. 
    
2. Entfernt die Zeile des Nachrichtenspeicher Anbieters aus der Statustabelle.
    
3. Ruft [IMSLogon:: Logoff](imslogon-logoff.md) auf, um alle geöffneten Objekte, unter Objekte und Statusobjekte zu veröffentlichen. 
    
4. Ruft [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) auf, um das Anmeldeobjekt des Nachrichtenspeicher Anbieters zu veröffentlichen. 
    
Einige Clients können den Aufruf von **IMsgStore:: StoreLogoff**weglassen, indem Sie das Herunterfahren des Nachrichtenspeicher Anbieters mit dem Aufruf der **IUnknown:: Release** -Methode des Nachrichtenspeichers initiieren. Ein Herunterfahren unter diesen Umständen ohne den Aufruf von **StoreLogoff** ist weniger geordnet und gesteuert. Schreiben Sie die **Release** -Methode des Nachrichtenspeichers, um diese Möglichkeit zu behandeln, und verfolgen Sie, ob ein Aufruf von **IMAPISupport:: StoreLogoffTransports** aufgetreten ist. **StoreLogoffTransports** muss beim Herunterfahren einmal aufgerufen werden. Wenn Sie in Ihrer **Release** -Methode feststellen, dass **StoreLogoffTransports** noch nicht aufgerufen wurde, rufen Sie Sie mit dem LOGOFF_ABORT-Flag auf. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md)

