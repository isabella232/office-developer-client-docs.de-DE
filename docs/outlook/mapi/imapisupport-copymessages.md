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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405156"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Ordner verwendet werden soll, der die zu kopierende oder zu verschiebende Nachricht enthält.
    
 _lpSrcFolder_
  
> [in] Ein Zeiger auf den Ordner, der die zu kopierende oder zu verschiebende Nachricht enthält.
    
 _lpMsgList_
  
> [in] Ein Zeiger auf ein Array von Eintragsbezeichnern, die die zu kopierenden oder verschobenen Nachrichten identifizieren. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Zielordner für die kopierten oder verschobenen Nachrichten verwendet werden soll.
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den Zielordner für die kopierten oder verschobenen Nachrichten. Dieser Ordner muss geöffnet sein.
    
 _ulUIParam_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der _lpProgress-Parameter_ wird ignoriert, es sei denn, MESSAGE_DIALOG in _ulFlags festgelegt ist._
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an. Der _lpProgress-Parameter_ wird ignoriert, es sei denn, MESSAGE_DIALOG in _ulFlags festgelegt ist._
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebevorgang durchgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MESSAGE_DIALOG 
  
> Fordert die Anzeige eines Statusindikators an.
    
MESSAGE_MOVE 
  
> Die Nachrichten sollten verschoben und nicht kopiert werden. Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Kopier- oder Verschiebevorgang war erfolgreich.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::CopyMessages-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter können **IMAPISupport::CopyMessages** in ihrer Implementierung von [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) aufrufen, um eine oder mehrere Nachrichten aus einem Ordner in einen anderen zu kopieren oder zu verschieben. Im Rahmen des **IMAPISupport::CopyMessages-Aufrufs** kann der Nachrichtenspeicheranbieter angeben, dass MAPI einen Statusindikator anzeigen soll. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

