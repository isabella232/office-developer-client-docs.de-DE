---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 938eaa6c1a39d24157d5d690c42b435af6192cb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417105"
---
# <a name="imapimessagesitesavemessage"></a>IMAPIMessageSite::SaveMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert, dass die aktuelle Nachricht gespeichert wird.
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a>Parameter

Keine.
  
## <a name="return-value"></a>Return value

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
## <a name="remarks"></a>Bemerkungen

Formulare rufen die **IMAPIMessageSite:: SaveMessage** -Methode auf, um das Speichern einer Nachricht anzufordern. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: SaveMessage  <br/> |MFCMAPI verwendet die **IMAPIMessageSite:: SaveMessage** -Methode, um die Nachricht zu speichern.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

