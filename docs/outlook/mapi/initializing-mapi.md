---
title: MAPI-Initialisierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f1dac712731175978bc639cc7296171448a41e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792710"
---
# <a name="initializing-mapi"></a>MAPI-Initialisierung

  
  
**Betrifft**: Outlook 
  
Alle Clientanwendungen, die MAPI-Bibliotheken verwenden, müssen die Funktion **"MAPIInitialize"** aufrufen. Weitere Informationen finden Sie unter ["MAPIInitialize"](mapiinitialize.md). **"MAPIInitialize"** globale Daten für die Sitzung initialisiert und bereitet die MAPI-Bibliotheken, die Anrufe annehmen. Es gibt einige Flags, die die festzulegenden in manchen Fällen eine wichtige Rolle spielen: 
  
- MAPI_NT_SERVICE
    
    Festlegen Sie MAPI_NT_SERVICE das Flag, ob Ihre Clients als Windows-Dienst implementiert wird. Wenn Ihr Client ein Windows-Dienst ist und nicht dieses Flag festlegen, wird Sie von MAPI nicht als Dienst erkannt. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    Das Flag MAPI_MULTITHREAD_NOTIFICATIONS bezieht sich auf wie MAPI Benachrichtigungen verwaltet wird. MAPI erstellt ein ausgeblendetes Fenster, das Fenster-Nachrichten empfängt beim Auftreten von Änderungen auf ein Objekt Benachrichtigungen generieren. Die Fensternachrichten werden zu einem bestimmten Zeitpunkt, verursacht die Benachrichtigungen gesendet werden und die entsprechenden [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) Methoden aufgerufen werden verarbeitet. 
    
- MAPI_NO_COINIT
    
    Das Flag MAPI_NO_COINT so festgelegt, dass **"MAPIInitialize"** nicht versucht, mit einem Aufruf von [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx)COM initialisieren. Wenn eine **MAPIINIT_0** -Struktur mit _UlFlags_ auf MAPI_NO_COINIT festgelegt in **"MAPIInitialize"** übergeben wird, wird MAPI wird vorausgesetzt, dass COM bereits initialisiert wurde, und den Aufruf von **CoInitialize**umgehen.
    
Wenn MAPI_MULTITHREAD_NOTIFICATIONS Flag nicht übergeben wird, MAPI erstellt das Benachrichtigung Thread, der verwendet wurde, für den ersten Aufruf **"MAPIInitialize"** . MAPI wird das Benachrichtigungsfenster in einem getrennten Thread erstellt, wenn MAPI_MULTITHREAD_NOTIFICATIONS übergeben wird – ein Thread dedizierte zum Behandeln von Benachrichtigungen. MAPI erwartet, dass den Thread, der zum Erstellen des Fensters ausgeblendete Benachrichtigung zu verwendet wird: 
  
- Haben Sie eine Nachrichtenschleife.
    
- Bleiben Sie während der Lebensdauer der Sitzung freigegeben werden soll.
    
- Haben Sie eine längere Lebensdauer als ein anderer Thread vom Client erstellt. 
    
Sie können auswählen, welcher Thread verwendet wird, indem ein Flag in der erste Aufruf **"MAPIInitialize"** . Die Gefahr zulassen eine der Threads, die Benachrichtigungen zu behandeln ist, die, wenn der Thread ausgeblendet wird, das Benachrichtigungsfenster gelöscht wird und Benachrichtigungen nicht mehr an eines Ihrer anderen Threads gesendet werden können. Spezielle Verarbeitung Bedarf auch, steuern den Versand der Benachrichtigung, die an das ausgeblendete Fenster Nachrichtenwarteschlange veröffentlicht werden. 
  
Wenn Sie ein separates Fenster zum Behandeln von Benachrichtigungen verwenden, sicher, dass zum entsprechenden Zeitpunkt in einem entsprechenden Thread Benachrichtigung angezeigt wird. Sie benötigen keine speziellen Code zum Suchen und Verarbeiten der Windows-Nachrichten, die in der Benachrichtigungsfenster bereitgestellt werden. 
  
MAPI empfiehlt, dass die folgenden Arten von Clientanwendungen einen getrennten Thread verwenden, um das ausgeblendete Fenster für die Unterstützung der Benachrichtigung zu erstellen:
  
- Alle Multithread-Clients.
    
- Single-Threading Windows-Dienste und Win32-Konsole Applications.
    
- Single-Thread-Clients, die nicht ihrer Hauptthread für die Benachrichtigung verwendet werden müssen.
    
Rufen Sie für die Verwendung den getrennten Thread Ansatz **"MAPIInitialize"** in jeder Thread, der das MAPI_MULTITHREAD_NOTIFICATIONS-Flag festlegen. 
  
> [!NOTE]
> Nur ein Client erste Aufruf von **"MAPIInitialize"** bewirkt, dass ein ausgeblendetes Fenster erstellt werden soll, um Benachrichtigungen zu unterstützen. Nachfolgende Aufrufe der einzige Ursache ein Referenzzähler erhöht werden soll. 
  

