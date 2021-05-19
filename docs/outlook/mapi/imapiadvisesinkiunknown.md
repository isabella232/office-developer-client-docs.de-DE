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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409566"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementiert ein Advise Sink-Objekt für die Behandlung von Benachrichtigungen. Ein Zeiger auf ein Advise Sink-Objekt wird in einem Aufruf der **Advise-Methode** eines Dienstanbieters übergeben, dem Mechanismus, der zum Registrieren für Benachrichtigungen verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Beraten von Sinkobjekten  <br/> |
|Implementiert von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Antwortet auf eine Benachrichtigung, indem mindestens eine Aufgabe ausgeführt wird. Die ausgeführten Aufgaben hängen vom Typ des Ereignisses und dem Objekt ab, das die Benachrichtigung generiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

