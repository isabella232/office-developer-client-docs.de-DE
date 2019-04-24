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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356532"
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
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den Ordner verwendet werden soll, der die Nachrichten enthält, die kopiert oder verschoben werden sollen.
    
 _lpSrcFolder_
  
> in Ein Zeiger auf den Ordner, der die Nachrichten enthält, die kopiert oder verschoben werden sollen.
    
 _lpMsgList_
  
> in Ein Zeiger auf ein Array von Eintrags Bezeichnern, die die Nachrichten identifizieren, die kopiert oder verschoben werden sollen. 
    
 _lpDestInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den Zielordner für die kopierten oder verschobenen Nachrichten verwendet werden soll.
    
 _lpDestFolder_
  
> in Ein Zeiger auf den Zielordner für die kopierten oder verschobenen Nachrichten. Dieser Ordner muss geöffnet sein.
    
 _ulUIParam_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird in _ulFlags_festgelegt.
    
 _lpProgress_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt. Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MESSAGE_DIALOG-Flag wird in _ulFlags_festgelegt.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie der Kopier-oder Verschiebungsvorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
MESSAGE_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an.
    
MESSAGE_MOVE 
  
> Die Nachrichten sollten verschoben und nicht kopiert werden. Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Kopier-oder Verschiebungsvorgang war erfolgreich.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: CopyMessages** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter können **IMAPISupport:: CopyMessages** in ihrer Implementierung von [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) aufrufen, um eine oder mehrere Nachrichten von einem Ordner in einen anderen zu kopieren oder zu verschieben. Als Teil des **IMAPISupport:: CopyMessages** -Aufrufs kann der Nachrichtenspeicher Anbieter angeben, dass MAPI eine Statusanzeige anzeigen soll. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

