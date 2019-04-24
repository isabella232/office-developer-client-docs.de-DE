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
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280127"
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
  
> in Ein Zeiger auf ein Array von [entrylist](entrylist.md) -Strukturen, die die zu kopierende oder zu verschiebende Nachricht oder Nachrichten identifizieren. 
    
 _lpInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den Zielordner verwendet wird, auf den durch den _lpDestFolder_ -Parameter verwiesen wird. Übergeben von NULL-Ergebnissen im Dienstanbieter zurückgeben der Standardordner Schnittstelle [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Clients müssen NULL überschreiten. Andere Aufrufer können den _lpInterface_ -Parameter auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festlegen. 
    
 _lpDestFolder_
  
> in Ein Zeiger auf den geöffneten Ordner, um die kopierten oder verschobenen Nachrichten zu empfangen.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, der Client legt das MESSAGE_DIALOG-Flag im _ulFlags_ -Parameter fest und übergibt im _LPPROGRESS_ -Parameter den Wert NULL. 
    
 _lpProgress_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird in _ulFlags_festgelegt.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie der Kopier-oder Verschiebungsvorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Informiert den Nachrichtenspeicher Anbieter, dass MAPI_E_DECLINE_COPY sofort zurückgegeben wird, wenn er **IMAPIFolder:: CopyMessages** implementiert, indem er das [IMAPISupport::D ocopyto](imapisupport-docopyto.md) oder [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) -Methode des Support-Objekts aufruft. 
    
MESSAGE_DIALOG 
  
> Zeigt eine Statusanzeige an, während der Vorgang fortgesetzt wird.
    
MESSAGE_MOVE 
  
> Die Nachrichten werden nicht kopiert, sondern verschoben. Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Nachricht oder Nachrichten wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_DECLINE_COPY 
  
> Der Anbieter implementiert diese Methode durch Aufrufen einer Support Objektmethode, und der Aufrufer hat das MAPI_DECLINE_OK-Flag übergeben.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Aufruf war erfolgreich, aber nicht alle Einträge wurden erfolgreich kopiert oder verschoben. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder:: CopyMessages** -Methode kopiert oder verschiebt Nachrichten in einen anderen Ordner. 
  
Mit Lese-/Schreibzugriff geöffnete Nachrichten können verschoben oder kopiert werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie Nachrichten in einen anderen Nachrichtenspeicher kopieren, ohne die [IMAPISupport:: CopyMessages](imapisupport-copymessages.md) -Methode zu verwenden, müssen Sie zunächst [IMAPIFolder:: SETREADFLAGS](imapifolder-setreadflags.md) mit dem GENERATE_RECEIPT_ONLY-Flagsatz aufrufen. Der empfangende Nachrichtenspeicher ist nicht für das Generieren von Lese Berichten für die kopierten oder verschobenen Nachrichten verantwortlich. Wenn Sie **IMAPISupport:: CopyMessages** zum Implementieren von **IMAPIFolder:: CopyMessages**aufrufen, rufen Sie **SetReadFlags**nicht auf; MAPI wird es aufrufen. 
  
Ihre Implementierung kann die Nachrichten in beliebiger Reihenfolge verschieben oder kopieren und Lesestatus Berichte in beliebiger Reihenfolge generieren. Das heißt, Sie können das Kopieren von Nachrichten abschließen, bevor Sie einen der Lesestatus Berichte generieren, oder die Berichte senden, bevor die Implementierung den Kopiervorgang startet. Allerdings sollten Lese Berichte gesendet werden, damit alle Nachrichten kopiert werden, unabhängig davon, ob die Kopie erfolgreich war.
  
Wenn der Kopier-oder Verschiebungsvorgang mehr als eine Nachricht umfasst, führen Sie den Vorgang so vollständig wie möglich aus. Beenden Sie den Vorgang nicht vorzeitig, es sei denn, es tritt ein Fehler auf, der außerhalb Ihres Steuerelements liegt, beispielsweise ausgehender Arbeitsspeicher, unzureichender Festplattenspeicherplatz oder Beschädigung im Nachrichtenspeicher.
  
Versuchen Sie, Eintrags-IDs über Verschiebungs-oder Kopiervorgänge hinweg zu verwalten. Sie sollten auch Eintrags-IDs beibehalten, obwohl dies nicht erforderlich ist.
  
Senden von Benachrichtigungen beim Verschieben oder Kopieren von Nachrichten, sodass Clients gewarnt werden, dass die Aufrufe der Nachrichten ' [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methoden fehlschlagen. 
  
Schließen Sie den Status einer Nachricht nicht in den Kopier-oder Verschiebungsvorgang ein. Das bewegen oder Kopieren eines Nachrichtenstatus wirkt sich erheblich auf die Leistung aus.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie **IMAPIFolder:: CopyMessages** , um Suchergebnisordner aufzufüllen, in denen Nachrichten häufig nach übergeordneten Ordnern gruppiert werden. 
  
Erwarten Sie diese Rückgabewerte unter den folgenden Bedingungen.
  
|**Bedingung**|**Rückgabewert**|
|:-----|:-----|
|**IMAPIFolder:: CopyMessages** hat jede Nachricht erfolgreich kopiert oder verschoben.  <br/> |S_OK  <br/> |
|**IMAPIFolder:: CopyMessages** konnte jede Nachricht nicht erfolgreich kopieren oder verschieben.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder:: CopyMessages** konnte nicht abgeschlossen werden.  <br/> |Beliebiger Fehlerwert  <br/> |
   
Wenn **IMAPIFolder:: CopyMessages** nicht abgeschlossen werden kann, sollten Sie nicht davon ausgehen, dass keine Arbeit ausgeführt wurde. **IMAPIFolder:: CopyMessages** kann möglicherweise eine oder mehrere Nachrichten kopieren oder verschieben, bevor der Fehler auftritt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

