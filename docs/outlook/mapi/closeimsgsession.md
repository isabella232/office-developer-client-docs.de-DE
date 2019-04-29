---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412037"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schließt eine nachrichtensitzung und alle innerhalb dieser Sitzung erstellten Nachrichten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Parameter

 _lpMsgSess_
  
> in Zeiger auf das Nachrichten Sitzungsobjekt, das mit der [OpenIMsgSession](openimsgsession.md) -Funktion zu Beginn der nachrichtensitzung abgerufen wurde. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Eine nachrichtensitzung wird von Clientanwendungen und Dienstanbietern verwendet, die mit mehreren verwandten MAPI- **IMessage** -Objekten umgehen möchten, die auf zugrunde liegenden OLE- **IStorage** -Objekten basieren. Der Client oder Anbieter verwendet die [OpenIMsgSession](openimsgsession.md) -und **CloseIMsgSession** -Funktionen, um die Erstellung solcher Nachrichten innerhalb einer nachrichtensitzung umzubrechen. Nach dem Öffnen der nachrichtensitzung übergibt der Client oder Anbieter einen Zeiger an diesen in einem Aufruf an [OpenIMsgOnIStg](openimsgonistg.md) , um ein neues **IMessage**-on- **IStorage** -Objekt zu erstellen. 
  
Eine nachrichtensitzung verfolgt alle **IMessage**-on- **IStorage** -Objekte, die während der Dauer der Sitzung geöffnet werden, zusätzlich zu allen Anlagen und anderen Eigenschaften der Nachrichten. Wenn ein Client oder Anbieter **CloseIMsgSession**aufruft, werden alle diese Objekte geschlossen. Das Aufrufen von **CloseIMsgSession** ist die einzige Möglichkeit zum Beenden von **IMessage**-on- **IStorage** -Objekten. 
  

