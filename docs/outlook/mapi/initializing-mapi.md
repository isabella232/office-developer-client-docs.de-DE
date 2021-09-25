---
title: Initialisieren von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7efde83b40ca62fcd19d430f9b261789bac55e18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556350"
---
# <a name="initializing-mapi"></a>Initialisieren von MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Clientanwendungen, die die MAPI-Bibliotheken verwenden, müssen die **MAPIInitialize-Funktion** aufrufen. Weitere Informationen finden Sie unter [MAPIInitialize](mapiinitialize.md). **MAPIInitialize initialisiert** globale Daten für die Sitzung und bereitet die MAPI-Bibliotheken auf die Annahme von Anrufen vor. Es gibt einige Flags, die in einigen Situationen festgelegt werden müssen: 
  
- MAPI_NT_SERVICE
    
    Legen Sie das flag MAPI_NT_SERVICE fest, wenn Ihr Client als Windows Dienst implementiert ist. Wenn Ihr Client ein Windows Dienst ist und Sie dieses Flag nicht festlegen, erkennt MAPI es nicht als Dienst. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    Das MAPI_MULTITHREAD_NOTIFICATIONS Flag bezieht sich darauf, wie MAPI Benachrichtigungen verwaltet. MAPI erstellt ein ausgeblendetes Fenster, das Fenstermeldungen empfängt, wenn Änderungen an einem Objekt vorgenommen werden, das Benachrichtigungen generiert. Die Fenstermeldungen werden zu einem bestimmten Zeitpunkt verarbeitet, wodurch die Benachrichtigungen gesendet und die entsprechenden [IMAPIAdviseSink::OnNotify-Methoden](imapiadvisesink-onnotify.md) aufgerufen werden. 
    
- MAPI_NO_COINIT
    
    Legen Sie das MAPI_NO_COINT Flag fest, damit **MAPIInitialize** nicht versucht, COM mit einem Aufruf von [CoInitialize zu initialisieren.](https://msdn.microsoft.com/library/ms886303.aspx) Wenn eine **MAPIINIT_0** Struktur an **MAPIInitialize** übergeben wird, wobei  _ulFlags_ auf MAPI_NO_COINIT festgelegt ist, geht MAPI davon aus, dass COM bereits initialisiert wurde, und umgeht den Aufruf von **CoInitialize**.
    
Wenn MAPI_MULTITHREAD_NOTIFICATIONS Flag nicht übergeben wird, erstellt MAPI das Benachrichtigungsfenster in dem Thread, der für Ihren ersten **MAPIInitialize-Aufruf** verwendet wurde. MAPI erstellt das Benachrichtigungsfenster in einem separaten Thread, wenn MAPI_MULTITHREAD_NOTIFICATIONS übergeben wird – ein Thread, der für die Verarbeitung von Benachrichtigungen vorgesehen ist. MAPI erwartet den Thread, der zum Erstellen des ausgeblendeten Benachrichtigungsfensters verwendet wird, wie folgt: 
  
- Eine Nachrichtenschleife haben.
    
- Bleiben Sie während der gesamten Sitzung entsperrt.
    
- Sie haben eine längere Lebensdauer als alle anderen Threads, die vom Client erstellt wurden. 
    
Sie können auswählen, welcher Thread verwendet wird, indem Sie im ersten **MAPIInitialize-Aufruf** ein Flag festlegen. Die Gefahr, dass einer Ihrer Threads die Benachrichtigungen verarbeiten kann, besteht darin, dass das Benachrichtigungsfenster zerstört wird und Benachrichtigungen nicht mehr an ihre anderen Threads gesendet werden können, wenn der Thread nicht mehr angezeigt wird. Außerdem kann eine spezielle Verarbeitung erforderlich sein, um die Verteilung der Benachrichtigungen zu steuern, die in der Nachrichtenwarteschlange des ausgeblendeten Fensters bereitgestellt werden. 
  
Wenn Sie ein separates Fenster verwenden, um Benachrichtigungen zu behandeln, sollten Sie sicher sein, dass Benachrichtigungen zum richtigen Zeitpunkt in einem entsprechenden Thread angezeigt werden. Sie benötigen keinen speziellen Code zum Suchen und Verarbeiten der Windows Nachrichten, die im Benachrichtigungsfenster veröffentlicht werden. 
  
MAPI empfiehlt, dass die folgenden Arten von Clientanwendungen einen separaten Thread verwenden, um das ausgeblendete Fenster für die Unterstützung von Benachrichtigungen zu erstellen:
  
- Alle Multithreadclients.
    
- Singlethread-Windows-Dienste und Win32-Konsolenanwendungen.
    
- Singlethread-Clients, die ihren Hauptthread nicht für Benachrichtigungen verwenden müssen.
    
Um den separaten Threadansatz zu verwenden, rufen Sie **MAPIInitialize** für jeden Thread auf, und legen Sie das MAPI_MULTITHREAD_NOTIFICATIONS Flag fest. 
  
> [!NOTE]
> Nur der erste Aufruf eines Clients an **MAPIInitialize** bewirkt, dass ein ausgeblendetes Fenster erstellt wird, um Benachrichtigungen zu unterstützen. Nachfolgende Aufrufe führen nur dazu, dass die Anzahl der Verweise erhöht wird. 
  

