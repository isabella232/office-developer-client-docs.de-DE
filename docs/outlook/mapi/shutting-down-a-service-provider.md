---
title: Herunterfahren eines Dienstanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: fe0e4ff369c35f4df1b120528ff3ada7ef8d34e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624216"
---
# <a name="shutting-down-a-service-provider"></a>Herunterfahren eines Dienstanbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Client die [IMAPISession::Logoff-Methode](imapisession-logoff.md) aufruft, um die Sitzung zu beenden und alle aktiven Dienstanbieter herunterzufahren, ruft MAPI wiederum die folgenden Methoden auf: 
  
- [IABLogon::Logoff](iablogon-logoff.md) für Adressbuchanbieter. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) für Nachrichtenspeicheranbieter. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) für Transportanbieter. 
    
Diese Methoden haben ähnliche Implementierungen. Die wichtigsten Aufgaben, die eine Abmeldemethode ausführt, sind:
  
- Freigeben aller geöffneten Objekte, einschließlich Unterobjekten und Statusobjekten.
    
- Aufrufen der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) des Supportobjekts zum Dekrementieren der Referenzanzahl. 
    
- Entfernen aller registrierten [MAPIUID-Strukturen](mapiuid.md) Ihres Anbieters. 
    
- Entfernen der Zeile des Anbieters in der Statustabelle.
    
- Ausführen von Aufgaben, die sich auf das Bereinigen von Ressourcen beziehen, z. B. die folgenden:
    
  - Beenden einer Verbindung mit einem Remoteserver.
    
  - Dekrementieren der Referenzanzahl für das Anmeldeobjekt.
    
  - Entfernen des Anmeldeobjekts aus der Liste der Anmeldeobjekte, die ihr Anbieter speichert.
    
  - Geben Sie im Debugmodus Ablaufverfolgungen aus, um Objekte zu finden, bei denen Speicher verloren geht.
    
Wenn die Abmeldemethode zurückgegeben wird, ruft MAPI Folgendes auf:
  
- Die **IUnknown::Release-Methode** ihres Anmeldeobjekts. 
    
- **Die Shutdown-Methode** des Anbieterobjekts, um alle endgültigen Bereinigungsaufgaben auszuführen. Je nach Anbietertyp wird eine der folgenden Methoden aufgerufen: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) für Adressbuchanbieter 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) für Nachrichtenspeicheranbieter 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) für Transportanbieter 
    
- Die **IUnknown::Release-Methode** ihres Anbieterobjekts. 
    
Wenn Ihr Anbieter ein Nachrichtenspeicher ist, wird durch einen Clientaufruf von [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) auch der Vorgang zum Herunterfahren initiiert. **StoreLogoff** beendet einen bestimmten Nachrichtenspeicheranbieter und hat keine Auswirkungen auf die Sitzung. Mit dieser Methode kann nur ein Nachrichtenspeicheranbieter heruntergefahren werden. Es gibt keine explizite Möglichkeit zum Herunterfahren eines bestimmten Adressbuchs oder Transportanbieters. Informationen zum Reagieren auf einen **StoreLogoff-Anruf** finden Sie unter [Herunterfahren eines Nachrichtenanbieters Store .](shutting-down-a-message-store-provider.md)
  
Die DLL Ihres Anbieters wird entladen, wenn DIE MAPI die Win32-API-Funktion **FreeLibrary** aufruft, ein Aufruf, der erfolgt, nachdem der letzte aktive Client [MAPIUninitialize](mapiuninitialize.md)aufgerufen hat. Zu diesem Zeitpunkt ist das Herunterfahren des Dienstanbieters beendet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

