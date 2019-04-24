---
title: Initialisieren von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309730"
---
# <a name="initializing-mapi"></a>Initialisieren von MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Clientanwendungen, die die MAPI-Bibliotheken verwenden, müssen die **MAPIInitialize** -Funktion aufrufen. Weitere Informationen finden Sie unter [MAPIInitialize](mapiinitialize.md). **MAPIInitialize** initialisiert globale Daten für die Sitzung und bereitet die MAPI-Bibliotheken so vor, dass Sie Anrufe annehmen. Es gibt einige Flags, die in einigen Situationen festgelegt werden müssen: 
  
- MAPI_NT_SERVICE
    
    Legen Sie das MAPI_NT_SERVICE-Flag fest, wenn Ihr Client als Windows-Dienst implementiert ist. Wenn Ihr Client ein Windows-Dienst ist und Sie dieses Flag nicht festlegen, wird es von MAPI nicht als Dienst erkannt. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    Das MAPI_MULTITHREAD_NOTIFICATIONS-Flag bezieht sich darauf, wie MAPI-Benachrichtigungen verwaltet werden. MAPI erstellt ein ausgeblendetes Fenster, das Fenster Meldungen empfängt, wenn Änderungen an Objekten erfolgen, die Benachrichtigungen generieren. Die Fenster Meldungen werden zu einem bestimmten Zeitpunkt verarbeitet, sodass die Benachrichtigungen gesendet werden und die entsprechenden [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methoden aufgerufen werden. 
    
- MAPI_NO_COINIT
    
    Legen Sie das MAPI_NO_COINT-Flag fest, sodass **MAPIInitialize** nicht versucht, com mit einem Aufruf [](https://msdn.microsoft.com/library/ms886303.aspx)von "Initialize" zu initialisieren. Wenn eine **MAPIINIT_0** -Struktur an **MAPIInitialize** übergeben wird, wobei _ulFlags_ auf MAPI_NO_COINIT festgelegt ist, wird von MAPI davon ausgegangen, dass com bereits INITIALISIERT wurde und den Aufruf von "diinitialize" umgehen. ****
    
Wenn das MAPI_MULTITHREAD_NOTIFICATIONS-Flag nicht übergeben wird, erstellt MAPI das Benachrichtigungsfenster für den Thread, der für Ihren ersten **MAPIInitialize** -Aufruf verwendet wurde. MAPI erstellt das Benachrichtigungsfenster in einem separaten Thread, wenn MAPI_MULTITHREAD_NOTIFICATIONS übergeben wird – ein Thread, der für die Behandlung von Benachrichtigungen reserviert ist. MAPI erwartet den Thread, der zum Erstellen des ausgeblendeten Benachrichtigungsfensters verwendet wird, für Folgendes: 
  
- Haben Sie eine Meldungsschleife.
    
- Während der gesamten Lebensdauer der Sitzung nicht blockiert.
    
- Sie haben eine längere Lebensdauer als alle anderen von Ihrem Client erstellten Threads. 
    
Sie können auswählen, welcher Thread verwendet wird, indem Sie im ersten **MAPIInitialize** -Aufruf eine Kennzeichnung festlegen. Die Gefahr, dass eines ihrer Threads die Benachrichtigungen verarbeitet, besteht darin, dass das Benachrichtigungsfenster zerstört wird und Benachrichtigungen nicht mehr an andere Threads gesendet werden können, wenn der Thread ausgeblendet wird. Außerdem kann eine spezielle Verarbeitung erforderlich sein, um die Versendung der Benachrichtigungen zu steuern, die an die Nachrichtenwarteschlange des ausgeblendeten Fensters gesendet werden. 
  
Wenn Sie ein separates Fenster zum Behandeln von Benachrichtigungen verwenden, müssen Sie sicherstellen, dass Benachrichtigungen zu einem geeigneten Zeitpunkt zu einem geeigneten Thread angezeigt werden. Sie benötigen keinen speziellen Code, um die im Benachrichtigungsfenster bereitgestellten Windows-Nachrichten zu überprüfen und zu verarbeiten. 
  
MAPI empfiehlt, dass die folgenden Typen von Clientanwendungen einen separaten Thread verwenden, um das ausgeblendete Fenster für die Benachrichtigungsunterstützung zu erstellen:
  
- Alle Multithread-Clients.
    
- Single threaded-Windows-Dienste und Win32-Konsolenanwendungen.
    
- Single Thread-Clients, die ihren Hauptthread für die Benachrichtigung nicht verwenden müssen.
    
Wenn Sie den separaten Thread Ansatz verwenden möchten, rufen Sie **MAPIInitialize** für jeden Thread auf, und legen Sie das MAPI_MULTITHREAD_NOTIFICATIONS-Flag fest. 
  
> [!NOTE]
> Nur der erste Aufruf des Clients an **MAPIInitialize** bewirkt, dass ein ausgeblendetes Fenster zur Unterstützung von Benachrichtigungen erstellt wird. Nachfolgende Aufrufe führen nur zu einer Erhöhung der Verweisanzahl. 
  

