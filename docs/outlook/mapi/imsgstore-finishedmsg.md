---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9da9a13f87eac097fba078da1f1d6c3f78f69c0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792637"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**Betrifft**: Outlook 
  
Aktiviert den Nachricht-Speicher-Anbieter für die Verarbeitung für eine gesendete Nachricht. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID der Nachricht verarbeitet werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Verarbeitung für die gesendete Nachricht war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Die Nachrichtenanbieter unterstützt keine Verarbeitung von gesendeten Nachrichten. Dieser Fehlerwert wird zurückgegeben, wenn der Aufrufer nicht die MAPI-Warteschlange befindet.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::FinishedMsg** -Methode führt die Verarbeitung für eine gesendete Nachricht. Löschen der Nachricht in einem anderen Ordner oder beide Aktionen verschieben betreffen diese Verarbeitung. Die Art der Verarbeitung hängt davon ab, ob die **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) und **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) Eigenschaften festgelegt werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Entsperren Sie in der Implementierung der **FinishedMsg**die Nachricht vom _LpEntryID_ , und führen Sie die entsprechende Verarbeitung. Die Zielnachricht wird immer gesperrt werden. die MAPI-Warteschlange übergibt die Eintrags-ID für eine nicht gesperrte Nachricht nie an **FinishedMsg**.
  
Es ist möglich, dass weder **PR_DELETE_AFTER_SUBMIT** oder **PR_SENTMAIL_ENTRYID** festgelegt ist, beide festgelegt werden oder mindestens eine der anderen festgelegt ist. Die folgende Tabelle beschreibt die Aktion, die Sie basierend auf der Einstellungen ausgeführt werden soll: 
  
|||
|:-----|:-----|
|Wenn weder-Eigenschaft festgelegt ist:  <br/> |Lassen Sie die Nachricht in den Ordner, von dem sie (in der Regel im Ordner Postausgang) gesendet wurde.  <br/> |
|Wenn beide Eigenschaften festgelegt werden:  <br/> |Verschieben der Nachricht in den angegebenen Ordner, falls gewünscht, und löschen Sie ihn.  <br/> |
|Wenn PR_SENTMAIL_ENTRYID festgelegt ist:  <br/> |Verschieben der Nachricht in den angegebenen Ordner.  <br/> |
|Wenn PR_DELETE_AFTER_SUBMIT festgelegt ist:  <br/> |Löschen der Nachricht.  <br/> |
   
Nachdem Sie die geeignete Aktion durchgeführt haben, rufen Sie die [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

