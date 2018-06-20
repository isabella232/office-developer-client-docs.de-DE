---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 096437f10c5b992a1db55f6a856c38021a81b99a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792206"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Betrifft**: Outlook 
  
Zeigt ein Dialogfeld, mit dem den Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formular Informationsobjekten, die diesen Formularen zu beschreiben.
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster im angezeigten Dialogfeld. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _pszTitle_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die Beschriftung des Dialogfelds enthält. Wenn der Parameter _PszTitle_ NULL ist, stellt der Formular-Bibliotheksanbieter, der die Formulare enthält einen Standardtitel. 
    
 _pfld_
  
> [in] Ein Zeiger auf den Ordner aus, wählen Sie die Formulare. Wenn der Parameter _Pfld_ NULL ist, werden die Formulare aus dem lokalen persönlich oder Organisation Formular Container ausgewählt. 
    
 _pfrminfoarray_
  
> [in] Ein Zeiger auf ein Array von Formular Informationen-Objekten, die für den Benutzer bereits ausgewählt sind.
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Array von Formular Informationen-Objekte.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormMgr::SelectMultipleForms** -Methode zum ersten vorhanden ein Dialogfeld, mit dem den Benutzer mehrere Formulare auswählen kann, und klicken Sie dann Informationen zum Abrufen eines Arrays des Formulars Objekte, die die ausgewählten Formulare beschreiben. Das Dialogfeld **SelectMultipleForms** zeigt alle Formulare, unabhängig davon, ob sie ausgeblendet werden (d. h., ob ihre ausgeblendeten Eigenschaften deaktiviert sind). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formular Viewer die Option MAPI_UNICODE im Parameter _UlFlags_ übergibt, werden alle Zeichenfolgen Unicode. Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

