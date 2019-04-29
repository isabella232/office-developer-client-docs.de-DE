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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420311"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Dialogfeld an, in dem der Benutzer mehrere Formulare auswählen kann, und es wird ein Array von Formular Informationsobjekten zurückgegeben, die diese Formulare beschreiben.
  
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
  
> in Ein Handle für das übergeordnete Fenster des angezeigten Dialogfelds. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _pszTitle_
  
> in Ein Zeiger auf eine Zeichenfolge, die die Beschriftung des Dialogfelds enthält. Wenn der _pszTitle_ -Parameter NULL ist, liefert der Formularbibliothek Anbieter, der die Formulare bereitstellt, eine Standardbeschriftung. 
    
 _pfld_
  
> in Ein Zeiger auf den Ordner, aus dem die Formulare ausgewählt werden sollen. Wenn der _pfld_ -Parameter NULL ist, werden die Formulare im Formular Container local, Personal oder Organization ausgewählt. 
    
 _pfrminfoarray_
  
> in Ein Zeiger auf ein Array von Formular Informationsobjekten, die für den Benutzer vorgewählt sind.
    
 _ppfrminfoarray_
  
> Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Array von Formular Informationsobjekten.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in der Regel auf die Schaltfläche **Abbrechen** im Dialogfeld geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr:: SelectMultipleForms** -Methode auf, um zuerst ein Dialogfeld zu öffnen, in dem der Benutzer mehrere Formulare auswählen und dann ein Array von Formular Informationsobjekten abrufen kann, die die ausgewählten Formulare beschreiben. Im Dialogfeld **SelectMultipleForms** werden alle Formulare angezeigt, unabhängig davon, ob Sie ausgeblendet sind (d..., ob Ihre ausgeblendeten Eigenschaften deaktiviert sind). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formular Betrachter das MAPI_UNICODE-Flag im _ulFlags_ -Parameter übergibt, sind alle Zeichenfolgen Unicode. Formularbibliothek Anbieter, die Unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

