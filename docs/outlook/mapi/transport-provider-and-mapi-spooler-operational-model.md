---
title: Betriebsmodell des Transportanbieters und des MAPI-Spoolers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426625"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Betriebsmodell des Transportanbieters und des MAPI-Spoolers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Initialisierung, der Start, die Verarbeitung, das Herunterfahren und die Deinitialisierung des Transportanbieters werden durch eine Reihe von Aufrufen vom MAPI-Spooler an den Transportanbieter durchgeführt. Die Aufrufe werden wie folgt sequenziert:
  
1. Der MAPI-Spooler ruft die [XPProviderInit-Funktion](xpproviderinit.md) auf, übergibt ein Supportobjekt, ruft das Anbieterobjekt ab und überprüft, ob der Transportanbieter und der MAPI-Spooler einen kompatiblen Bereich von MAPI-Versionsnummern unterstützen. 
    
2. Der MAPI-Spooler ruft die [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) der [IXPProvider : IUnknown-Schnittstelle](ixpprovideriunknown.md) auf. Es wird eine Sitzung zwischen dem MAPI-Spooler und dem Transportanbieter mit den Anmeldeinformationen im aktuellen Abschnitt des Profils eingerichtet. Der Transportanbieter gibt ein Anmeldeobjekt zurück. 
    
3. Der MAPI-Spooler ruft die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) auf. Der Transportanbieter gibt eine Liste der eindeutigen Bezeichner (UIDs) und E-Mail-Adresstypen zurück, die er akzeptiert. 
    
4. Der Transportanbieter ruft die [IMAPISupport::ModifyStatusRow-Methode auf,](imapisupport-modifystatusrow.md) um die Zeile in der MAPI-Statustabelle zu erstellen. 
    
5. Der MAPI-Spooler ruft die [IXPLogon::TransportNotify-Methode auf,](ixplogon-transportnotify.md) um die Nachrichtenübermittlung und den Empfang zu aktivieren. 
    
6. Wenn der Transportanbieter in seiner Rückgabe für den **TransportLogon-Aufruf** angefordert wird, ruft der MAPI-Spooler regelmäßig die [IXPLogon::Idle-Methode](ixplogon-idle.md) auf. Die Verarbeitung im Leerlauf ist hilfreich, wenn der Transportanbieter das zugrunde liegende Messagingsystem auf neue Nachrichten abfragen oder andere Aufgaben mit niedriger Priorität ausführen muss. 
    
7. Der MAPI-Spooler und der Transportanbieter senden und empfangen Nachrichten. Weitere Informationen finden Sie unter [Nachrichtenübermittlungsmodell](message-submission-model.md) und [Nachrichtenempfangsmodell](message-reception-model.md). Die MAPI-Spoolerdienste transportieren Anforderungen und Aufrufe von Support-, Nachrichten- und Anlagenobjekten.
    
8. Der MAPI-Spooler ruft die **TransportNotify-Methode** auf, um die Nachrichtenübermittlung und den Empfang zu deaktivieren. 
    
9. Der MAPI-Spooler gibt die Anmelde- und Anbieterobjekte frei. Weitere Informationen finden Sie unter [der IXPProvider::Shutdown-Methode.](ixpprovider-shutdown.md) 
    

