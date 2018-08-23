---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5e3a2224daace9be7f4504a693806ccb3cf4abbe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570492"
---
# <a name="imapimessagesitegetformmanager"></a>IMAPIMessageSite::GetFormManager

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt eine Formular-Manager-Schnittstelle, die ein Formular Server verwenden kann, um ein anderes Formular Server zu öffnen.
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a>Parameter

 _ppFormMgr_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular-Manager-Schnittstelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetFormManager  <br/> |MFCMAPI (engl.) wird die **IMAPIMessageSite::GetFormManager** -Methode verwendet, um [MAPIOpenFormMgr](mapiopenformmgr.md) aufrufen und die Ergebnisse des Aufrufs, dass zurückzugeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIOpenFormMgr](mapiopenformmgr.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

