---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423580"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Dialogfeld an, in dem der Benutzer ein Formular auswählen kann, und gibt ein Formularinformationsobjekt zurück, das dieses Formular beschreibt.
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
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
  
> [in] Ein Zeiger auf eine Zeichenfolge, die die Beschriftung des Dialogfelds enthält. Wenn der  _pszTitle-Parameter_ NULL ist, stellt der Formularbibliotheksanbieter eine Standardbeschriftung zur Verfügung. 
    
 _pfld_
  
> [in] Ein Zeiger auf den Ordner, aus dem das Formular ausgewählt werden soll. Wenn der  _pfld-Parameter_ NULL ist, kann das Formular aus dem lokalen, persönlichen oder Organisationsformularcontainer ausgewählt werden. 
    
 _ppfrminfoReturned_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formularinformationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen im Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::SelectForm-Methode** auf, um zunächst ein Dialogfeld anzuzeigen, in dem der Benutzer ein Formular auswählen und dann ein Formularinformationsobjekt abrufen kann, das das ausgewählte Formular beschreibt. Das Dialogfeld schränkt den Benutzer ein, ein einzelnes Formular auszuwählen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im **Dialogfeld SelectForm** werden nur Formulare angezeigt, die nicht ausgeblendet sind (d. h. Formulare, deren ausgeblendete Eigenschaften klar sind). Wenn ein Formularanzeiger das MAPI_UNICODE im  _ulFlags-Parameter_ übergibt, sind alle Zeichenfolgen Unicode. Formularbibliotheksanbieter, die keine Unicode-Zeichenfolgen unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, MAPI_UNICODE übergeben wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI verwendet die **IMAPIFormMgr::SelectForm-Methode,** um ein Formular auszuwählen und Informationen über das Formular an ein oder mehrere Protokolle zu senden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

