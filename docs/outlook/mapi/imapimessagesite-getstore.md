---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792219"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**Betrifft**: Outlook 
  
Gibt den Nachrichtenspeicher, der die aktuelle Nachricht enthält zurück, wenn eine solche ein Speicher vorhanden ist. Diese Methode gibt NULL im Parameter _PpStore_ für eingebettete Nachrichten zurück, die in eine andere Nachricht anstatt direkt in einem Nachrichtenspeicher gespeichert werden. 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>Parameter

 _ppStore_
  
> [out] Ein Zeiger auf einen Zeiger auf den Nachrichtenspeicher.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
S_FALSE 
  
> Es ist kein Speicher, die die Nachricht enthält.
    
## <a name="remarks"></a>Hinweise

Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |MFCMAPI (engl.) verwendet die **IMAPIMessageSite::GetStore** -Methode den aktuell zwischengespeicherten Zeiger auf den angegebenen Speicher, abgerufen, sofern es vorhanden ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formulars Schnittstellen](mapi-form-interfaces.md)

