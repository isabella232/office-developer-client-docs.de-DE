---
title: Herunterfahren eines Nachrichtenanbieters Store
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
# <a name="shutting-down-a-message-store-provider"></a>Herunterfahren eines Nachrichtenanbieters Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Ihr Anbieter ein Nachrichtenspeicheranbieter ist, kann er auf eine der folgenden Arten heruntergefahren werden:
  
- Wenn ein Client oder der MAPI-Spooler [IMsgStore::StoreLogoff aufruft.](imsgstore-storelogoff.md) Das Herunterfahren eines Nachrichtenspeicheranbieters mit **StoreLogoff** führt dazu, dass das Herunterfahren auf geordnete und kontrollierte Weise erfolgt. 
    
- Wenn ein Client [IMAPISession::Logoff aufruft.](imapisession-logoff.md) 
    
Ihre Implementierung von **IMsgStore::StoreLogoff** sollte zunächst [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) aufrufen, um MAPI darüber zu informieren, dass es heruntergefahren wird, was angibt, dass alle zugehörigen Transportanbieter abgemeldet werden sollten. Wenn **IMsgStore::StoreLogoff** zurückgegeben wird, ruft der Aufrufer die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) ihres Nachrichtenspeichers auf. Implementieren Sie **diese Release-Methode,** indem Sie die **IUnknown::Release-Methode des Supportobjekts** aufrufen. 
  
MAPI führt die folgenden Aufgaben in der Implementierung von **IUnknown::Release für** Nachrichtenspeicher aus: 
  
1. Entfernt alle vom Nachrichtenspeicheranbieter registrierten [MAPIUID-Strukturen.](mapiuid.md) 
    
2. Entfernt die Zeile des Nachrichtenspeicheranbieters aus der Statustabelle.
    
3. Ruft [IMSLogon::Logoff auf,](imslogon-logoff.md) um alle geöffneten Objekte, Unterobjekte und Statusobjekte frei zu geben. 
    
4. Ruft [IUnknown::Release auf,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) um das Anmeldeobjekt des Nachrichtenspeicheranbieters frei zu geben. 
    
Einige Clients können den Aufruf von **IMsgStore::StoreLogoff** auslassen und das Herunterfahren Ihres Nachrichtenspeicheranbieters mit dem Aufruf der **IUnknown::Release-Methode** des Nachrichtenspeichers initiieren. Ein Herunterfahren unter diesen Umständen ohne den Aufruf von **StoreLogoff** ist weniger geordnet und gesteuert. Schreiben Sie die **Release-Methode** Ihres Nachrichtenspeichers, um diese Möglichkeit zu behandeln und zu verfolgen, ob ein Aufruf von **IMAPISupport::StoreLogoffTransports** stattgefunden hat. **StoreLogoffTransports** muss während des Herunterfahrens einmal aufgerufen werden. Wenn Sie in Ihrer **Release-Methode** feststellen, dass **StoreLogoffTransports** noch nicht aufgerufen wurde, rufen Sie es mit dem Flag LOGOFF_ABORT auf. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md)

