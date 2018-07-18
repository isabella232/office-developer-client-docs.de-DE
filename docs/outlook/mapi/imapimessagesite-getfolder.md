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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea95ea4efbbf50e5551a27eb81fe5d5ab3b73948
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792202"
---
# <a name="imapimessagesitegetfolder"></a>IMAPIMessageSite::GetFolder

  
  
**Betrifft**: Outlook 
  
Der Ordner, in dem die aktuelle Nachricht geöffnet oder erstellt wurde, zurückgegeben, wenn solche ein Ordner vorhanden ist. Diese Methode gibt NULL zurück, in der _PpFolder_ -Parameter für eingebettete Nachrichten, die nicht direkt in einem Ordner gespeichert werden. 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a>Parameter

 _ppFolder_
  
> [out] Ein Zeiger auf einen Zeiger auf den zurückgegebenen Ordner.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
S_FALSE 
  
> Kein Ordner für die Nachricht vorhanden ist.
    
## <a name="remarks"></a>Bemerkungen

Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern, finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetFolder  <br/> |MFCMAPI (engl.) wird die **IMAPIMessageSite::GetFolder** -Methode verwendet, um die aktuell zwischengespeicherten Zeiger auf den angegebenen Ordner zurückzugeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

