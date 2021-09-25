---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3567a0bc4c24ecdeefe6d58fe0075b1979001407
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561516"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein numerisches Token, das die [IMAPISession::ShowForm-Methode](imapisession-showform.md) verwendet, um auf eine Nachricht zuzugreifen. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf die Nachricht verwendet werden soll. Das Übergeben von **NULL** führt dazu, dass die Standardschnittstelle [(IMessage)](imessageimapiprop.md)verwendet wird. Der  _lpInterface-Parameter_ muss **null** oder IID_IMessage sein. 
    
 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht, die im Formular angezeigt werden soll.
    
 _lpulMessageToken_
  
> [out] Ein Zeiger auf ein Nachrichtentoken, das von der **IMAPISession::ShowForm** -Methode verwendet wird, um auf die Nachricht zuzugreifen, auf die von  _lpMessage_ verwiesen wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Formularvorbereitung war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::P repareForm-Methode** erstellt ein Nachrichtentoken für die Nachricht, auf die der  _parameter lpMessage_ verweist, und ruft die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) der Nachricht auf. Dieses Token wird im  _ulMessageToken-Parameter_ an **IMAPISession::ShowForm** übergeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Aufruf von **PrepareForm** erfolgreich ist, geben Sie die Nachricht los, auf die  _lpMessage_ verweist, indem Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufrufen, bevor Sie **ShowForm** aufrufen. Wenn die Nachricht nicht freigegeben wird, bevor Sie **ShowForm aufrufen,** kann dies zu Speicherverlusten führen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI verwendet die **IMAPISession::P repareForm-Methode** zusammen mit **IMAPISession::ShowForm,** um eine Nachricht in einem modalen Formular anzuzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

