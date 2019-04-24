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
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335764"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein numerisches Token, das von der [IMAPISession:: ShowForm](imapisession-showform.md) -Methode für den Zugriff auf eine Nachricht verwendet wird. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf die Nachricht verwendet werden soll. Übergeben von **null** -Ergebnissen in der Standardschnittstelle oder [IMessage](imessageimapiprop.md), wird verwendet. Der _lpInterface_ -Parameter muss **null** oder IID_IMessage sein. 
    
 _lpMessage_
  
> in Ein Zeiger auf die Nachricht, die im Formular angezeigt werden soll.
    
 _lpulMessageToken_
  
> Out Ein Zeiger auf ein Nachrichten Token, das von der **IMAPISession:: ShowForm** -Methode verwendet wird, um auf die Nachricht zuzugreifen, auf die von _lpMessage_verwiesen wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Formular Vorbereitung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::P repareform** -Methode erstellt ein Nachrichten Token für die Nachricht, auf die durch den _lpMessage_ -Parameter verwiesen wird, und ruft die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode der Nachricht auf. Dieses Token wird im _ulMessageToken_ -Parameter an **IMAPISession:: ShowForm**übergeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Aufruf von **PrepareForm** erfolgreich ist, veröffentlichen Sie die Nachricht, auf die durch _lpMessage_ verwiesen wird, indem Sie die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, bevor Sie **ShowForm**aufrufen. Wenn Sie die Nachricht nicht freigeben, bevor Sie **ShowForm** aufrufen, kann dies zu Speicherverlusten führen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI verwendet die **IMAPISession::P repareform** -Methode zusammen mit **IMAPISession:: ShowForm**, um eine Nachricht in einem modalen Formular anzuzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

