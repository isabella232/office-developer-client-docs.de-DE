---
title: Herunterfahren eines Nachrichtenanbieters Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98de0a59b3b3526a69d4c75fef4bc453ce122dbe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624223"
---
# <a name="shutting-down-a-message-store-provider"></a>Herunterfahren eines Nachrichtenanbieters Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Ihr Anbieter ein Nachrichtenspeicheranbieter ist, kann er auf eine der folgenden Arten heruntergefahren werden:
  
- Wenn ein Client oder der MAPI-Spooler [IMsgStore::StoreLogoff aufruft.](imsgstore-storelogoff.md) Das Herunterfahren eines Nachrichtenspeicheranbieters mit **StoreLogoff** bewirkt, dass das Herunterfahren ordnungsgemäß und kontrolliert erfolgt. 
    
- Wenn ein Client [IMAPISession::Logoff aufruft.](imapisession-logoff.md) 
    
Ihre Implementierung von **IMsgStore::StoreLogoff** sollte beginnen, indem [SIE IMAPISupport::StoreLogoffTransports aufruft,](imapisupport-storelogofftransports.md) um die MAPI darüber zu informieren, dass sie heruntergefahren wird, was angibt, dass alle zugehörigen Transportanbieter abgemeldet werden sollen. Wenn **IMsgStore::StoreLogoff** zurückgegeben wird, ruft der Aufrufer die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) Ihres Nachrichtenspeichers auf. Implementieren Sie diese **Release-Methode,** indem Sie die **IUnknown::Release-Methode** des Supportobjekts aufrufen. 
  
MAPI führt die folgenden Aufgaben in der Implementierung von **IUnknown::Release** für Nachrichtenspeicher aus: 
  
1. Entfernt alle [MAPIUID-Strukturen,](mapiuid.md) die vom Nachrichtenspeicheranbieter registriert wurden. 
    
2. Entfernt die Zeile des Nachrichtenspeicheranbieters aus der Statustabelle.
    
3. Ruft [IMSLogon::Logoff](imslogon-logoff.md) auf, um alle geöffneten Objekte, Unterobjekte und Statusobjekte freizugeben. 
    
4. Ruft [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) auf, um das Anmeldeobjekt des Nachrichtenspeicheranbieters freizugeben. 
    
Einige Clients lassen möglicherweise den Aufruf von **IMsgStore::StoreLogoff** aus und initiieren das Herunterfahren des Nachrichtenspeicheranbieters mit dem Aufruf der **IUnknown::Release-Methode** des Nachrichtenspeichers. Ein Herunterfahren unter diesen Umständen ohne den Aufruf von **StoreLogoff** ist weniger ordnungsgemäß und weniger kontrolliert. Schreiben Sie die **Release-Methode** Ihres Nachrichtenspeichers, um diese Möglichkeit zu behandeln, und verfolgen Sie, ob ein Aufruf von **IMAPISupport::StoreLogoffTransports** aufgetreten ist. **StoreLogoffTransports** muss während des Herunterfahrens einmal aufgerufen werden. Wenn Sie in Ihrer **Release-Methode** erkennen, dass **StoreLogoffTransports** noch nicht aufgerufen wurde, rufen Sie es mit dem flag LOGOFF_ABORT auf. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md)

