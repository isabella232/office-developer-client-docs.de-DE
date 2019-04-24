---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350918"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementiert ein Advise-Senke-Objekt zur Behandlung von Benachrichtigungen. Ein Zeiger auf ein Advise-Senke-Objekt wird in einem Aufruf an die **Advise** -Methode eines Dienstanbieters übergeben, den Mechanismus, der für die Registrierung der Benachrichtigung verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Advise-Objekt  <br/> |
|Implementiert von:  <br/> |Client Anwendungen und MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Reagiert auf eine Benachrichtigung, indem eine oder mehrere Aufgaben ausgeführt werden. Die ausgeführten Aufgaben hängen vom Ereignistyp und dem Objekt ab, das die Benachrichtigung generiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

