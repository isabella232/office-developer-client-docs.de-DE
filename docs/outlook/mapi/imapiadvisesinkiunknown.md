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
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792055"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Betrifft**: Outlook 
  
Implementiert eine Advise-Empfängerobjekt für die Verarbeitung der Benachrichtigung. Ein Zeiger auf eine Advise-Empfängerobjekt wird in einem Aufruf des Dienstanbieters **Advise** -Methode verwendeten Mechanismus zum Registrieren für die Benachrichtigung übergeben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Beraten der Empfängerobjekten  <br/> |
|Implementiert von:  <br/> |Clientanwendungen und MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Zeigertyp:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Antwortet auf eine Benachrichtigung durch eine oder mehrere Aufgaben ausführen. Die Aufgaben ausgeführt, abhängig von den Typ des Ereignisses und das Objekt, das die Benachrichtigung generiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

