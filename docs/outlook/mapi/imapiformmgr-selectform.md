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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321672"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Dialogfeld an, in dem der Benutzer ein Formular auswählen und ein Formular Informationsobjekt zurückgibt, das dieses Formular beschreibt.
  
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
  
> in Ein Handle für das übergeordnete Fenster des angezeigten Dialogfelds. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _pszTitle_
  
> in Ein Zeiger auf eine Zeichenfolge, die die Beschriftung des Dialogfelds enthält. Wenn der _pszTitle_ -Parameter NULL ist, stellt der Formularbibliothek Anbieter eine Standardbeschriftung bereit. 
    
 _pfld_
  
> in Ein Zeiger auf den Ordner, aus dem das Formular ausgewählt werden soll. Wenn der _pfld_ -Parameter NULL ist, kann das Formular aus dem Container für lokale, persönliche oder organisatorische Formulare ausgewählt werden. 
    
 _ppfrminfoReturned_
  
> Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular Informationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in der Regel auf die Schaltfläche **Abbrechen** im Dialogfeld geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr:: SelectForm** -Methode auf, um zuerst ein Dialogfeld darzustellen, das es dem Benutzer ermöglicht, ein Formular auszuwählen und dann ein Formular Informationsobjekt abzurufen, das das ausgewählte Formular beschreibt. Das Dialogfeld schränkt den Benutzer ein, um ein einzelnes Formular auszuwählen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Im Dialogfeld **SelectForm** werden nur Formulare angezeigt, die nicht ausgeblendet sind (also Formulare, deren ausgeblendete Eigenschaften deaktiviert sind). Wenn ein Formular Betrachter das MAPI_UNICODE-Flag im _ulFlags_ -Parameter übergibt, sind alle Zeichenfolgen Unicode. Formularbibliothek Anbieter, die Unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSelectForm  <br/> |MFCMAPI verwendet die **IMAPIFormMgr:: SelectForm** -Methode, um ein Formular auszuwählen und Informationen zum Formular an ein oder mehrere Protokolle zu senden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

