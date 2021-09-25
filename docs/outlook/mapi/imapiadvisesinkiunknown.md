---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1807497f75b37b4aed041ba680cdd231337157e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600953"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementiert ein Empfehlungssenkenobjekt für die Behandlung von Benachrichtigungen. Ein Zeiger auf ein Empfehlungssenkenobjekt wird in einem Aufruf der **Advise-Methode** eines Dienstanbieters übergeben, dem Mechanismus, der zum Registrieren für Benachrichtigungen verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Empfehlen von Senkenobjekten  <br/> |
|Implementiert von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Antwortet auf eine Benachrichtigung, indem eine oder mehrere Aufgaben ausgeführt werden. Die ausgeführten Aufgaben hängen vom Ereignistyp und dem Objekt ab, das die Benachrichtigung generiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

