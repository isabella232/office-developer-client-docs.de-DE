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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393236"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Vorbereitung Formular war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::PrepareForm** -Methode erstellt eine Nachricht Token für die Meldung über den Parameter _LpMessage_ und die Nachricht [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode aufgerufen. Dieses Token wird an **IMAPISession::ShowForm**im _UlMessageToken_ -Parameter übergeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Aufruf von **PrepareForm** erfolgreich ist, Version der Meldung von _LpMessage_ dessen [IUnknown](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, bevor Sie **ShowForm aus**aufrufen. Installationsfehler, die Nachricht freigeben, bevor Sie **ShowForm aus** aufrufen kann Speicherverluste entstehen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::PrepareForm** -Methode, zusammen mit **IMAPISession::ShowForm**, um eine Nachricht in ein modales Formular anzuzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

