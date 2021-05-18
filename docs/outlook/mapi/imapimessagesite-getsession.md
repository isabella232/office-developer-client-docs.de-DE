---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e1ea68a7690a93915cd80ad5406c4d71d3a97400
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412688"
---
# <a name="imapimessagesitegetsession"></a>IMAPIMessageSite::GetSession

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die MAPI-Sitzung zurück, in der die aktuelle Nachricht erstellt oder geöffnet wurde.
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a>Parameter

 _ppSession_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Sitzungsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
S_FALSE 
  
> Für die aktuelle Nachricht ist keine Sitzung vorhanden.
    
## <a name="remarks"></a>Hinweise

Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI verwendet die **IMAPIMessageSite::GetSession-Methode,** um den aktuell zwischengespeicherten Sitzungszeiger zurückzukehren, sofern er verfügbar ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

