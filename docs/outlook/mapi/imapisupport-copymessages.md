---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3ca7f2b32dd04bf46f1d150ad0d30213045f27e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575841"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt Nachrichten von einem Ordner in einen anderen Ordner.
  
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
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Ordner verwendet werden soll, der die zu kopierenden oder zu verschiebenden Nachrichten enthält.
    
 _lpSrcFolder_
  
> [in] Ein Zeiger auf den Ordner, der die zu kopierenden oder zu verschiebenden Nachrichten enthält.
    
 _lpMsgList_
  
> [in] Ein Zeiger auf ein Array von Eintragsbezeichnern, die die zu kopierenden oder zu verschiebenden Nachrichten identifizieren. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Zielordner für die kopierten oder verschobenen Nachrichten verwendet werden soll.
    
 _lpDestFolder_
  
> [in] Ein Zeiger auf den Zielordner für die kopierten oder verschobenen Nachrichten. Dieser Ordner muss geöffnet sein.
    
 _ulUIParam_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag MESSAGE_DIALOG in  _ulFlags_ festgelegt ist.
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt. Wenn NULL in  _lpProgress_ übergeben wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierungen eine Statusanzeige an. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag MESSAGE_DIALOG in  _ulFlags_ festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebungsvorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
MESSAGE_DIALOG 
  
> Fordert die Anzeige einer Statusanzeige an.
    
MESSAGE_MOVE 
  
> Die Nachrichten sollten verschoben werden, anstatt sie zu kopieren. Wenn MESSAGE_MOVE nicht festgelegt ist, werden die Nachrichten kopiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Kopier- oder Verschiebungsvorgang war erfolgreich.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::CopyMessages-Methode** ist für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter können **IMAPISupport::CopyMessages** in ihrer Implementierung von [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) aufrufen, um eine oder mehrere Nachrichten von einem Ordner in einen anderen zu kopieren oder zu verschieben. Im Rahmen des **IMAPISupport::CopyMessages-Aufrufs** kann der Nachrichtenspeicheranbieter angeben, dass die MAPI eine Statusanzeige anzeigen soll. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

