---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c4dba3d43c13ef10063acff87a35f6b52c041e6b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610517"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt ein Dialogfeld dar, in dem der Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formularinformationsobjekten zurück, die diese Formulare beschreiben.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster des angezeigten Dialogfelds. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _pszTitle_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die die Beschriftung des Dialogfelds enthält. Wenn der  _PszTitle-Parameter_ NULL ist, stellt der Formularbibliotheksanbieter, der die Formulare bereitstellt, eine Standardbeschriftung bereit. 
    
 _pfld_
  
> [in] Ein Zeiger auf den Ordner, aus dem die Formulare ausgewählt werden sollen. Wenn der  _Pfld-Parameter_ NULL ist, werden die Formulare aus dem lokalen, persönlichen oder Organisationsformularcontainer ausgewählt. 
    
 _pfrminfoarray_
  
> [in] Ein Zeiger auf ein Array von Formularinformationsobjekten, die für den Benutzer vorab ausgewählt sind.
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Array von Formularinformationsobjekten.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormMgr::SelectMultipleForms-Methode** auf, um zunächst ein Dialogfeld anzuzeigen, in dem der Benutzer mehrere Formulare auswählen und dann ein Array von Formularinformationsobjekten abrufen kann, die die ausgewählten Formulare beschreiben. Im Dialogfeld **SelectMultipleForms** werden alle Formulare angezeigt, unabhängig davon, ob sie ausgeblendet sind (d. b. ob ihre ausgeblendeten Eigenschaften deaktiviert sind). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formularviewer das MAPI_UNICODE Flag im  _ulFlags-Parameter_ übergibt, sind alle Zeichenfolgen Unicode. Formularbibliotheksanbieter, die unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

