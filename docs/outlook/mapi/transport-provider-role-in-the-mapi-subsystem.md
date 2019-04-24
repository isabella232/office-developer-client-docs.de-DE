---
title: Transportanbieterrolle im MAPI-Subsystem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7cadb57706e3feec7ed98dd5e4e8d75967036fef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356620"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Transportanbieterrolle im MAPI-Subsystem
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Transport Provider Dynamic-Link Libraries (DLLs) stellen die Schnittstelle zwischen dem MAPI-Spooler und dem Teil eines Messagingsystems bereit, das für das Senden und empfangen von Nachrichten zuständig ist. Die MAPI-Spooler und der Transportanbieter arbeiten zusammen, um die Zuständigkeiten des Sendens einer Nachricht oder des Empfangens einer Nachricht zu behandeln. Der MAPI-Spooler lädt die Transportanbieter-DLL, wenn Sie zuerst verwendet wird, und gibt Sie frei, wenn Sie nicht mehr benötigt wird. Mehrere Transportanbieter können auf demselben System installiert werden, MAPI stellt jedoch den erforderlichen Spooler bereit.
  
Client Anwendungen kommunizieren in der Regel nicht direkt mit dem Transportanbieter. Stattdessen übermitteln Clients Nachrichten über einen Speicheranbieter, und der MAPI-Spooler sendet ausgehende Nachrichten an den entsprechenden Transportanbieter und übermittelt eingehende Nachrichten an den entsprechenden Nachrichtenspeicher. Der MAPI-Spooler funktioniert und ruft seine Anrufe an Transportanbieter ab, wenn vordergrundanwendungen im Leerlauf sind. Nachdem optional Dialogfelder angezeigt werden, wenn der Transportanbieter zum ersten Mal angemeldet ist, werden Transportanbieter im Hintergrund ausgeführt, es sei denn, der Client wird zum leeren von Sende-und Empfangs Warteschlangen aufgerufen. 
  
Transport Anbieter haben folgende Zuständigkeiten in einem MAPI-Messagingsystem:
  
- Registrieren Sie die Adresstypen, die Sie mit dem MAPI-Spooler akzeptieren können, damit der MAPI-Spooler Nachrichten abhängig von der Zieladresse der Nachrichten an den entsprechenden Transportanbieter übermitteln kann. Ein Transportanbieter kann mehrere Adresstypen registrieren. Transport Anbieter können auch bestimmte Empfängeradressen mit dem MAPI-Spooler registrieren. An eine dieser Adressen adressierte Nachrichten werden an den Transportanbieter übermittelt, der die Adresse mit dem MAPI-Spooler registriert hat. Weitere Informationen finden Sie unter [Transport Anbieter und MAPI-Spooler-Betriebsmodell](transport-provider-and-mapi-spooler-operational-model.md).
    
- Übermitteln Sie eingehende Nachrichten an den MAPI-Spooler. Je nach Art des Messagingsystems kann ein Transportanbieter den MAPI-Spooler entweder direkt benachrichtigen, wenn eine neue Nachricht eingeht, oder er kann anfordern, dass der MAPI-Spooler den Transportanbieter regelmäßig abfragt, ob er nach neuen Nachrichten suchen soll.
    
- Konvertieren von MAPI-Nachrichteneigenschaften in und aus Nachrichteneigenschaften, die im Messagingsystem systemintern sind. Beispielsweise muss der Transportanbieter die Absender-und Empfängeradressen in einer ausgehenden Nachricht in ein für das Messagingsystem akzeptables Formular konvertieren. Einige Messagingsysteme unterstützen nicht alle MAPI-Nachrichteneigenschaften. Weitere Informationen zum Beibehalten von MAPI-Nachrichteneigenschaften beim Übermitteln von Nachrichten an ein Messagingsystem finden Sie unter [Entwickeln eines TNEF-fähigEn Transport Anbieters](developing-a-tnef-enabled-transport-provider.md).
    
- Registrieren von Nachrichten-und Empfängeroptionen für den Transportanbieter.
    
- Führen Sie die Überprüfung der vom Messagingsystem erforderlichen Anmeldeinformationen durch.
    
- Zugriff auf ausgehende Nachrichten mithilfe des Message-Objekts, das vom MAPI-Spooler an die Nachricht übergeben wird.
    
- Nachrichtenformat nach Bedarf des zugrunde liegenden Messagingsystems übersetzen.
    
- Benachrichtigen Sie den MAPI-Spooler, welche Empfänger einer ausgehenden Nachricht der Transportanbieter die Verantwortung für die Behandlung übernommen hat, indem Sie die **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft für diese Empfänger festlegen.
    
- Informieren Sie den MAPI-Spooler, wenn eine eingehende Nachricht behandelt werden muss.
    
- Weiterleiten eingehender Nachrichtendaten an den MAPI-Spooler mithilfe von Message-Objekten.
    
- Weisen Sie allen erforderlichen MAPI-Nachrichteneigenschaften für eingehende Nachrichten Werte zu.
    
- Löschen Sie, falls erforderlich, die Nachricht aus dem zugrunde liegenden Messagingsystem.
    
- Bereitstellen von Statusinformationen für die MAPI-Spooler-und Clientanwendungen.
    
Die folgende Abbildung zeigt die Rolle eines Transportanbieters im Hinblick auf die anderen Komponenten der MAPI-Architektur.
  
**Transportanbieterrolle in einem Messaging-System**
  
![Transport Anbieterrolle in einem Messagingsystem] (media/xp01.gif "Transport Anbieterrolle in einem Messagingsystem")
  

