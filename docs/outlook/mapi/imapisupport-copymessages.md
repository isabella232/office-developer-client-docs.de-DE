---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 64b2c147acb02b6c29cf080076b6fe2e3eefb717
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792346"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Betrifft**: Outlook 
  
Kopiert oder verschiebt Nachrichten aus einem Ordner in einen anderen Ordner.
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpSrcInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle dar, verwendet werden soll, auf den Ordner zugreifen, der enthält die Nachrichten, kopiert oder verschoben werden soll.
    
 _lpSrcFolder_
  
> [in] Ein Zeiger auf den Ordner mit der Nachrichten an kopiert oder verschoben werden sollen.
    
 _lpMsgList_
  
> [in] Ein Zeiger auf ein Array von Eintragsbezeichner, mit denen die Nachrichten, kopiert oder verschoben werden soll. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugriff auf den Zielordner für die kopierte oder verschobenen Nachrichten zu verwendende darstellt.
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den Zielordner für die Nachrichten kopierten oder verschoben. In diesem Ordner muss geöffnet sein.
    
 _ulUIParam_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG in _UlFlags_festgelegt ist.
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt. Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter eine Statusanzeige mithilfe der MAPI-Fortschritt objektimplementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MESSAGE_DIALOG in _UlFlags_festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der kopieren oder verschieben-Vorgang ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MESSAGE_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige.
    
MESSAGE_MOVE 
  
> Die Nachrichten verschoben werden soll, sondern kopiert. Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Kopieren oder verschieben-Vorgang erfolgreich war.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::CopyMessages** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert. Nachricht-Anbieter können in ihrer Durchführung des [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) zu kopieren oder verschieben eine oder mehrere Nachrichten aus einem Ordner in einen anderen **IMAPISupport::CopyMessages** aufrufen. Teil des Aufrufs **IMAPISupport::CopyMessages** kann der Nachricht Speicheranbieter angeben, dass MAPI eine Statusanzeige angezeigt werden sollen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

