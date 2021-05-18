---
title: Freigeben des Transportanbieters
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
# <a name="releasing-the-transport-provider"></a>Freigeben des Transportanbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn MAPI oder der MAPI-Spooler mit einem Transportanmeldeobjekt abgeschlossen wird:
  
1. MAPI oder der MAPI-Spooler ruft die [IXPLogon::TransportLogoff-Methode des Transportanbieters](ixplogon-transportlogoff.md) auf. 
    
2. Der Transportanbieter macht das status-Objekt ungültig, indem die [IMAPISupport::MakeInvalid-Methode](imapisupport-makeinvalid.md) aufruft. Ob der Transportanbieter Nachrichtenobjekte ungültig macht, die zum Zeitpunkt des **TransportLogoff-Aufrufs** gesendet oder empfangen werden, hängt von den Flags ab, die an **TransportLogoff übergeben wurden.**
    
3. Der Transportanbieter ruft die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) des Supportobjekts auf, um die Zeile des Transportanbieters aus der Statustabelle zu entfernen und alle eindeutigen Bezeichner (UIDs), die mit der [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) festgelegt wurden, aus internen Tabellen zu entfernen. Dadurch wird die Anzahl der bekannten Anmeldeobjekte, die für dieses Anbieterobjekt aktiv sind, dekrementiert. Wenn die Anzahl null erreicht, ruft MAPI die [IXPProvider::Shutdown-Methode](ixpprovider-shutdown.md) und **Release für** das Anbieterobjekt auf. Wenn dies das letzte bekannte Anbieterobjekt war, das diese DLL für diesen Prozess verwendet, ruft MAPI die **FreeLibrary-Funktion** zu einem späteren Zeitpunkt in der DLL auf. Der Arbeitsspeicher für das MAPI-Unterstützungsobjekt wird freigegeben, und die **Release-Methode des Supportobjekts gibt** zurück. 
    
4. Die **TransportLogoff-Methode** gibt S_OK. 
    
5. MAPI oder der MAPI-Spooler ruft **Release für** das Anmeldeobjekt des Transportanbieters auf. Der Arbeitsspeicher für das Objekt wird freigegeben. 
    
6. MAPI oder der MAPI-Spooler ruft **FreeLibrary** für die Anbieter-DLL auf. 
    
Zur Robustheit sollten die Anmelde- und Anbieterobjekte  in der Lage sein, endgültige Releaseaufrufe für sich selbst zu verarbeiten, ohne zuerst ihre **TransportLogoff-** oder **Shutdown-Methoden** aufrufen zu müssen. Wenn **Release** in solchen Fällen aufgerufen wird, sollten Transportanbieter die Anrufe so behandeln, als ob **TransportLogoff** oder **Shutdown** mit einem Nullargument gefolgt von Release aufgerufen **worden wären.**
  

