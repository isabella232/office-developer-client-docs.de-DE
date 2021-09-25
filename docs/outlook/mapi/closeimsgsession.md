---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3683c8dee88f26d7152789378a811c55fa70c15e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571990"
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
  
> [in] Zeiger auf das Nachrichtensitzungsobjekt, das mithilfe der [OpenIMsgSession-Funktion](openimsgsession.md) zu Beginn der Nachrichtensitzung abgerufen wurde. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Nachrichtensitzung wird von Clientanwendungen und Dienstanbietern verwendet, die sich mit mehreren verwandten **MAPI-IMessage-Objekten** befassen möchten, die auf zugrunde liegenden OLE **IStorage-Objekten** basieren. Der Client oder Anbieter verwendet die [Funktionen OpenIMsgSession](openimsgsession.md) und **CloseIMsgSession,** um die Erstellung solcher Nachrichten innerhalb einer Nachrichtensitzung einzuschließen. Nachdem die Nachrichtensitzung geöffnet wurde, übergibt der Client oder Anbieter einen Zeiger an ihn in einem Aufruf von [OpenIMsgOnIStg,](openimsgonistg.md) um ein neues **IMessage**-on- **IStorage-Objekt** zu erstellen. 
  
Eine Nachrichtensitzung verfolgt alle IMessage-on-IStorage-Objekte, die während der Dauer der Sitzung geöffnet wurden, zusätzlich zu allen Anlagen und anderen Eigenschaften der Nachrichten.  Wenn ein Client oder Anbieter **CloseIMsgSession** aufruft, werden alle diese Objekte geschlossen. Das Aufrufen von **CloseIMsgSession** ist die einzige Möglichkeit zum Schließen von IMessage-on-IStorage-Objekten.   
  

