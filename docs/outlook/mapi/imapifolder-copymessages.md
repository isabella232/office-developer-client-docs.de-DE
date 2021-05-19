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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424455"
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
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) die die zu kopierende oder verschiebende Nachricht oder Nachrichten identifizieren. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Zielordner verwendet werden soll, auf den der  _lpDestFolder-Parameter_ verweist. Das Übergeben von NULL führt dazu, dass der Dienstanbieter die Standardordnerschnittstelle [IMAPIFolder : IMAPIContainer zurück gibt.](imapifolderimapicontainer.md) Clients müssen NULL übergeben. Andere Aufrufer können den  _lpInterface-Parameter_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den geöffneten Ordner, um die kopierten oder verschobenen Nachrichten zu empfangen.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. Der _ulUIParam-Parameter_ wird ignoriert, es sei denn, der Client legt das MESSAGE_DIALOG im _ulFlags-Parameter_ fest und übergibt NULL im _lpProgress-Parameter._ 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der _lpProgress-Parameter_ wird ignoriert, es sei denn, MESSAGE_DIALOG in _ulFlags festgelegt ist._
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebevorgang durchgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Informiert den Nachrichtenspeicheranbieter, MAPI_E_DECLINE_COPY sofort zurückzukehren, wenn **er IMAPIFolder::CopyMessages** implementiert, indem die [IMAPISupport::D oCopyTo-](imapisupport-docopyto.md) oder [IMAPISupport::D oCopyProps-Methode](imapisupport-docopyprops.md) des Supportobjekts aufruft. 
    
MESSAGE_DIALOG 
  
> Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
MESSAGE_MOVE 
  
> Die Nachricht oder Nachrichten sollen verschoben werden, anstatt sie zu kopieren. Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht oder Nachrichten wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_DECLINE_COPY 
  
> Der Anbieter implementiert diese Methode durch Aufrufen einer Supportobjektmethode, und der Aufrufer hat das MAPI_DECLINE_OK übergeben.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf ist erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert oder verschoben. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::CopyMessages-Methode** kopiert oder verschiebt Nachrichten in einen anderen Ordner. 
  
Nachrichten, die mit Lese-/Schreibberechtigung geöffnet werden, können verschoben oder kopiert werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie Nachrichten in einen anderen Nachrichtenspeicher kopieren, ohne die [IMAPISupport::CopyMessages-Methode](imapisupport-copymessages.md) zu verwenden, müssen Sie zunächst [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) mit dem GENERATE_RECEIPT_ONLY aufrufen. Der empfangende Nachrichtenspeicher ist nicht für das Generieren von Leseberichten für die kopierten oder verschobenen Nachrichten verantwortlich. Wenn Sie **IMAPISupport::CopyMessages** aufrufen, um **IMAPIFolder::CopyMessages** zu implementieren, rufen Sie **SetReadFlags** nicht auf. MAPI wird es aufrufen. 
  
Ihre Implementierung kann die Nachrichten in beliebiger Reihenfolge verschieben oder kopieren und Lesestatusberichte in beliebiger Reihenfolge generieren. Das heißt, Sie können das Kopieren von Nachrichten beenden, bevor Sie einen der Lesestatusberichte generieren oder die Berichte senden, bevor Die Implementierung den Kopiervorgang startet. Leseberichte sollten jedoch gesendet werden, damit alle Nachrichten kopiert werden, unabhängig davon, ob die Kopie erfolgreich ist.
  
Wenn der Kopier- oder Verschiebevorgang mehrere Nachrichten umfasst, führen Sie den Vorgang so vollständig wie möglich aus. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der sich außerhalb Ihres Steuerelements befindet, z. B. nicht genügend Arbeitsspeicher, nicht genügend Speicherplatz oder Beschädigungen im Nachrichtenspeicher.
  
Versuchen Sie, Eintragsbezeichner für alle Verschieben- oder Kopiervorgänge zu verwalten. Sie sollten auch Eintragsbezeichner beibehalten, obwohl sie nicht erforderlich sind.
  
Senden Sie Benachrichtigungen, wenn Sie Nachrichten verschieben oder kopieren, damit Clients darauf warnt werden, dass ihre Aufrufe der [IMAPIProp::SaveChanges-Methoden](imapiprop-savechanges.md) der Nachrichten fehlschlagen können. 
  
Schließen Sie den Status einer Nachricht nicht in den Kopier- oder Verschiebevorgang ein. Das Verschieben oder Kopieren eines Nachrichtenstatus wirkt sich stark auf die Leistung aus.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden **Sie IMAPIFolder::CopyMessages** zum Auffüllen von Suchergebnissenordnern, in denen Nachrichten häufig nach übergeordneten Ordnern gruppieren. 
  
Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**R�ckgabewert**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** hat jede Nachricht erfolgreich kopiert oder verschoben.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** konnte nicht jede Nachricht erfolgreich kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **IMAPIFolder::CopyMessages** nicht abgeschlossen werden kann, gehen Sie nicht davon aus, dass keine Arbeit ausgeführt wurde. **IMAPIFolder::CopyMessages** konnte möglicherweise eine oder mehrere Nachrichten kopieren oder verschieben, bevor der Fehler aufgetreten ist. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

