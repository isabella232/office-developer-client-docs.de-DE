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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e7f652e7426792d8b4c878b7f6738439aec65348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793304"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**Betrifft**: Outlook 
  
Erstellt und öffnet eine Sofortnachrichtensitzung, die darin enthaltenen erstellten Nachrichten gruppiert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Parameter

 _lpMalloc_
  
> [in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx) -Schnittstelle verfügbar macht. MAPI muss diese Zuordnungsmethode verwenden, bei der Arbeit mit der OLE- [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx) -Schnittstelle. 
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein. 
    
 _lppMsgSess_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene Nachricht Session-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Die Sitzung geöffnet wurde.
    
MAPI_E_INVALID_PARAMETER
  
>  _LpMalloc_ oder _LppMsgSess_ ist NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Es wurden ungültige Flags übergeben.
    
PARAMETER MAPI_UNICODE
  
> Beim Aufruf von dieser Funktion wird ein Client oder Dienstanbieter die Option MAPI_UNICODE Unicode MSG-Dateien zu erstellen. Die resultierende [Imessage](imessageimapiprop.md) Datei zeigt STORE_UNICODE_OK in seiner PR_STORE_SUPPORT_MASK und Unicode-Eigenschaften unterstützt. 
    
## <a name="remarks"></a>Bemerkungen

Eine Sofortnachrichtensitzung wird von Clientanwendungen und Dienstanbieter, die für den Umgang mit mehreren möchten verwandte MAPI [IMessage: IMAPIProp](imessageimapiprop.md) Objekte auf der Basis zugrunde liegenden OLE **IStorage** -Objekte. Der Client oder Anbieter verwendet die Funktionen **OpenIMsgSession** und [CloseIMsgSession](closeimsgsession.md) um die Erstellung solcher Nachrichten innerhalb einer Sofortnachrichtensitzung zu umschließen. Sobald die Nachricht Sitzung geöffnet ist, übergibt der Client oder der Anbieter einen Zeiger auf es in einem Aufruf von [OpenIMsgOnIStg](openimsgonistg.md) zum Erstellen einer neuen **IMessage**- auf - **IStorage** -Objekt. 
  
Eine Sofortnachrichtensitzung werden von nachverfolgt alle **IMessage**- auf - **IStorage** -Objekten, die während der Dauer der Sitzung, zusätzlich zu aller Anlagen und andere Eigenschaften der Nachrichten erstellt. Wenn ein Client oder Anbieter **CloseIMsgSession**aufruft, wird dieser Objekte geschlossen. **CloseIMsgSession** aufrufen, ist die einzige Möglichkeit **IMessage**- auf - **IStorage** -Objekte zu schließen. 
  
 **OpenIMsgSession** wird von Clients und Anbietern, die die Möglichkeit, mehrere verwandte Nachrichten als OLE- **IStorage** Objekte behandelt werden müssen. Wenn nur eine dieser Nachrichten gleichzeitig geöffnet sein, besteht es keine Notwendigkeit zum Nachverfolgen von mehrere Nachrichten und keinen Grund eine Sofortnachrichtensitzung mit **OpenIMsgSession**zu erstellen. 
  
Da Umgang mit einem zugrunde liegenden OLE-Objekt muss MAPI OLE Zuweisung von virtuellem Speicher verwenden. Weitere Informationen zu OLE strukturierte Speicherobjekte und OLE-arbeitsspeicherreservierung, finden Sie unter [OLE und Daten übertragen](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

