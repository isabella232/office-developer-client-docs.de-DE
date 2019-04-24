---
title: Aufrufen von MAPI über Windows-Dienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318105"
---
# <a name="calling-mapi-from-windows-services"></a>Aufrufen von MAPI über Windows-Dienste

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um MAPI-Clientanwendungen zu aktivieren, die als Windows-Dienste für den Betrieb mit MAPI-kompatiblen Dienstanbietern geschrieben wurden, stellt MAPI mehrere Einschränkungen und Anforderungen fest.
  
MAPI-Clients weisen die folgenden Einschränkungen auf:
  
- Eine Benutzeroberfläche kann nicht zugelassen werden.
    
- Sie können Nachrichten nur über einen eng gekoppelten Nachrichtenspeicher und Transportanbieter senden. Darüber hinaus können MAPI-Clients Nachrichten nur mithilfe des Microsoft Exchange-Servers oder eines anderen Server basierten Transportanbieters senden und empfangen. Aufgrund von Identitäts-und Sicherheitsproblemen zwischen Clientanwendungen und dem MAPI-Spooler werden die meisten Transportanbieter in einem Dienst nicht unterstützt. 
    
Alle MAPI-Clientanwendungen, unabhängig davon, ob Sie als Windows-Dienste implementiert werden, müssen die [MAPIInitialize](mapiinitialize.md) -Funktion aufrufen, um die MAPI-Bibliotheken zu initialisieren. Ein Aufruf der [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) -Funktion ist auch erforderlich, um die OLE-Bibliotheken zu verwenden. Sowohl [MAPIInitialize](mapiinitialize.md) als auch [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) führen Aufrufe der [](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) Funktion zum INITIALISIEREN der Component Object Model (com)-Bibliotheken aus. Clients, die Dienste sind, müssen ein spezielles Flag, MAPI_NT_SERVICE, im **ulFlags** -Element der [MAPIINIT_0](mapiinit_0.md) -Struktur festlegen, das an [MAPIInitialize](mapiinitialize.md) und im _ulFlags_ -Parameter übergeben wird, der an die [MAPILogonEx](mapilogonex.md) übergeben wird. Funktion, um MAPI über Ihre spezielle Implementierung zu informieren. 
  
MAPI-Clients, die als Windows-Dienste geschrieben und mit der MAPI-Clientschnittstelle geschrieben wurden, haben eine zusätzliche Anforderung. Sie müssen das MAPI_NO_MAIL-Flag im Aufruf von [MAPILogonEx](mapilogonex.md)festlegen. Andere Clienttypen müssen kein Flag für die Anmeldung festlegen, da es automatisch von MAPI festgelegt wird.
  
Um Nachrichten in einem Initialisierungsthread zu behandeln, führt ein MAPI-Client, der als Dienst implementiert wird, folgende Aktionen aus:
  
1. Ruft die [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) -Funktion auf, wenn der Hauptthread blockiert. 
    
2. Ruft die [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx)-, [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)-und [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) -Sequenz von Windows-Funktionen auf, um die Nachricht zu behandeln, wenn [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) die Summe des Werts des _nCount_ -Parameters und des der Wert von **WAIT_OBJECT_0**, der angibt, dass sich eine Nachricht in der Warteschlange befindet.
    
## <a name="see-also"></a>Siehe auch



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Probleme bei der Betriebsumgebung](operating-environment-issues.md)

