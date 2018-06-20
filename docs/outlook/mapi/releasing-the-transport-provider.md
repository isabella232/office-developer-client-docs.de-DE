---
title: Freigeben der Adressbuchhierarchie
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: b8032b22c78ae34bce7e9ccfb0f0a14cdde07290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795362"
---
# <a name="releasing-the-transport-provider"></a>Freigeben der Adressbuchhierarchie

 
  
**Betrifft**: Outlook 
  
Wenn MAPI oder die MAPI-Warteschlange beendet eine Anmeldung Transportobjekt verwenden ist:
  
1. MAPI- oder die MAPI-Warteschlange der Adressbuchhierarchie [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) Methode aufgerufen. 
    
2. Der Transportdienst wird das Statusobjekt durch Aufrufen der Methode [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) ungültig. Ob der Adressbuchhierarchie Nachrichtenobjekte ungültig, die hängt gesendet oder empfangen zum Zeitpunkt des Anrufs **TransportLogoff** der Kennzeichen, die an **TransportLogoff**übergeben wurden.
    
3. Der Transportdienst Ruft die des Unterstützungsobjekts [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode zum Entfernen der Adressbuchhierarchie Zeile aus der Statustabelle und aus internen Tabellen eine beliebige eindeutige Bezeichner (UIDs), die mit der [IMAPISupport festgelegt wurden: SetProviderUID](imapisupport-setprovideruid.md) Methode. Es verringert die Anzahl der bekannten Logon-Objekten, die auf dieses Anbieterobjekt aktiv. Wenn die Anzahl 0 (null) erreicht, ruft MAPI die [IXPProvider::Shutdown](ixpprovider-shutdown.md) -Methode und die **Freigabe** für das Provider-Objekt. Wenn dies das letzte bekannte Anbieterobjekt verwenden diese DLL für diesen Prozess war, ruft MAPI **FreeLibrary** -Funktion der DLL zu einem späteren Zeitpunkt. Speicher für das MAPI-Support-Objekt wird freigegeben und **Release** -Methode das Support-Objekt zurückgibt. 
    
4. Die **TransportLogoff** -Methode gibt S_OK zurück. 
    
5. MAPI- oder die MAPI-Warteschlange ruft **Release** auf der Adressbuchhierarchie Anmeldung-Objekt. Der Speicher für das Objekt wird freigegeben. 
    
6. MAPI- oder die MAPI-Warteschlange ruft **FreeLibrary** auf der Provider-DLL. 
    
Für Stabilität sollte die Anmeldung und Anbieter-Objekte endgültige **Version** Anrufe auf sich selbst ohne zuvor ihre **TransportLogoff** oder **zum Herunterfahren von** Methoden behandeln können. Wenn in solchen Fällen **Release** aufgerufen wird, sollte Transportanbieter die Anrufe behandelt, als ob **TransportLogoff** oder **Herunterfahren** mit einem NULL-Argument gefolgt von **Release**aufgerufen wurde, hatte.
  

