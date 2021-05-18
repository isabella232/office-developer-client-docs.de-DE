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
  
Schließt eine Nachrichtensitzung und alle in dieser Sitzung erstellten Nachrichten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Imessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Parameter

 _lpMsgSess_
  
> [in] Zeiger auf das Nachrichtensitzungsobjekt, das mit der [OpenIMsgSession-Funktion](openimsgsession.md) zu Beginn der Nachrichtensitzung erhalten wurde. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Eine Nachrichtensitzung wird von Clientanwendungen und Dienstanbietern verwendet, die sich mit mehreren verwandten **MAPI-IMessage-Objekten** befassen möchten, die auf zugrunde liegenden OLE **IStorage-Objekten** aufgebaut sind. Der Client oder Anbieter verwendet die [Funktionen OpenIMsgSession](openimsgsession.md) und **CloseIMsgSession,** um die Erstellung solcher Nachrichten in einer Nachrichtensitzung zu umschließen. Nachdem die Nachrichtensitzung geöffnet wurde, übergibt der Client oder Anbieter einen Zeiger an [openIMsgOnIStg,](openimsgonistg.md) um ein neues **IMessage**-on-IStorage-Objekt zu erstellen.  
  
Eine Nachrichtensitzung verfolgt alle **IMessage** **-on-IStorage-Objekte,** die während der Sitzung geöffnet wurden, zusätzlich zu allen Anlagen und anderen Eigenschaften der Nachrichten. Wenn ein Client oder Anbieter **CloseIMsgSession aufruft,** werden alle diese Objekte geschlossen. Das **Aufrufen von CloseIMsgSession** ist die einzige Möglichkeit, **IMessage**-on-IStorage-Objekte **zu** schließen. 
  

