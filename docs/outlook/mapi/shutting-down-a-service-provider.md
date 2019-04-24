---
title: Herunterfahren eines Dienstanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339207"
---
# <a name="shutting-down-a-service-provider"></a>Herunterfahren eines Dienstanbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Client die [IMAPISession:: Abmelde](imapisession-logoff.md) Methode aufruft, um die Sitzung zu beenden und alle aktiven Dienstanbieter herunterzufahren, ruft MAPI wiederum die folgenden Methoden auf: 
  
- [IABLogon:: Logoff](iablogon-logoff.md) für Adressbuchanbieter. 
    
- [IMSLogon:: Logoff](imslogon-logoff.md) für Nachrichtenspeicher Anbieter. 
    
- [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) für Transportanbieter. 
    
Diese Methoden weisen ähnliche Implementierungen auf. Die wichtigsten Aufgaben, die eine Abmelde Methode ausführt, lauten wie folgt:
  
- Freigeben aller geöffneten Objekte, einschließlich unter Objekte und Statusobjekte.
    
- Aufrufen der [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode des Support Objekts, um den Verweiszähler zu verringern. 
    
- Entfernen aller registrierten [MAPIUID](mapiuid.md) -Strukturen Ihres Anbieters. 
    
- Entfernen der Zeile des Anbieters in der Statustabelle.
    
- Ausführen von Aufgaben, die sich auf das Bereinigen von Ressourcen beziehen, wie etwa die folgenden:
    
  - Beenden einer Verbindung mit einem Remoteserver.
    
  - Dekrementieren der Verweisanzahl für das Logon-Objekt.
    
  - Entfernen des Anmelde Objekts aus der Liste der Anmeldeobjekte, die der Anbieter speichert.
    
  - Im Debugmodus werden Ablaufverfolgungen ausgegeben, um Objekte zu finden, die Speicherplatz verloren haben.
    
Wenn die Abmelde Methode zurückgegeben wird, ruft MAPI Folgendes auf:
  
- Die **IUnknown:: Release** -Methode des LOGON-Objekts. 
    
- Die **Shutdown** -Methode Ihres Provider-Objekts, um abschließende Aufräum Aufgaben auszuführen. Je nach Typ des Anbieters wird eine der folgenden Methoden aufgerufen: 
    
  - [IABProvider:: Herunterfahren](iabprovider-shutdown.md) für Adressbuchanbieter 
    
  - [IMSProvider:: Herunterfahren](imsprovider-shutdown.md) für Nachrichtenspeicher Anbieter 
    
  - [IXPProvider:: Herunterfahren](ixpprovider-shutdown.md) für Transportanbieter 
    
- Die **IUnknown:: Release** -Methode des Anbieterobjekts. 
    
Wenn Ihr Anbieter ein Nachrichtenspeicher ist, initiiert ein Clientaufruf von [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) auch den Shutdown-Prozess. **StoreLogoff** beendet einen bestimmten Nachrichtenspeicher Anbieter und hat keine Auswirkung auf die Sitzung. Nur ein Nachrichtenspeicher Anbieter kann mit dieser Methode heruntergefahren werden; Es gibt keine explizite Möglichkeit zum Herunterfahren eines bestimmten Adressbuchs oder Transportanbieters. Informationen zur Reaktion auf einen **StoreLogoff** -Anruf finden Sie unter [Herunterfahren eines Nachrichtenspeicher Anbieters](shutting-down-a-message-store-provider.md).
  
Die DLL Ihres Anbieters wird entladen, wenn MAPI die Win32-API-Funktion **FreeLibrary**aufruft, ein Aufruf, der nach dem letzten aktiven Client [MAPIUninitialize](mapiuninitialize.md)aufgerufen wird. Zu diesem Zeitpunkt wird der Dienstanbieter beendet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

