---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a62c3edce79349e748620d82e7b18d482dfdb187
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625280"
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
  
> [in] Der Zeiger auf ein Formular empfiehlt ein Senkenobjekt oder NULL.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung oder Stornierung für die Formularbenachrichtigung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewContext::SetAdviseSink-Methode** auf, um sich über Änderungen in der Formularanzeige zu informieren oder eine vorherige Registrierung abzubrechen. Wenn  _pmvns_ auf NULL festgelegt ist, möchte das Formular eine Registrierung abbrechen. Wenn  _pmvns_ auf eine gültige Formular-Empfehlungssenke zeigt, möchte das Formular für zukünftige Benachrichtigungen registriert werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn **SetAdviseSink** einen Formularberater-Senkenzeiger enthält, behalten Sie einen Verweis darauf bei, bis ein weiterer **SetAdviseSink-Aufruf** ausgeführt wird, um die Benachrichtigung abzubrechen. Senden Sie eine Benachrichtigung, wenn eine Änderung in Ihrem Viewer auftritt und Wenn Sie eine neue Nachricht laden. 
  
Weitere Informationen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen.](sending-and-receiving-form-notifications.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implementiert die **IMAPIViewContext::SetAdviseSink-Methode** in dieser Funktion.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

