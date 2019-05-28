---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326194"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt und öffnet eine nachrichtensitzung, in der die darin erstellten Nachrichten gruppiert werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Parameter

 _lpMalloc_
  
> in Zeiger auf ein Speicher Zuordnungsobjekt, das die OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) -Schnittstelle verfügbar macht. MAPI muss diese Zuordnungsmethode beim Arbeiten mit der OLE- [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) -Schnittstelle verwenden. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein. 
    
 _lppMsgSess_
  
> Timeout Zeiger auf einen Zeiger auf das zurückgegebene Nachrichten Sitzungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Sitzung wurde geöffnet.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ oder _lppMsgSess_ ist NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Ungültige Flags wurden übergeben.
    
MAPI_UNICODE
  
> Beim Aufrufen dieser Funktion legt ein Client-oder Dienstanbieter das MAPI_UNICODE-Flag so fest, dass Unicode-msg-Dateien erstellt werden. Die resultierende [IMessage](imessageimapiprop.md) -Datei zeigt STORE_UNICODE_OK in seinem PR_STORE_SUPPORT_MASK und unterstützt Unicode-Eigenschaften. 
    
## <a name="remarks"></a>Hinweise

Eine nachrichtensitzung wird von Clientanwendungen und Dienstanbietern verwendet, die sich mit mehreren verwandten MAPI- [IMessage: IMAPIProp](imessageimapiprop.md) -Objekten befassen möchten, die auf zugrunde liegenden OLE **IStorage** -Objekten basieren. Der Client oder Anbieter verwendet die **OpenIMsgSession** -und [CloseIMsgSession](closeimsgsession.md) -Funktionen, um die Erstellung solcher Nachrichten in einer nachrichtensitzung einzuschließen. Nachdem die nachrichtensitzung geöffnet wurde, übergibt der Client oder Anbieter einen Zeiger darauf in einem Aufruf von [OpenIMsgOnIStg](openimsgonistg.md) , um ein neues **IMessage**-on- **IStorage** -Objekt zu erstellen. 
  
In einer nachrichtensitzung werden alle **IMessage**- **IStorage** -Objekte verfolgt, die während der Sitzungsdauer erstellt wurden, zusätzlich zu allen Anlagen und anderen Eigenschaften der Nachrichten. Wenn ein Client oder Anbieter **CloseIMsgSession**aufruft, werden alle diese Objekte geschlossen. Das Aufrufen von **CloseIMsgSession** ist die einzige Möglichkeit zum Schließen von **IMessage**-on- **IStorage** -Objekten. 
  
 **OpenIMsgSession** wird von Clients und Anbietern verwendet, die die Möglichkeit zum Verarbeiten mehrerer verwandter Nachrichten als OLE- **IStorage** -Objekte benötigen. Wenn nur eine solche Nachricht gleichzeitig geöffnet sein soll, ist es nicht erforderlich, mehrere Nachrichten zu überwachen, und es gibt keinen Grund, eine nachrichtensitzung mit **OpenIMsgSession**zu erstellen. 
  
Da es sich um ein zugrunde liegendes OLE-Objekt handelt, muss MAPI die OLE-Speicherzuweisung verwenden. Weitere Informationen zu OLE Structured Storage-Objekten und zur OLE-Speicherzuweisung finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

