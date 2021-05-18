---
title: Aufrufen von MAPI von Windows Diensten
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
# <a name="calling-mapi-from-windows-services"></a>Aufrufen von MAPI von Windows Diensten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um mapi-client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.
  
FÜR MAPI-Clients gelten die folgenden Einschränkungen:
  
- Sie können keine Benutzeroberfläche zulassen.
    
- Sie können Nachrichten nur über einen eng gekoppelten Nachrichtenspeicher und Transportanbieter senden. Darüber hinaus können MAPI-Clients Nachrichten nur mithilfe des Microsoft Exchange Server oder eines anderen serverbasierten Transportanbieters senden und empfangen. Aufgrund von Identitäts- und Sicherheitsproblemen zwischen Clientanwendungen und dem MAPI-Spooler werden die meisten Transportanbieter in einem Dienst nicht unterstützt. 
    
Alle MAPI-Clientanwendungen, unabhängig davon, ob sie als Windows implementiert werden, müssen die [MAPIInitialize-Funktion](mapiinitialize.md) aufrufen, um die MAPI-Bibliotheken zu initialisieren. Ein Aufruf der [OleInitialize-Funktion](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) ist auch erforderlich, um die OLE-Bibliotheken zu verwenden. Sowohl [MAPIInitialize](mapiinitialize.md) als auch [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) rufen die [CoInitialize-Funktion](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) auf, um die COM-Bibliotheken (Component Object Model) zu initialisieren. Clients, die Dienste sind, müssen ein spezielles Flag MAPI_NT_SERVICE im **ulFlags-Element** der [MAPIINIT_0-Struktur](mapiinit_0.md) festlegen, das an [MAPIInitialize](mapiinitialize.md) und den  _ulFlags-Parameter_ übergeben wird, der an die [MAPILogonEx-Funktion](mapilogonex.md) übergeben wird, um MAPI über die spezielle Implementierung zu informieren. 
  
MAPI-Clients, die als Windows geschrieben und mit der MAPI-Clientschnittstelle geschrieben werden, haben eine zusätzliche Anforderung. Sie müssen das MAPI_NO_MAIL im Aufruf von [MAPILogonEx festlegen.](mapilogonex.md) Andere Typen von Clients müssen kein Kennzeichen für die Anmeldung festlegen, da es automatisch von MAPI festgelegt wird.
  
Um Nachrichten in einem Initialisierungsthread zu verarbeiten, führt ein als Dienst implementierter MAPI-Client die folgenden Schritte aus:
  
1. Ruft die [MsgWaitForMultipleObjects-Funktion auf,](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) wenn der Hauptthread blockiert wird. 
    
2. Ruft die [GetMessage-,](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx) [TranslateMessage-](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)und [DispatchMessage-Sequenz](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) von Windows-Funktionen auf, um die Nachricht zu behandeln, wenn [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) die Summe des Werts des _Parameters nCount_ und den Wert von **WAIT_OBJECT_0** zurückgibt, der angibt, dass sich eine Nachricht in der Warteschlange befindet.
    
## <a name="see-also"></a>Siehe auch



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[Probleme mit der Betriebsumgebung](operating-environment-issues.md)

