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
  
Erstellt und öffnet eine Nachrichtensitzung, die die in ihr erstellten Nachrichten gruppen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Imessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Parameter

 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE [IMalloc-Schnittstelle verfügbar](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) machen soll. MAPI muss diese Zuordnungsmethode verwenden, wenn sie mit der OLE [IStorage-Schnittstelle](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) arbeitet. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein. 
    
 _lppMsgSess_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Nachrichtensitzungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Sitzung wurde geöffnet.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ oder  _lppMsgSess_ ist NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Ungültige Flags wurden übergeben.
    
MAPI_UNICODE
  
> Beim Aufrufen dieser Funktion legt ein Client oder Dienstanbieter das MAPI_UNICODE fest, um Unicode-MSG-Dateien zu erstellen. Die resultierende [Imessage-Datei](imessageimapiprop.md) STORE_UNICODE_OK in ihrer PR_STORE_SUPPORT_MASK und unterstützt Unicode-Eigenschaften. 
    
## <a name="remarks"></a>Hinweise

Eine Nachrichtensitzung wird von Clientanwendungen und Dienstanbietern verwendet, die sich mit mehreren verwandten MAPI [IMessage : IMAPIProp-Objekten](imessageimapiprop.md) befassen möchten, die auf zugrunde liegenden OLE **IStorage-Objekten** basieren. Der Client oder Anbieter verwendet die **Funktionen OpenIMsgSession** und [CloseIMsgSession,](closeimsgsession.md) um die Erstellung solcher Nachrichten in einer Nachrichtensitzung zu umschließen. Nachdem die Nachrichtensitzung geöffnet wurde, übergibt der Client oder Anbieter einen Zeiger an [openIMsgOnIStg,](openimsgonistg.md) um ein neues **IMessage**-on-IStorage-Objekt zu erstellen.  
  
Eine Nachrichtensitzung verfolgt alle **IMessage** **-on-IStorage-Objekte,** die während der Sitzung erstellt wurden, zusätzlich zu allen Anlagen und anderen Eigenschaften der Nachrichten. Wenn ein Client oder Anbieter **CloseIMsgSession aufruft,** werden alle diese Objekte geschlossen. Das **Aufrufen von CloseIMsgSession** ist die einzige Möglichkeit, **IMessage**-on-IStorage-Objekte **zu** schließen. 
  
 **OpenIMsgSession** wird von Clients und Anbietern verwendet, die die Möglichkeit benötigen, mehrere verwandte Nachrichten als OLE **IStorage-Objekte zu** behandeln. Wenn nur eine solche Nachricht gleichzeitig geöffnet werden soll, müssen sie nicht mehrere Nachrichten nachverfolgen und es gibt keinen Grund, eine Nachrichtensitzung mit **OpenIMsgSession zu erstellen.** 
  
Da es sich um ein zugrunde liegendes OLE-Objekt handelt, muss MAPI die OLE-Speicherzuordnung verwenden. Weitere Informationen zu strukturierten OLE-Speicherobjekten und der OLE-Speicherzuweisung finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

