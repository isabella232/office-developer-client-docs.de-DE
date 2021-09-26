---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d553a4a3ee99ab71206385134fde52da215c535
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610538"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt ein Dialogfeld dar, in dem der Benutzer ein Formular auswählen kann, und gibt ein Formularinformationsobjekt zurück, das dieses Formular beschreibt.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster des angezeigten Dialogfelds. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _pszTitle_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die die Beschriftung des Dialogfelds enthält. Wenn der  _Parameter pszTitle_ NULL ist, stellt der Formularbibliotheksanbieter eine Standardbeschriftung bereit. 
    
 _pfld_
  
> [in] Ein Zeiger auf den Ordner, aus dem das Formular ausgewählt werden soll. Wenn der  _Pfld-Parameter_ NULL ist, kann das Formular aus dem lokalen, persönlichen oder Organisationsformularcontainer ausgewählt werden. 
    
 _ppfrminfoReturned_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formularinformationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormMgr::SelectForm-Methode** auf, um zunächst ein Dialogfeld anzuzeigen, in dem der Benutzer ein Formular auswählen und dann ein Formularinformationsobjekt abrufen kann, das das ausgewählte Formular beschreibt. Das Dialogfeld schränkt den Benutzer ein, um ein einzelnes Formular auszuwählen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im Dialogfeld **Formular** auswählen werden nur Formulare angezeigt, die nicht ausgeblendet sind (d. b. Formulare, deren ausgeblendete Eigenschaften deaktiviert sind). Wenn ein Formularviewer das MAPI_UNICODE Flag im  _ulFlags-Parameter_ übergibt, sind alle Zeichenfolgen Unicode. Formularbibliotheksanbieter, die unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI verwendet die **IMAPIFormMgr::SelectForm-Methode,** um ein Formular auszuwählen und Informationen zum Formular an mindestens ein Protokoll zu senden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

