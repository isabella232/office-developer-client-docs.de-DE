---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 026a120406b714a50a9191e4761021693a250b94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792319"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Betrifft**: Outlook 
  
Erstellt eine numerische Token, das die [IMAPISession::ShowForm](imapisession-showform.md) -Methode verwendet, um auf eine Nachricht zuzugreifen. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugriff auf die Nachricht zu verwendende darstellt. Übergeben von **null** führt in der standard-Benutzeroberfläche oder [IMessage](imessageimapiprop.md), verwendet wird. Der Parameter _LpInterface_ muss **null** oder IID_IMessage sein. 
    
 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht, die im Formular angezeigt werden.
    
 _lpulMessageToken_
  
> [out] Ein Zeiger auf ein Token Nachricht, die von der **IMAPISession::ShowForm** -Methode zum Zugriff auf die Meldung _LpMessage_verwendet wird.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Vorbereitung Formular war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::PrepareForm** -Methode erstellt eine Nachricht Token für die Meldung über den Parameter _LpMessage_ und die Nachricht [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) -Methode aufgerufen. Dieses Token wird an **IMAPISession::ShowForm**im _UlMessageToken_ -Parameter übergeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Aufruf von **PrepareForm** erfolgreich ist, Version der Meldung von _LpMessage_ dessen [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, bevor Sie **ShowForm aus**aufrufen. Installationsfehler, die Nachricht freigeben, bevor Sie **ShowForm aus** aufrufen kann Speicherverluste entstehen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::PrepareForm** -Methode, zusammen mit **IMAPISession::ShowForm**, um eine Nachricht in ein modales Formular anzuzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

