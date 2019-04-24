---
title: Freigeben des Transport Anbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328385"
---
# <a name="releasing-the-transport-provider"></a>Freigeben des Transport Anbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn MAPI oder der MAPI-Spooler mit einem Transport Logon-Objekt abgeschlossen ist:
  
1. MAPI oder der MAPI-Spooler Ruft die [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) -Methode des Transportanbieters auf. 
    
2. Der Transportanbieter validiert das Status-Objekt durch Aufrufen der [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) -Methode. Ob der Transportanbieter Nachrichtenobjekte, die gesendet oder empfangen werden, zum Zeitpunkt des **TransportLogoff** -Aufrufs ungültig macht, hängt von den Flags ab, die an **TransportLogoff**übergeben wurden.
    
3. Der Transportanbieter Ruft die [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode des Support Objekts auf, um die Zeile des Transportanbieters aus der Statustabelle zu entfernen und aus internen Tabellen alle eindeutigen Bezeichner (IDs) zu entfernen, die mit der IMAPISupport festgelegt wurden [: SetProviderUID](imapisupport-setprovideruid.md) -Methode. Die Anzahl bekannter Anmeldeobjekte, die für dieses Anbieterobjekt aktiv sind, wird verringert. Wenn die Anzahl 0 (null) erreicht, ruft MAPI die [IXPProvider:: Shutdown](ixpprovider-shutdown.md) -Methode und die **Freigabe** für das Provider-Objekt auf. Wenn dies das letzte bekannte Anbieterobjekt ist, das diese DLL verwendet, ruft MAPI zu einem späteren Zeitpunkt die **FreeLibrary** -Funktion für die dll auf. Der Speicher für das MAPI-Unterstützungsobjekt wird freigegeben, und die **Release** -Methode des Support-Objekts gibt zurück. 
    
4. Die **TransportLogoff** -Methode gibt S_OK zurück. 
    
5. MAPI oder der MAPI-Spooler Ruft die **Freigabe** für das Anmeldeobjekt des Transportanbieters auf. Der Arbeitsspeicher für das Objekt wird freigegeben. 
    
6. MAPI oder der MAPI-Spooler ruft **FreeLibrary** für die Anbieter-DLL auf. 
    
Aus Stabilitäts-, Anmelde-und Anbieter Objekten sollte in der Lage sein, abschließende **Freigabe** Aufrufe für sich selbst zu behandeln, ohne zuvor Ihre **TransportLogoff** -oder **Shutdown** -Methoden aufgerufen zu haben. Wenn **Release** in solchen Fällen aufgerufen wird, sollten Transportanbieter die Aufrufe so behandeln, als ob **TransportLogoff** oder **Shutdown** mit einem NULL-Argument, gefolgt von **Release**, aufgerufen wurde.
  

