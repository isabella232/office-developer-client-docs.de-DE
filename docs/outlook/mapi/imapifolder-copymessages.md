---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e6e9e9cefc75ffc78ee7beb47e89063ea1a66ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792099"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**Betrifft**: Outlook 
  
Kopiert oder verschiebt eine oder mehrere Nachrichten.
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpMsgList_
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST](entrylist.md) -Strukturen, die identifizieren, zu kopieren oder Verschieben von Nachrichten. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, um Zugriff auf den Zielordner darstellt, auf den durch den Parameter _LpDestFolder_ verwiesen wird. Bei Übergabe von NULL führt den Dienstanbieter Zurückgeben der Schnittstelle Standardordner [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Clients müssen NULL übergeben. Andere Aufrufer können den Parameter _LpInterface_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festgelegt. 
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den Ordner öffnen, um die kopierte oder verschobenen Nachrichten zu empfangen.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, der Client das Flag MESSAGE_DIALOG in der _UlFlags_ -Parameter wird und übergibt NULL im _LpProgress_ -Parameter. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG in _UlFlags_festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der kopieren oder verschieben-Vorgang ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Informiert den Nachricht-Speicher-Anbieter, um sofort MAPI_E_DECLINE_COPY zurückzugeben, wenn er **IMAPIFolder::CopyMessages** implementiert, durch die des Unterstützungsobjekts [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) oder [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) -Methode aufrufen. 
    
MESSAGE_DIALOG 
  
> Eine Statusanzeige wird angezeigt, wie der-Vorgang fortgesetzt wird.
    
MESSAGE_MOVE 
  
> Nachrichten werden anstelle von verschoben werden kopiert. Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Nachricht oder die Nachrichten wurden erfolgreich verschoben oder kopiert wurde.
    
MAPI_E_DECLINE_COPY 
  
> Der Anbieter implementiert diese Methode durch den Aufruf einer Support, und der Aufrufer das Flag MAPI_DECLINE_OK verstrichen ist.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge erfolgreich kopiert oder verschoben wurden. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::CopyMessages** -Methode kopiert oder verschiebt Nachrichten in einen anderen Ordner. 
  
Nachrichten, die mit Lese-/Schreibzugriff Berechtigung verschoben oder kopiert werden kann. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie Nachrichten an einen anderen Nachrichtenspeicher ohne Verwendung der Methode [IMAPISupport::CopyMessages](imapisupport-copymessages.md) kopieren möchten, müssen Sie zunächst [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) mit dem GENERATE_RECEIPT_ONLY-Flag aufrufen. Der empfangenden Nachrichtenspeicher ist nicht verantwortlich für die kopierte oder verschobenen Nachrichten lesen Berichte zu erstellen. Wenn Sie **IMAPISupport::CopyMessages** zum Implementieren der **IMAPIFolder::CopyMessages**aufrufen, rufen Sie **SetReadFlags**nicht. MAPI wird aufgerufen. 
  
Die Implementierung kann verschieben oder Kopieren von Nachrichten in beliebiger Reihenfolge und Lesen Statusberichte in beliebiger Reihenfolge zu generieren. D. h., können Sie das Kopieren von Nachrichten vor dem Generieren eines Berichts gelesen-Status abgeschlossen oder die Berichte senden, bevor die Implementierung den Kopiervorgang beginnt. Lesen Sie jedoch für alle Nachrichten kopiert werden sollen, unabhängig davon, ob der Kopiervorgang erfolgreich war, Berichte gesendet werden soll.
  
Wenn der Vorgang kopieren oder Verschieben von mehr als eine Nachricht beteiligt sind, führen Sie den Vorgang vollständig wie möglich. Beenden Sie den Vorgang nicht vorzeitig auf, es sei denn, ein Fehler, die außerhalb Ihrer Kontrolle auftritt, wie nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder der Beschädigung im Nachrichtenspeicher ausgeführt wird.
  
Versuchen Sie, Eintragsbezeichner Verschiebe-oder Kopie zu wahren. Sie sollten auch Eintragsbezeichner, beibehalten, obwohl es nicht erforderlich ist.
  
Senden Sie Benachrichtigung, wenn Sie verschieben oder Kopieren von Nachrichten, damit Clients passieren werden, dass ihre Anrufe an die Nachrichten [IMAPIProp::SaveChanges](imapiprop-savechanges.md) Methoden fehlschlagen. 
  
Schließen Sie eine Nachricht den Status in die Kopie oder Verschiebevorgang nicht. Verschieben oder Kopieren eines Nachrichtenstatus erheblich wirkt sich auf Leistung.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie **IMAPIFolder::CopyMessages** , um Suchergebnisse Ordner, aufzufüllen, in dem Nachrichten häufig übergeordneten Ordner gruppiert werden. 
  
Diese Rückgabewerte unter folgenden Umständen zu erwarten.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** wurde erfolgreich kopiert oder jeder Nachricht verschoben.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** konnte nicht erfolgreich kopieren oder verschieben Sie jede Nachricht.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** konnte nicht abgeschlossen.  <br/> |Einen anderen Fehlerwert als  <br/> |
   
Wenn **IMAPIFolder::CopyMessages** konnte nicht abgeschlossen ist, gehen Sie nicht, dass keine Arbeit ausgeführt wurde. **IMAPIFolder::CopyMessages** wurden möglicherweise kopieren oder verschieben Sie eine oder mehrere Nachrichten vor den Fehler auftreten können. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)

