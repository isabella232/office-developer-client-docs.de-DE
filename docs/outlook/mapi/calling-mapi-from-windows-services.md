---
title: Aufrufen von MAPI-Anruf über Windows-Dienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6465b2d24c3a38da40f2d1e6df79c2fa256b64b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791365"
---
# <a name="calling-mapi-from-windows-services"></a>Aufrufen von MAPI-Anruf über Windows-Dienste

  
  
**Betrifft**: Outlook 
  
Um MAPI-Clientanwendungen zu aktivieren, die als Windows-Dienste für den Betrieb mit MAPI-kompatible Dienstanbieter geschrieben werden, erfordert MAPI verschiedene Einschränkungen und Anforderungen.
  
MAPI-Clients bieten die folgenden Nachteile:
  
- Sie können eine Benutzeroberfläche nicht zulassen.
    
- Sie können Nachrichten nur über einen eng gekoppelten Nachrichtenspeicher und Transport Anbieter. Darüber hinaus können MAPI-Clients senden und Empfangen von Nachrichten mithilfe von nur die Microsoft Exchange-Server oder einen anderen Server-basierten Transportanbieter. Aufgrund des Identität und Sicherheit zwischen Clientanwendungen und die MAPI-Warteschlange sind die meisten Transportanbieter in einem Dienst nicht unterstützt. 
    
Alle MAPI-Clientanwendungen, ob sie als Windows-Dienste implementiert werden, müssen die Funktion ["MAPIInitialize"](mapiinitialize.md) zum Initialisieren der MAPI-Bibliotheken aufrufen. Ein Aufruf der Funktion [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) ist auch erforderlich, die OLE-Bibliotheken verwenden. ["MAPIInitialize"](mapiinitialize.md) und [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) tätigen von Anrufen an die Funktion [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) die Bibliotheken Component Object Model (COM) nicht initialisiert werden. Clients, die Dienste sind müssen ein spezielles Flag, MAPI_NT_SERVICE, legen Sie im **UlFlags** -Member der [MAPIINIT_0](mapiinit_0.md) -Struktur, die ["MAPIInitialize"](mapiinitialize.md) übergeben wird, und die _UlFlags_ -Parameter, der an die [MAPILogonEx](mapilogonex.md) übergeben wird Funktion, um die spezielle Implementierung MAPI zu informieren. 
  
MAPI-Clients, die als Windows-Dienste und mit der MAPI-Client-Schnittstelle geschrieben werden müssen, eine zusätzliche Anforderung. Sie müssen das Flag MAPI_NO_MAIL im Aufruf [MAPILogonEx](mapilogonex.md)festgelegt. Andere Typen von Clients müssen kein Flag für die Anmeldung festgelegt werden, da er automatisch vom MAPI festgelegt wurde.
  
Zur Verarbeitung von Nachrichten in einem Initialisierungsthread, führt ein MAPI-Client, der als Dienst implementiert wird Folgendes aus:
  
1. Ruft die [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) Funktion bei der Hauptthread blockiert. 
    
2. Ruft die [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx) [TranslateMessage](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx)und [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) Abfolge der Windows-Funktionen in der Nachricht behandelt [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) die Summe der Wert des Parameters _nCount_ zurückgibt und die der Wert der **WAIT_OBJECT_0**, die angibt, dass eine Meldung in der Warteschlange ist.
    
## <a name="see-also"></a>Siehe auch



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Probleme in der Betriebssystemumgebung](operating-environment-issues.md)

