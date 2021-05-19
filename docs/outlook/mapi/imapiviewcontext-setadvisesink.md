---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419394"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet die Registrierung eines Formulars, um Benachrichtigungen über Änderungen im Viewer zu erhalten. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parameter

 _pmvns_
  
> [in] Zeiger auf ein Formular raten sink-Objekt oder NULL.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung oder Der Abbruch der Formularbenachrichtigung war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Form-Objekte rufen die **IMAPIViewContext::SetAdviseSink-Methode** auf, um sich entweder zu registrieren, um mehr über Änderungen in der Formularanzeige zu erfahren, oder um eine vorherige Registrierung abbricht. Wenn  _pmvns_ auf NULL festgelegt ist, möchte das Formular eine Registrierung abbrechen. Wenn  _pmvns_ auf eine gültige Formularsenke verweist, möchte das Formular für zukünftige Benachrichtigungen registriert werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn **SetAdviseSink** einen Formular-Hinweis-Senkenzeiger enthält, behalten Sie einen Verweis darauf bei, bis ein anderer **SetAdviseSink-Aufruf** zum Abbrechen der Benachrichtigung erfolgt ist. Senden Sie eine Benachrichtigung, wenn eine Änderung in Ihrem Viewer auftritt und Wenn Sie eine neue Nachricht laden. 
  
Weitere Informationen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implementiert die **IMAPIViewContext::SetAdviseSink-Methode** in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

