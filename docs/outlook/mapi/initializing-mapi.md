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
  
Alle Clientanwendungen, die die MAPI-Bibliotheken verwenden, müssen die **MAPIInitialize-Funktion** aufrufen. Weitere Informationen finden Sie unter [MAPIInitialize](mapiinitialize.md). **MAPIInitialize** initialisiert globale Daten für die Sitzung und bereitet die MAPI-Bibliotheken auf die Annahme von Anrufen vor. Es gibt einige Kennzeichen, die in einigen Situationen festgelegt werden müssen: 
  
- MAPI_NT_SERVICE
    
    Legen Sie das MAPI_NT_SERVICE, wenn Ihr Client als Dienst implementiert Windows ist. Wenn Ihr Client ein Windows ist und Sie dieses Flag nicht festlegen, erkennt MAPI ihn nicht als Dienst. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    Das MAPI_MULTITHREAD_NOTIFICATIONS bezieht sich auf die Verwaltung von Benachrichtigungen durch MAPI. MAPI erstellt ein ausgeblendetes Fenster, das Fensternachrichten empfängt, wenn Änderungen an einem Objekt auftreten, das Benachrichtigungen generiert. Die Fensternachrichten werden zu einem bestimmten Zeitpunkt verarbeitet, sodass die Benachrichtigungen gesendet werden und die entsprechenden [IMAPIAdviseSink::OnNotify-Methoden](imapiadvisesink-onnotify.md) aufgerufen werden. 
    
- MAPI_NO_COINIT
    
    Legen Sie MAPI_NO_COINT-Flag fest, damit **MAPIInitialize** nicht versucht, COM mit einem Aufruf von [CoInitialize zu initialisieren.](https://msdn.microsoft.com/library/ms886303.aspx) Wenn eine **MAPIINIT_0** an **MAPIInitialize** übergeben wird und  _ulFlags_ auf MAPI_NO_COINIT festgelegt ist, geht MAPI davon aus, dass COM bereits initialisiert wurde und den Aufruf von **CoInitialize** umgehen.
    
Wenn MAPI_MULTITHREAD_NOTIFICATIONS nicht übergeben wird, erstellt MAPI das Benachrichtigungsfenster im Thread, der für den ersten **MAPIInitialize-Aufruf verwendet** wurde. MAPI erstellt das Benachrichtigungsfenster in einem separaten Thread, MAPI_MULTITHREAD_NOTIFICATIONS übergeben wird – ein Thread, der für die Verarbeitung von Benachrichtigungen verwendet wird. MAPI erwartet den Thread, der zum Erstellen des ausgeblendeten Benachrichtigungsfensters verwendet wird, für: 
  
- Verfügen Sie über eine Nachrichtenschleife.
    
- Bleiben Sie während der gesamten Lebensdauer der Sitzung unblocked.
    
- Sie haben eine längere Lebensdauer als jeder andere thread, der von Ihrem Client erstellt wurde. 
    
Sie können auswählen, welcher Thread verwendet wird, indem Sie im ersten **MAPIInitialize-Aufruf** ein Flag festlegen. Die Gefahr, dass einer Ihrer Threads die Benachrichtigungen verarbeiten kann, besteht in der Gefahr, dass das Benachrichtigungsfenster zerstört wird, wenn der Thread nicht mehr angezeigt wird und Benachrichtigungen nicht mehr an ihre anderen Threads gesendet werden können. Außerdem ist möglicherweise eine spezielle Verarbeitung erforderlich, um die Versendung der Benachrichtigungen zu steuern, die in der Nachrichtenwarteschlange des ausgeblendeten Fensters gepostet werden. 
  
Wenn Sie ein separates Fenster zum Behandeln von Benachrichtigungen verwenden, müssen Sie sicher sein, dass Benachrichtigungen zum richtigen Zeitpunkt in einem geeigneten Thread angezeigt werden. Sie benötigen keinen speziellen Code zum Überprüfen und Verarbeiten der Windows nachrichten, die im Benachrichtigungsfenster bereitgestellt werden. 
  
MAPI empfiehlt, dass die folgenden Typen von Clientanwendungen einen separaten Thread verwenden, um das ausgeblendete Fenster für die Benachrichtigungsunterstützung zu erstellen:
  
- Alle Multithreadclients.
    
- Single-Thread-Windows-Dienste und Win32-Konsolenanwendungen.
    
- Clients mit einem Thread, die ihren Hauptthread nicht für die Benachrichtigung verwenden müssen.
    
Um den separaten Threadansatz zu verwenden, rufen Sie **MAPIInitialize** für jeden Thread auf, und setzen Sie MAPI_MULTITHREAD_NOTIFICATIONS Flag. 
  
> [!NOTE]
> Nur der erste Aufruf eines Clients bei **MAPIInitialize** bewirkt, dass ein ausgeblendetes Fenster erstellt wird, um Benachrichtigungen zu unterstützen. Nachfolgende Aufrufe führen nur dazu, dass eine Verweisanzahl erhöht wird. 
  

