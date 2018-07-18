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
ms.openlocfilehash: abee768dd29cc807b605a7d13570a579cb271b2c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792496"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Betrifft**: Outlook 
  
Verwaltet ein Formular Registrierung Erhalt von Benachrichtigungen zu Änderungen im Viewer. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parameter

 _pmvns_
  
> [in] Zeiger auf ein Formular advise-Empfängerobjekt oder NULL.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Registrierung oder die Löschung für Formular-Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte Aufrufen die **IMAPIViewContext::SetAdviseSink** -Methode, um entweder Register erfahren Sie mehr über die Änderungen im Formular-Viewer oder Abbrechen einer vorherigen Erfassung. Wenn _Pmvns_ auf NULL festgelegt ist, das Formular eine Registrierung abbrechen möchte. Wenn _Pmvns_ verweist auf ein gültiges Formular-Empfänger Advise, möchte, dass das Formular für zukünftige Benachrichtigungen registriert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn **SetAdviseSink** enthält ein Formular advise-Empfängerzeiger, halten, um einen Verweis auf ein anderes **SetAdviseSink** aufgerufen wird, Benachrichtigung abzubrechen. Senden Sie eine Benachrichtigung bei einer Änderung wird im Viewer und Laden Sie eine neue Nachricht. 
  
Weitere Informationen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI (engl.) implementiert die **IMAPIViewContext::SetAdviseSink** -Methode in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

