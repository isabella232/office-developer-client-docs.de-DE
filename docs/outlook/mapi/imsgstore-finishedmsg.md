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
  
Ermöglicht dem Nachrichtenspeicher Anbieter das Ausführen der Verarbeitung für eine gesendete Nachricht. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID der zu verarbeitenden Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Verarbeitung der gesendeten Nachricht war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Der Nachrichtenspeicher Anbieter unterstützt keine gesendete Nachrichtenverarbeitung. Dieser Fehlerwert wird zurückgegeben, wenn der Aufrufer nicht der MAPI-Spooler ist.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: FinishedMsg** -Methode führt eine Verarbeitung für eine gesendete Nachricht aus. Bei dieser Verarbeitung kann es sich um das Löschen der Nachricht, die Verschiebung in einen anderen Ordner oder um beide Aktionen handeln. Die Art der Verarbeitung hängt davon ab, ob die Eigenschaften **PR_DELETE_AFTER_SUBMIT** ([Pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md)) und **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md)) festgelegt sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Entsperren Sie in ihrer Implementierung von **FinishedMsg**die Nachricht, die von _lpEntryID_ identifiziert wurde, und führen Sie die entsprechende Verarbeitung aus. Die Zielnachricht ist immer gesperrt; der MAPI-Spooler übergibt nie den Eintragsbezeichner für eine nicht gesperrte Nachricht an **FinishedMsg**.
  
Es ist möglich, dass weder **PR_DELETE_AFTER_SUBMIT** noch **PR_SENTMAIL_ENTRYID** festgelegt ist, beides festgelegt ist oder die andere festgelegt ist. In der folgenden Tabelle wird die Aktion beschrieben, die Sie auf der Grundlage der Einstellungen ergreifen sollten: 
  
|||
|:-----|:-----|
|Wenn keine Eigenschaft festgelegt ist:  <br/> |BeLassen Sie die Nachricht in dem Ordner, von dem Sie gesendet wurde (in der Regel der Postausgang).  <br/> |
|Wenn beide Eigenschaften festgelegt sind:  <br/> |Verschieben Sie die Nachricht, falls gewünscht, in den angegebenen Ordner, und löschen Sie Sie.  <br/> |
|Wenn PR_SENTMAIL_ENTRYID festgelegt ist:  <br/> |Verschieben Sie die Nachricht in den angegebenen Ordner.  <br/> |
|Wenn PR_DELETE_AFTER_SUBMIT festgelegt ist:  <br/> |Löschen Sie die Nachricht.  <br/> |
   
Wenn Sie alle geeigneten Aktionen ausgeführt haben, rufen Sie die [IMAPISupport::D osentmail](imapisupport-dosentmail.md) -Methode auf. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

