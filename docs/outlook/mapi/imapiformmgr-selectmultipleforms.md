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
  
Stellt ein Dialogfeld vor, in dem der Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formularinformationsobjekten zurück, die diese Formulare beschreiben.
  
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
  
> [in] Ein Handle zum übergeordneten Fenster des angezeigten Dialogfelds. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _pszTitle_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die die Beschriftung des Dialogfelds enthält. Wenn der  _pszTitle-Parameter_ NULL ist, stellt der Formularbibliotheksanbieter, der die Formulare zur Verfügung stellt, eine Standardbeschriftung zur Verfügung. 
    
 _pfld_
  
> [in] Ein Zeiger auf den Ordner, aus dem die Formulare ausgewählt werden. Wenn der  _pfld-Parameter_ NULL ist, werden die Formulare aus dem lokalen, persönlichen oder Organisationsformularcontainer ausgewählt. 
    
 _pfrminfoarray_
  
> [in] Ein Zeiger auf ein Array von Formularinformationsobjekten, die für den Benutzer vorab ausgewählt sind.
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Array von Formularinformationsobjekten.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen im Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::SelectMultipleForms-Methode** auf, um zunächst ein Dialogfeld anzuzeigen, in dem der Benutzer mehrere Formulare auswählen und dann ein Array von Formularinformationsobjekten abrufen kann, die die ausgewählten Formulare beschreiben. Im **Dialogfeld SelectMultipleForms** werden alle Formulare angezeigt, unabhängig davon, ob sie ausgeblendet sind (d. h., ob ihre ausgeblendeten Eigenschaften klar sind oder nicht). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formularanzeiger das MAPI_UNICODE im  _ulFlags-Parameter_ übergibt, sind alle Zeichenfolgen Unicode. Formularbibliotheksanbieter, die keine Unicode-Zeichenfolgen unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, MAPI_UNICODE übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

