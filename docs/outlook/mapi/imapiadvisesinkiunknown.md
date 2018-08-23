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
ms.openlocfilehash: b9244e28337c74487562ec235f246559a49a390d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573803"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Implementiert eine Advise-Empfängerobjekt für die Verarbeitung der Benachrichtigung. Ein Zeiger auf eine Advise-Empfängerobjekt wird in einem Aufruf des Dienstanbieters **Advise** -Methode verwendeten Mechanismus zum Registrieren für die Benachrichtigung übergeben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verfügbar gemacht von:  <br/> |Beraten der Empfängerobjekten  <br/> |
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

