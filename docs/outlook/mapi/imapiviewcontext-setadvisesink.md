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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351191"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet die Registrierung eines Formulars, um Benachrichtigungen zu Änderungen im Viewer zu erhalten. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parameter

 _pmvns_
  
> in Zeiger auf ein Formular Advise Sink-Objekt oder NULL.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung oder Stornierung für die Formular Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewContext:: SetAdviseSink** -Methode auf, um sich zu registrieren, um sich über Änderungen im Formular-Viewer zu informieren oder um eine vorherige Registrierung abzubrechen. Wenn _pmvns_ auf NULL festgelegt ist, möchte das Formular eine Registrierung abbrechen. Wenn _pmvns_ auf eine gültige Form Advise-Senke zeigt, möchte das Formular für zukünftige Benachrichtigungen registrieren. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn **SetAdviseSink** einen Form Advise-Senk Zeiger enthält, behalten Sie einen Verweis darauf, bis ein weiterer **SetAdviseSink** -Aufruf zum Abbrechen der Benachrichtigung erfolgt. Senden Sie eine Benachrichtigung, wenn eine Änderung in Ihrem Viewer auftritt und wenn Sie eine neue Nachricht laden. 
  
Weitere Informationen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: SetAdviseSink  <br/> |MFCMAPI implementiert die **IMAPIViewContext:: SetAdviseSink** -Methode in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

