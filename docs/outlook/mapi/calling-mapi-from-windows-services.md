---
title: Aufrufen der MAPI über Windows-Dienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 460c214c5bc713c9cd644a9afc85c37a895ad58c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576541"
---
# <a name="calling-mapi-from-windows-services"></a>Aufrufen der MAPI über Windows-Dienste

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Damit MAPI-Clientanwendungen, die als Windows-Dienste geschrieben werden, mit MAPI-kompatiblen Dienstanbietern arbeiten können, gelten für die MAPI mehrere Einschränkungen und Anforderungen.
  
FÜR MAPI-Clients gelten die folgenden Einschränkungen:
  
- Sie können keine Benutzeroberfläche zulassen.
    
- Nachrichten können nur über einen eng gekoppelten Nachrichtenspeicher und Transportanbieter gesendet werden. Darüber hinaus können MAPI-Clients Nachrichten nur mithilfe der Microsoft Exchange Server oder eines anderen serverbasierten Transportanbieters senden und empfangen. Aufgrund von Identitäts- und Sicherheitsproblemen zwischen Clientanwendungen und dem MAPI-Spooler werden die meisten Transportanbieter in einem Dienst nicht unterstützt. 
    
Alle MAPI-Clientanwendungen, unabhängig davon, ob sie als Windows-Dienste implementiert sind, müssen die [MAPIInitialize-Funktion](mapiinitialize.md) aufrufen, um die MAPI-Bibliotheken zu initialisieren. Ein Aufruf der [OleInitialize-Funktion](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) ist auch erforderlich, um die OLE-Bibliotheken zu verwenden. Sowohl [MAPIInitialize](mapiinitialize.md) als [auch OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) rufen die [CoInitialize-Funktion](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) auf, um die COM-Bibliotheken (Component Object Model) zu initialisieren. Clients, die Dienste sind, müssen ein spezielles Flag MAPI_NT_SERVICE im **ulFlags-Element** der [MAPIINIT_0](mapiinit_0.md) Struktur festlegen, die an [MAPIInitialize](mapiinitialize.md) übergeben wird, und im  _ulFlags-Parameter,_ der an die [MAPILogonEx-Funktion](mapilogonex.md) übergeben wird, um die MAPI über ihre spezielle Implementierung zu informieren. 
  
MAPI-Clients, die als Windows-Dienste geschrieben und mit der MAPI-Clientschnittstelle geschrieben werden, müssen zusätzlich erforderlich sein. Sie müssen das flag MAPI_NO_MAIL im Aufruf von [MAPILogonEx](mapilogonex.md)festlegen. Andere Arten von Clients müssen kein Kennzeichen für die Anmeldung festlegen, da sie automatisch von MAPI festgelegt werden.
  
Um Nachrichten in einem Initialisierungsthread zu verarbeiten, führt ein MAPI-Client, der als Dienst implementiert ist, folgende Aktionen aus:
  
1. Ruft die [MsgWaitForMultipleObjects-Funktion](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) auf, wenn der Hauptthread blockiert wird. 
    
2. Ruft die [Sequenz getMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)und [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) von Windows Funktionen auf, um die Nachricht zu verarbeiten, wenn [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) die Summe des Werts des _nCount-Parameters_ und den Wert von **WAIT_OBJECT_0** zurückgibt, der angibt, dass sich eine Nachricht in der Warteschlange befindet.
    
## <a name="see-also"></a>Siehe auch



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Probleme mit der Betriebsumgebung](operating-environment-issues.md)

