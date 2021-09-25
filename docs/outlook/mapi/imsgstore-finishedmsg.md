---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 45047ea14fe364f8c4d33275ba771d01f77e5110
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571675"
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner der zu verarbeitenden Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Verarbeitung der gesendeten Nachricht war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Der Nachrichtenspeicheranbieter unterstützt die Verarbeitung gesendeter Nachrichten nicht. Dieser Fehlerwert wird zurückgegeben, wenn der Aufrufer nicht der MAPI-Spooler ist.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::FinishedMsg-Methode** führt die Verarbeitung einer gesendeten Nachricht aus. Diese Verarbeitung kann das Löschen der Nachricht, das Verschieben in einen anderen Ordner oder beide Aktionen umfassen. Der Verarbeitungstyp hängt davon ab, ob die **Eigenschaften PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) und **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) festgelegt sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Entsperren Sie in Ihrer Implementierung von **FinishedMsg** die von  _lpEntryID identifizierte_ Nachricht, und führen Sie die entsprechende Verarbeitung durch. Die Zielnachricht wird immer gesperrt. Der MAPI-Spooler übergibt nie den Eintragsbezeichner für eine entsperrte Nachricht an **FinishedMsg**.
  
Es ist möglich, dass weder **PR_DELETE_AFTER_SUBMIT** noch **PR_SENTMAIL_ENTRYID** festgelegt sind, beide festgelegt sind oder eine oder die andere festgelegt ist. In der folgenden Tabelle wird die Aktion beschrieben, die Sie basierend auf den Einstellungen ausführen sollten: 
  
|||
|:-----|:-----|
|Wenn keine der beiden Eigenschaften festgelegt ist:  <br/> |Belassen Sie die Nachricht in dem Ordner, aus dem sie gesendet wurde (in der Regel der Postausgang).  <br/> |
|Wenn beide Eigenschaften festgelegt sind:  <br/> |Verschieben Sie die Nachricht in den angegebenen Ordner, falls gewünscht, und löschen Sie sie.  <br/> |
|Wenn PR_SENTMAIL_ENTRYID festgelegt ist:  <br/> |Verschieben Sie die Nachricht in den angegebenen Ordner.  <br/> |
|Wenn PR_DELETE_AFTER_SUBMIT festgelegt ist:  <br/> |Löschen Sie die Nachricht.  <br/> |
   
Nachdem Sie die entsprechende Aktion ausgeführt haben, rufen Sie die [IMAPISupport::D oSentMail-Methode](imapisupport-dosentmail.md) auf. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

