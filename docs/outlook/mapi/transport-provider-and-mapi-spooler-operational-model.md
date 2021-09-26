---
title: Transportanbieter- und MAPI-Spooler-Betriebsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9613c46ee105d24317c6c902f8d5f122cf4689cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619596"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Transportanbieter- und MAPI-Spooler-Betriebsmodell

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisierung, Start, Verarbeitung, Herunterfahren und Initialisierung des Transportanbieters werden durch eine Reihe von Aufrufen des MAPI-Spoolers an den Transportanbieter ausgeführt. Die Aufrufe werden wie folgt sequenziert:
  
1. Der MAPI-Spooler ruft die [XPProviderInit-Funktion](xpproviderinit.md) auf, übergibt ein Supportobjekt, ruft das Anbieterobjekt ab und überprüft, ob der Transportanbieter und der MAPI-Spooler einen kompatiblen Bereich von MAPI-Versionsnummern unterstützen. 
    
2. Der MAPI-Spooler ruft die [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) der [IXPProvider : IUnknown-Schnittstelle](ixpprovideriunknown.md) auf. Zwischen dem MAPI-Spooler und dem Transportanbieter wird eine Sitzung mit den Anmeldeinformationen im aktuellen Abschnitt des Profils eingerichtet. Der Transportanbieter gibt ein Anmeldeobjekt zurück. 
    
3. Der MAPI-Spooler ruft die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) auf. Der Transportanbieter gibt eine Liste der eindeutigen Bezeichner (UIDs) und E-Mail-Adresstypen zurück, die er akzeptiert. 
    
4. Der Transportanbieter ruft die [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) auf, um die Zeile in der MAPI-Statustabelle zu erstellen. 
    
5. Der MAPI-Spooler ruft die [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) auf, um die Nachrichtenübertragung und den Nachrichtenempfang zu aktivieren. 
    
6. Wenn der Transportanbieter in seiner Rückgabe für den **TransportLogon-Aufruf** angefordert wird, ruft der MAPI-Spooler in regelmäßigen Abständen die [IXPLogon::Idle-Methode](ixplogon-idle.md) auf. Die Leerlaufverarbeitung ist nützlich, wenn der Transportanbieter das zugrunde liegende Messagingsystem auf neue Nachrichten abfragen oder andere Aufgaben mit niedriger Priorität ausführen muss. 
    
7. Der MAPI-Spooler und der Transportanbieter senden und empfangen Nachrichten. Weitere Informationen finden Sie unter [Nachrichtenübermittlungsmodell](message-submission-model.md) und [Nachrichtenempfangsmodell.](message-reception-model.md) Die MAPI-Spoolerdienste transportanfragen und -aufrufe für Support-, Nachrichten- und Anlagenobjekte.
    
8. Der MAPI-Spooler ruft die **TransportNotify-Methode** auf, um die Nachrichtenübertragung und den Nachrichtenempfang zu deaktivieren. 
    
9. Der MAPI-Spooler gibt die Anmelde- und Anbieterobjekte frei. Weitere Informationen finden Sie unter der [IXPProvider::Shutdown-Methode.](ixpprovider-shutdown.md) 
    

