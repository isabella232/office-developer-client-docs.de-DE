---
title: Freigeben des Transportanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: c2c4ff3d3d827950080f8f81545471b087c2581d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624371"
---
# <a name="releasing-the-transport-provider"></a>Freigeben des Transportanbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn die MAPI oder der MAPI-Spooler die Verwendung eines Transportanmeldeobjekts abgeschlossen hat:
  
1. Die MAPI oder der MAPI-Spooler ruft die [IXPLogon::TransportLogoff-Methode](ixplogon-transportlogoff.md) des Transportanbieters auf. 
    
2. Der Transportanbieter macht das Statusobjekt ungültig, indem die [IMAPISupport::MakeInvalid-Methode](imapisupport-makeinvalid.md) aufgerufen wird. Ob der Transportanbieter Nachrichtenobjekte ungültig macht, die zum Zeitpunkt des **TransportLogoff-Aufrufs** gesendet oder empfangen werden, hängt von den Flags ab, die an **TransportLogoff** übergeben wurden.
    
3. Der Transportanbieter ruft die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) des Supportobjekts auf, um die Zeile des Transportanbieters aus der Statustabelle zu entfernen und alle eindeutigen Bezeichner (UIDs), die mit der [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) festgelegt wurden, aus internen Tabellen zu entfernen. Die Anzahl bekannter Anmeldeobjekte, die für dieses Anbieterobjekt aktiv sind, wird verringert. Wenn die Anzahl Null erreicht, ruft MAPI die [IXPProvider::Shutdown-Methode](ixpprovider-shutdown.md) und **Release** für das Anbieterobjekt auf. Wenn dies das letzte bekannte Anbieterobjekt war, das diese DLL in diesem Prozess verwendet, ruft MAPI die **FreeLibrary-Funktion** zu einem späteren Zeitpunkt auf der DLL auf. Speicher für das MAPI-Unterstützungsobjekt wird freigegeben, und die **Release-Methode** des Supportobjekts wird zurückgegeben. 
    
4. Die **TransportLogoff-Methode** gibt S_OK zurück. 
    
5. DIE MAPI oder der MAPI-Spooler ruft **Release** für das Anmeldeobjekt des Transportanbieters auf. Der Speicher für das Objekt wird freigegeben. 
    
6. Die MAPI oder der MAPI-Spooler ruft **FreeLibrary** auf der Anbieter-DLL auf. 
    
Aus Gründen der Robustheit sollten die Anmelde-  und Anbieterobjekte in der Lage sein, endgültige Release-Aufrufe für sich selbst zu verarbeiten, ohne zuvor die **TransportLogoff-** oder **Shutdown-Methoden** aufgerufen zu haben. Wenn **Release** in solchen Fällen aufgerufen wird, sollten Transportanbieter die Aufrufe so behandeln, als ob **TransportLogoff** oder **Shutdown** mit einem Null-Argument gefolgt von **Release** aufgerufen worden wäre.
  

