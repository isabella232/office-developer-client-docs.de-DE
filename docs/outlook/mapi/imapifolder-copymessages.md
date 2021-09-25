---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5cb92a74e20cddc9a7e86555980d6babdea7b32d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576051"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) die die zu kopierenden oder zu verschiebenden Nachrichten identifizieren. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Zielordner verwendet werden soll, auf den der  _lpDestFolder-Parameter_ verweist. Wenn NULL übergeben wird, gibt der Dienstanbieter die Standardordnerschnittstelle [IMAPIFolder zurück: IMAPIContainer](imapifolderimapicontainer.md). Clients müssen NULL übergeben. Andere Aufrufer können den  _parameter lpInterface_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festlegen. 
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den geöffneten Ordner, um die kopierten oder verschobenen Nachrichten zu empfangen.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. Der _ulUIParam-Parameter_ wird ignoriert, es sei denn, der Client legt das MESSAGE_DIALOG Flag im _ulFlags-Parameter_ fest und übergibt NULL im _lpProgress-Parameter._ 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag MESSAGE_DIALOG in  _ulFlags_ festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebungsvorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Informiert den Nachrichtenspeicheranbieter, sofort MAPI_E_DECLINE_COPY zurückzugeben, wenn **IMAPIFolder::CopyMessages** implementiert wird, indem die [IMAPISupport::D oCopyTo-](imapisupport-docopyto.md) oder [IMAPISupport::D oCopyProps-Methode](imapisupport-docopyprops.md) des Supportobjekts aufgerufen wird. 
    
MESSAGE_DIALOG 
  
> Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
MESSAGE_MOVE 
  
> Die Nachricht oder Die Nachrichten werden verschoben, anstatt kopiert zu werden. Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht oder Nachrichten wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_DECLINE_COPY 
  
> Der Anbieter implementiert diese Methode durch Aufrufen einer Supportobjektmethode, und der Aufrufer hat das flag MAPI_DECLINE_OK übergeben.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert oder verschoben. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::CopyMessages-Methode** kopiert oder verschiebt Nachrichten in einen anderen Ordner. 
  
Nachrichten, die mit Lese-/Schreibberechtigung geöffnet werden, können verschoben oder kopiert werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie Nachrichten in einen anderen Nachrichtenspeicher kopieren, ohne die [IMAPISupport::CopyMessages-Methode](imapisupport-copymessages.md) zu verwenden, müssen Sie zuerst [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) aufrufen, wobei das GENERATE_RECEIPT_ONLY-Flag festgelegt ist. Der empfangende Nachrichtenspeicher ist nicht für das Generieren von Leseberichten für die kopierten oder verschobenen Nachrichten verantwortlich. Wenn Sie **IMAPISupport::CopyMessages** aufrufen, um **IMAPIFolder::CopyMessages** zu implementieren, rufen Sie **setReadFlags** nicht auf; MAPI ruft sie auf. 
  
Ihre Implementierung kann die Nachrichten in beliebiger Reihenfolge verschieben oder kopieren und Lesestatusberichte in beliebiger Reihenfolge generieren. Das heißt, Sie können das Kopieren von Nachrichten beenden, bevor Sie einen der Lesestatusberichte generieren, oder die Berichte senden, bevor die Implementierung den Kopiervorgang startet. Leseberichte sollten jedoch für alle zu kopierenden Nachrichten gesendet werden, unabhängig davon, ob die Kopie erfolgreich ist.
  
Wenn der Kopier- oder Verschiebungsvorgang mehrere Nachrichten umfasst, führen Sie den Vorgang so vollständig wie möglich aus. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihrer Kontrolle liegt, z. B. zu wenig Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.
  
Versuchen Sie, Eintragsbezeichner über Verschiebungs- oder Kopiervorgänge hinweg zu verwalten. Sie sollten auch Eintragsbezeichner beibehalten, obwohl dies nicht erforderlich ist.
  
Senden Sie Benachrichtigungen, wenn Sie Nachrichten verschieben oder kopieren, damit Clients gewarnt werden, dass ihre Aufrufe an die [IMAPIProp::SaveChanges-Methoden](imapiprop-savechanges.md) der Nachrichten fehlschlagen können. 
  
Schließen Sie den Status einer Nachricht nicht in den Kopier- oder Verschiebungsvorgang ein. Das Verschieben oder Kopieren eines Nachrichtenstatus wirkt sich erheblich auf die Leistung aus.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie **IMAPIFolder::CopyMessages,** um Suchergebnisordner aufzufüllen, in denen Nachrichten häufig nach übergeordnetem Ordner gruppiert werden. 
  
Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** hat jede Nachricht erfolgreich kopiert oder verschoben.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** konnte nicht jede Nachricht erfolgreich kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **IMAPIFolder::CopyMessages** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **IMAPIFolder::CopyMessages** konnte möglicherweise eine oder mehrere Nachrichten kopieren oder verschieben, bevor der Fehler auftritt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

