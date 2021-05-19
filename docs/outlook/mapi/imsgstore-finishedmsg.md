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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427087"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht dem Nachrichtenspeicheranbieter die Verarbeitung einer gesendeten Nachricht. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID der zu verarbeitende Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Verarbeitung der gesendeten Nachricht war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Der Nachrichtenspeicheranbieter unterstützt keine gesendete Nachrichtenverarbeitung. Dieser Fehlerwert wird zurückgegeben, wenn der Aufrufer nicht der MAPI-Spooler ist.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::FinishedMsg-Methode** führt die Verarbeitung einer gesendeten Nachricht durch. Diese Verarbeitung kann das Löschen der Nachricht, das Verschieben in einen anderen Ordner oder beide Aktionen umfassen. Der Verarbeitungstyp hängt davon ab, ob **die Eigenschaften PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) und **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) festgelegt sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Entsperren Sie in Ihrer Implementierung von **FinishedMsg** die durch  _lpEntryID_ identifizierte Nachricht, und führen Sie die entsprechende Verarbeitung aus. Die Zielnachricht wird immer gesperrt. Der MAPI-Spooler übergibt niemals den Eintragsbezeichner für eine entsperrte Nachricht an **FinishedMsg**.
  
Es ist möglich, dass **PR_DELETE_AFTER_SUBMIT** oder **PR_SENTMAIL_ENTRYID** festgelegt ist, beide festgelegt oder die eine oder die andere festgelegt ist. In der folgenden Tabelle wird die Aktion beschrieben, die Sie basierend auf den Einstellungen ergreifen sollten: 
  
|||
|:-----|:-----|
|Wenn keine eigenschaft festgelegt ist:  <br/> |Lassen Sie die Nachricht im Ordner, aus dem sie gesendet wurde (in der Regel der Posteingang).  <br/> |
|Wenn beide Eigenschaften festgelegt sind:  <br/> |Verschieben Sie die Nachricht bei Bedarf in den angegebenen Ordner, und löschen Sie sie dann.  <br/> |
|Wenn PR_SENTMAIL_ENTRYID festgelegt ist:  <br/> |Verschieben Sie die Nachricht in den angegebenen Ordner.  <br/> |
|Wenn PR_DELETE_AFTER_SUBMIT festgelegt ist:  <br/> |Löschen Sie die Nachricht.  <br/> |
   
Nachdem Sie die entsprechende Aktion ausgeführt haben, rufen Sie die [IMAPISupport::D oSentMail-Methode](imapisupport-dosentmail.md) auf. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

