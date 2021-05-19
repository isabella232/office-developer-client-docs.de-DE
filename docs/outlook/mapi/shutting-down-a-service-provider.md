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
  
Wenn ein Client die [IMAPISession::Logoff-Methode](imapisession-logoff.md) aufruft, um die Sitzung zu beenden und alle aktiven Dienstanbieter herunterfahren, ruft MAPI wiederum die folgenden Methoden auf: 
  
- [IABLogon::Logoff](iablogon-logoff.md) für Adressbuchanbieter. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) für Nachrichtenspeicheranbieter. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) für Transportanbieter. 
    
Diese Methoden haben ähnliche Implementierungen. Die wichtigsten Aufgaben, die eine Abmeldemethode ausführt, sind:
  
- Freigeben aller geöffneten Objekte, einschließlich Unterobjekten und Statusobjekten.
    
- Aufrufen der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) des Supportobjekts, um die Referenzanzahl zu dekrementieren. 
    
- Entfernen aller registrierten [MAPIUID-Strukturen](mapiuid.md) Ihres Anbieters. 
    
- Entfernen der Zeile Ihres Anbieters in der Statustabelle.
    
- Ausführen von Aufgaben im Zusammenhang mit dem Bereinigen von Ressourcen, z. B.:
    
  - Beenden einer Verbindung mit einem Remoteserver.
    
  - Dekrementieren der Referenzanzahl für das Anmeldeobjekt.
    
  - Entfernen des Anmeldeobjekts aus der Liste der Anmeldeobjekte, die ihr Anbieter speichert.
    
  - Im Debugmodus werden Ablaufverfolgungen zum Auffinden von Objekten mit speicherleckiertem Speicher ausstellen.
    
Wenn Ihre Abmeldemethode zurückgegeben wird, ruft MAPI Folgendes auf:
  
- Die **IUnknown::Release-Methode** des Anmeldeobjekts. 
    
- Die Shutdown-Methode des **Anbieterobjekts,** um alle endgültigen Bereinigungsaufgaben auszuführen. Je nach Anbietertyp wird eine der folgenden Methoden aufgerufen: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) für Adressbuchanbieter 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) für Nachrichtenspeicheranbieter 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) für Transportanbieter 
    
- Die **IUnknown::Release-Methode** Ihres Anbieterobjekts. 
    
Wenn es sich bei Ihrem Anbieter um einen Nachrichtenspeicher handelt, initiiert ein Clientaufruf an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) auch den Herunterfahrensprozess. **StoreLogoff** beendet einen bestimmten Nachrichtenspeicheranbieter und hat keine Auswirkung auf die Sitzung. Mit dieser Methode kann nur ein Nachrichtenspeicheranbieter heruntergefahren werden. Es gibt keine explizite Möglichkeit zum Herunterfahren eines bestimmten Adressbuchs oder Transportanbieters. Informationen zum Reagieren auf einen **StoreLogoff-Anruf** finden Sie unter [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).
  
Die DLL Ihres Anbieters wird entladen, wenn MAPI die Win32-API-Funktion **FreeLibrary** aufruft, ein Aufruf, der ausgeführt wird, nachdem der letzte aktive Client [MAPIUninitialize aufgerufen hat.](mapiuninitialize.md) Bis zu diesem Zeitpunkt ist das Herunterfahren des Dienstanbieters beendet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

