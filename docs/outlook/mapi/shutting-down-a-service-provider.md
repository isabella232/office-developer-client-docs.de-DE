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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395175"
---
# <a name="shutting-down-a-service-provider"></a>Herunterfahren eines Dienstanbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Client die [IMAPISession::Logoff](imapisession-logoff.md) -Methode ruft, um die Sitzung zu beenden und alle aktiven-Dienstanbieter heruntergefahren, ruft MAPI wiederum die folgenden Methoden: 
  
- [IABLogon::Logoff](iablogon-logoff.md) für adressbuchanbietern implementierte. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) für Nachricht-Anbieter. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) für Transportanbieter. 
    
Diese Methoden haben ähnliche Implementierungen. Die wichtigsten Aufgaben, die eine Abmeldung-Methode führt lauten wie folgt:
  
- Veröffentlichen alle geöffneten Objekte, einschließlich Unterobjekte und Status-Objekte.
    
- Aufrufen das Support-Objekt [IUnknown](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode, um die Anzahl der Verweise zu verringern. 
    
- Entfernen alle registrierten [MAPIUID](mapiuid.md) -Strukturen Ihres Anbieters. 
    
- Entfernen von Zeile des Anbieters in der Tabelle "Status".
    
- Ausführen von Aufgaben, die zum Bereinigen von Ressourcen, wie die folgenden beziehen:
    
  - Beenden einer Verbindung mit einem Remoteserver.
    
  - Verringern Sie den Verweis auf das Anmeldeobjekt zählen.
    
  - Entfernen des Anmeldung-Objekts aus der Liste der Logon-Objekten, die vom Dienstanbieter speichert.
    
  - Im Debugmodus ausstellen Spuren, um Objekte zu suchen, die Speicher verloren haben.
    
Wenn Ihre Abmeldung-Methode zurückgegeben wird, ruft MAPI Folgendes:
  
- Die Anmeldung des Objekts **IUnknown** -Methode. 
    
- Provider-Objekts **Shutdown** -Methode der endgültige Cleanup Aufgaben ausgeführt. Je nach Typ des vom Dienstanbieter wird eine der folgenden Methoden aufgerufen: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) für adressbuchanbietern implementierte 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) für Nachricht-Anbieter 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) für Transportanbieter 
    
- **IUnknown** -Methode der Provider-Objekt. 
    
Wenn der Anbieter einen Nachrichtenspeicher ist, wird ein Clientaufruf von [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) auch des Herunterfahrens initiieren. **StoreLogoff** Anbieter für eine bestimmte Nachricht anmelden heruntergefahren und hat keine Auswirkung auf die Sitzung. Mit dieser Methode kann nur eine Nachricht Speicheranbieter heruntergefahren werden; Es gibt keine explizite Möglichkeit zum Herunterfahren von eines bestimmten Adresse Adressbuch oder Transport Anbieters. [Herunterfahren nach unten einer Nachricht Speicheranbieter](shutting-down-a-message-store-provider.md)finden Sie Informationen zur Beantwortung einer **StoreLogoff** aufrufen ist.
  
DLL des Anbieters werden entfernt, wenn MAPI Win32 API-Funktion **FreeLibrary**, einen Anruf aufruft, der ausgeführt wird, nachdem der letzte aktive Client [MAPIUninitialize](mapiuninitialize.md)aufgerufen hat. Zu diesem Zeitpunkt wird Ihren Dienstanbieter abgeschlossen haben, wird beendet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

