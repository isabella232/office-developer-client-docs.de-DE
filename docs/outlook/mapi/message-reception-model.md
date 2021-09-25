---
title: Nachrichtenempfangsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48cd642cf72a04764c17be5480b10036f61142d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592039"
---
# <a name="message-reception-model"></a>Nachrichtenempfangsmodell

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Transportanbieter steuert, ob der MAPI-Spooler eingehende E-Mails abfragen muss oder ob beim Eintreffen neuer E-Mails ein Rückruf an den MAPI-Spooler ausgeführt wird. Der Transportanbieter legt das flag SP_LOGON_POLL fest, wenn er von [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) zurückgegeben wird, um Abfragen anzufordern. Andernfalls verwendet der Transportanbieter [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md) wenn eingehende E-Mails verfügbar sind. Nachdem sie erfahren haben, dass eingehende E-Mails verfügbar sind, öffnet der MAPI-Spooler eine neue Nachricht und fordert den Transportanbieter auf, die empfangenen Nachrichteneigenschaften in der Nachricht zu speichern. 
  
Dieser Vorgang funktioniert wie folgt:
  
1. Verfügbare Nachrichten werden entweder durch den Transportanbieter angezeigt, der **IMAPISupport::SpoolerNotify** aufruft, oder durch den MAPI-Spooler, der [IXPLogon::P oll aufruft.](ixplogon-poll.md)
    
2. Der MAPI-Spooler ruft [IXPLogon::StartMessage](ixplogon-startmessage.md) auf, um den Prozess zu initiieren. 
    
3. Der Transportanbieter platziert einen Verweiswert an dem Speicherort, auf den in **StartMessage** verwiesen wird. Diese Referenzwerte ermöglichen es dem Transportanbieter und dem MAPI-Spooler, nachzuverfolgen, welche Nachricht verarbeitet wird, wenn mehrere Nachrichten zu übermitteln sind.
    
4. Der Transportanbieter speichert die Nachrichtendaten in der übergebenen [IMessage : IMAPIProp-Instanz.](imessageimapiprop.md) 
    
5. Der Transportanbieter ruft die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) für die **IMessage-Instanz** auf und gibt von **StartMessage** zurück.
    
6. Der MAPI-Spooler ruft [IXPLogon::TransportNotify auf,](ixplogon-transportnotify.md) wenn die Nachrichtenübermittlung beendet werden muss. 
    
> [!NOTE]
> Wenn ein Transportanbieter eine große Anzahl von Nachrichten übermitteln muss und der Transportanbieter **IMAPISupport::SpoolerNotify** anstelle von **IXPLogon::P Oll** verwendet, sollten Sie darauf achten, **SpoolerNotify** nicht zu häufig aufzurufen, um andere Transportanbieter von CPU-Zeit nicht zu belasten. Der MAPI-Spooler verfügt über Logik, um dies zu verhindern. Im Allgemeinen sollte das Intervall zwischen **SpoolerNotify-Aufrufen** jedoch länger als die Zeit sein, die der Transportanbieter für die Verarbeitung einer Nachricht benötigt. > Außerdem verarbeitet der MAPI-Spooler möglicherweise keine eingehende Nachricht sofort. Der MAPI-Spooler kann den Transportanbieter bitten, andere Aufgaben auszuführen, bevor er die eingehende Nachricht empfängt. 
  

