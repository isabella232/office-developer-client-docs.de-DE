---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430567"
---
# <a name="imapimessagesitegetfolder"></a>IMAPIMessageSite::GetFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Ordner zurück, in dem die aktuelle Nachricht erstellt oder geöffnet wurde, wenn ein solcher Ordner vorhanden ist. Diese Methode gibt NULL im _ppFolder_ -Parameter für eingebettete Nachrichten zurück, die nicht direkt in einem Ordner gespeichert werden. 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a>Parameter

 _ppFolder_
  
> Out Ein Zeiger auf einen Zeiger auf den zurückgegebenen Ordner.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
S_FALSE 
  
> Für die Nachricht ist kein Ordner vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: getFolder  <br/> |MFCMAPI verwendet die **IMAPIMessageSite:: GetFolder** -Methode, um den aktuell zwischengespeicherten Zeiger auf den angegebenen Ordner zurückzugeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

