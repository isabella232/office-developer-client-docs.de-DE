---
title: Nachrichtenempfangs Modell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356945"
---
# <a name="message-reception-model"></a>Nachrichtenempfangs Modell

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Transportanbieter steuert, ob der MAPI-Spooler es für eingehende e-Mails Abfragen muss, oder ob er beim Eintreffen neuer e-Mails einen Rückruf an den MAPI-Spooler ausführt. Der Transportanbieter legt das SP_LOGON_POLL-Flag fest, wenn es von [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) zurückgibt, um Polling anzufordern. Andernfalls verwendet der Transportanbieter [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) , wenn eingehende e-Mail verfügbar ist. Nachdem Sie erfahren haben, dass eingehende e-Mails verfügbar sind, öffnet der MAPI-Spooler eine neue Nachricht und fordert den Transportanbieter auf, die empfangenen Nachrichteneigenschaften in der Nachricht zu speichern. 
  
Dieser Vorgang funktioniert wie folgt:
  
1. Verfügbare Nachrichten werden entweder vom Transportanbieter, der **IMAPISupport:: SpoolerNotify** oder vom MAPI-Warteschlangen Aufruf [IXPLogon::P oll](ixplogon-poll.md)angezeigt.
    
2. Der MAPI-Spooler ruft [IXPLogon:: StartMessage](ixplogon-startmessage.md) auf, um den Prozess zu initiieren. 
    
3. Der Transportanbieter platziert einen Verweiswert an dem Speicherort, auf den in **StartMessage**verwiesen wird. Anhand dieser Referenzwerte können Transportanbieter und MAPI-Spooler nachverfolgen, welche Nachricht verarbeitet wird, wenn mehrere zu übermittelnde Nachrichten vorhanden sind.
    
4. Der Transportanbieter speichert die Nachrichtendaten in der übergebenen [IMessage: IMAPIProp](imessageimapiprop.md) -Instanz. 
    
5. Der Transportanbieter Ruft die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode für die **IMessage** -Instanz auf und gibt von **StartMessage**zurück.
    
6. Der MAPI-Warteschlangen Aufruf [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) , wenn die Nachrichtenübermittlung beendet werden muss. 
    
> [!NOTE]
> Wenn ein Transportanbieter eine hohe Anzahl von Nachrichten übermitteln muss und der Transportanbieter **IMAPISupport:: SpoolerNotify** anstelle von **IXPLogon verwendet::P oll**, sollte darauf geachtet werden, **SpoolerNotify** nicht zu häufig aufzurufen, um nicht anderen Transportanbietern die CPU-Zeit entziehen. Der MAPI-Spooler hat Logik, um dies zu verhindern, aber im Allgemeinen sollte das Intervall zwischen **SpoolerNotify** -anrufen länger sein als die Zeit, die der Transportanbieter zum Verarbeiten einer Nachricht benötigt. > Außerdem kann der MAPI-Spooler keine eingehenden Nachrichten sofort verarbeiten. Der MAPI-Spooler kann den Transportanbieter bitten, andere Aufgaben auszuführen, bevor die eingehende Nachricht empfangen wird. 
  

