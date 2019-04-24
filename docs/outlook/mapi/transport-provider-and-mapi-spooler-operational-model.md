---
title: Transport Anbieter und MAPI-Spooler-Betriebsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356609"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Transport Anbieter und MAPI-Spooler-Betriebsmodell

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Transportanbieter Initialisierung, Start, Verarbeitung, Herunterfahren und Deinitialisierung werden durch eine Reihe von Aufrufen vom MAPI-Spooler an den Transportanbieter durchgeführt. Die Anrufe werden wie folgt sequenziert:
  
1. Der MAPI-Spooler Ruft die [XPProviderInit](xpproviderinit.md) -Funktion auf, übergibt ein Support-Objekt, ruft das Anbieterobjekt ab und überprüft, ob der Transportanbieter und der MAPI-Spooler einen kompatiblen MAPI-Versions Nummerntyp unterstützen. 
    
2. Der MAPI-Spooler Ruft die [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) -Methode der [IXPProvider: IUnknown](ixpprovideriunknown.md) -Schnittstelle auf. Zwischen dem MAPI-Spooler und dem Transportanbieter wird eine Sitzung mit den Anmeldeinformationen im aktuellen Abschnitt des Profils eingerichtet. Der Transportanbieter gibt ein LOGON-Objekt zurück. 
    
3. Die MAPI-Warteschlange ruft die [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode auf. Der Transportanbieter gibt eine Liste der eindeutigen Bezeichner (IDs) und e-Mail-Adresstypen zurück, die er akzeptiert. 
    
4. Der Transportanbieter Ruft die [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode auf, um die Zeile in der MAPI-Statustabelle zu erstellen. 
    
5. Die MAPI-Warteschlange ruft die [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) -Methode auf, um die Nachrichtenübertragung und den Empfang zu aktivieren. 
    
6. Wenn der Transportanbieter in seiner Rückgabe für den **TransportLogon** -Aufruf angefordert wird, ruft der MAPI-Spooler in regelmäßigen Abständen die [IXPLogon:: idle](ixplogon-idle.md) -Methode auf. Die Leerlaufverarbeitung ist nützlich, wenn der Transportanbieter das zugrunde liegende Messagingsystem auf neue Nachrichten Abfragen oder andere Aufgaben mit niedriger Priorität ausführen muss. 
    
7. Die MAPI-Warteschlange und der Transportanbieter senden und empfangen Nachrichten. Weitere Informationen finden Sie unter [Nachrichten Übermittlungs Modell](message-submission-model.md) und [Nachrichtenempfangs Modell](message-reception-model.md). Die MAPI-Warteschlangendienste transportieren Anforderungen und Aufrufe für Support-, Message-und Attachment-Objekte.
    
8. Die MAPI-Warteschlange ruft die **TransportNotify** -Methode auf, um die Nachrichtenübertragung und den Empfang zu deaktivieren. 
    
9. Der MAPI-Spooler gibt die Objekte LOGON und Provider frei. Weitere Informationen finden Sie unter der [IXPProvider:: Shutdown](ixpprovider-shutdown.md) -Methode. 
    

