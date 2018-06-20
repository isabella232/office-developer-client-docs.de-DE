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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791413"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**Betrifft**: Outlook 
  
Schließt eine Sofortnachrichtensitzung und alle Nachrichten, die in dieser Sitzung erstellt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Parameter

 _lpMsgSess_
  
> [in] Zeiger auf das Objekt "Message" Sitzung mithilfe der Funktion [OpenIMsgSession](openimsgsession.md) am Anfang der Nachricht Sitzung abgerufen. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Hinweise

Eine Sofortnachrichtensitzung wird von Clientanwendungen und Dienstanbieter, die für den Umgang mit mehrere verwandte MAPI- **IMessage** -Objekte auf der Basis zugrunde liegenden OLE **IStorage** -Objekte werden soll. Der Client oder Anbieter verwendet die Funktionen [OpenIMsgSession](openimsgsession.md) und **CloseIMsgSession** um die Erstellung solcher Nachrichten innerhalb einer Sofortnachrichtensitzung zu umschließen. Sobald die Nachricht Sitzung geöffnet ist, übergibt der Client oder der Anbieter einen Zeiger auf es in einem Aufruf von [OpenIMsgOnIStg](openimsgonistg.md) zum Erstellen einer neuen **IMessage**- auf - **IStorage** -Objekt. 
  
Eine Sofortnachrichtensitzung werden von nachverfolgt alle **IMessage**- auf - **IStorage** -Objekte, die während der Dauer der Sitzung, zusätzlich zu aller Anlagen und andere Eigenschaften der Nachrichten geöffnet. Wenn ein Client oder Anbieter **CloseIMsgSession**aufruft, wird dieser Objekte geschlossen. **CloseIMsgSession** aufrufen, ist die einzige Möglichkeit **IMessage**- auf - **IStorage** -Objekte zu schließen. 
  

