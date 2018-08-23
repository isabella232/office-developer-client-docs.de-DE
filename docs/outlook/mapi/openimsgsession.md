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
ms.openlocfilehash: 39dd053b2896ebcfcdec97d976af3e75e19f8c0b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564955"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE [IMalloc](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-imalloc) -Schnittstelle verfügbar macht. MAPI muss diese Zuordnungsmethode verwenden, bei der Arbeit mit der OLE- [IStorage](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istorage) -Schnittstelle. 
    
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Sofortnachrichtensitzung wird von Clientanwendungen und Dienstanbieter, die für den Umgang mit mehreren möchten verwandte MAPI [IMessage: IMAPIProp](imessageimapiprop.md) Objekte auf der Basis zugrunde liegenden OLE **IStorage** -Objekte. Der Client oder Anbieter verwendet die Funktionen **OpenIMsgSession** und [CloseIMsgSession](closeimsgsession.md) um die Erstellung solcher Nachrichten innerhalb einer Sofortnachrichtensitzung zu umschließen. Sobald die Nachricht Sitzung geöffnet ist, übergibt der Client oder der Anbieter einen Zeiger auf es in einem Aufruf von [OpenIMsgOnIStg](openimsgonistg.md) zum Erstellen einer neuen **IMessage**- auf - **IStorage** -Objekt. 
  
Eine Sofortnachrichtensitzung werden von nachverfolgt alle **IMessage**- auf - **IStorage** -Objekten, die während der Dauer der Sitzung, zusätzlich zu aller Anlagen und andere Eigenschaften der Nachrichten erstellt. Wenn ein Client oder Anbieter **CloseIMsgSession**aufruft, wird dieser Objekte geschlossen. **CloseIMsgSession** aufrufen, ist die einzige Möglichkeit **IMessage**- auf - **IStorage** -Objekte zu schließen. 
  
 **OpenIMsgSession** wird von Clients und Anbietern, die die Möglichkeit, mehrere verwandte Nachrichten als OLE- **IStorage** Objekte behandelt werden müssen. Wenn nur eine dieser Nachrichten gleichzeitig geöffnet sein, besteht es keine Notwendigkeit zum Nachverfolgen von mehrere Nachrichten und keinen Grund eine Sofortnachrichtensitzung mit **OpenIMsgSession**zu erstellen. 
  
Da Umgang mit einem zugrunde liegenden OLE-Objekt muss MAPI OLE Zuweisung von virtuellem Speicher verwenden. Weitere Informationen zu OLE strukturierte Speicherobjekte und OLE-arbeitsspeicherreservierung, finden Sie unter [OLE und Daten übertragen](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

