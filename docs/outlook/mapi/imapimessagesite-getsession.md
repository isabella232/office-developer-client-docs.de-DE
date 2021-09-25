---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24cd1c4326c31fd694d8f1e16aba1fe508cf0a24
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630733"
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
    
## <a name="remarks"></a>Bemerkungen

Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI-Formularschnittstellen.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI verwendet die **IMAPIMessageSite::GetSession-Methode,** um den aktuell zwischengespeicherten Sitzungszeiger zurückzugeben, sofern verfügbar.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

