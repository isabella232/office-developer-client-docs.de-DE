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
ms.openlocfilehash: b481eaf00b7568da5f02ffa3301e8f2698a98e1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792190"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Betrifft**: Outlook 
  
Zeigt ein Dialogfeld, mit dem den Benutzer ein Formular auswählen an und gibt ein Form-Informationen-Objekt, das dieses Formular beschreibt.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster im angezeigten Dialogfeld. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _pszTitle_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die Beschriftung des Dialogfelds enthält. Wenn der Parameter _PszTitle_ NULL ist, stellt der Form Library Anbieter einen Standardtitel. 
    
 _pfld_
  
> [in] Ein Zeiger auf den Ordner aus der das Formular auswählen. Wenn der Parameter _Pfld_ NULL ist, kann das Formular aus dem lokalen persönlich oder Organisation Formular Container ausgewählt werden. 
    
 _ppfrminfoReturned_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Informationen Formularobjekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormMgr::SelectForm** -Methode zum ersten Gegenwart ein Dialogfeld, mit dem den Benutzer ein Formular auswählen, und klicken Sie dann zum Abrufen eines Formulars Informationen-Objekts, die das ausgewählte Formular beschreibt. Das Dialogfeld schränkt des Benutzers ein einzelnes Formular auswählen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das Dialogfeld **SelectForm** zeigt nur für Formulare, die nicht ausgeblendet werden (d. h., deaktivieren Sie Formulare, die ihre ausgeblendeten Eigenschaften haben). Wenn ein Formular Viewer die Option MAPI_UNICODE im Parameter _UlFlags_ übergibt, werden alle Zeichenfolgen Unicode. Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI (engl.) wird die **IMAPIFormMgr::SelectForm** -Methode verwendet, um ein Formular auswählen und die Informationen zum Formular an einen oder mehrere Protokolle senden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

