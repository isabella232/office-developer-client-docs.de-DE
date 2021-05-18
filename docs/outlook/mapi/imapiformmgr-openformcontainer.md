---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321637"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine [IMAPIFormContainer-Schnittstelle](imapiformcontaineriunknown.md) für einen bestimmten Formularcontainer. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameter

 _hfrmreg_
  
> [in] Eine HFRMREG-Aufzählung, die die zu öffnende Formularbibliothek angibt (d. h. den zu öffnenden Formularcontainer). Eine HFRMREG-Enumeration ist eine Enumeration, die für einen Formularbibliotheksanbieter spezifisch ist. Mögliche HFRMREG-Werte sind:
    
HFRMREG_DEFAULT 
  
> Ein praktischer Formularcontainer.
    
HFRMREG_FOLDER 
  
> Ein Ordnercontainer. 
    
HFRMREG_PERSONAL 
  
> Der Container für den Standardnachrichtenspeicher. 
    
HFRMREG_LOCAL 
  
> Ein lokaler Formularcontainer. 
    
 _lpunk_
  
> [in] Ein Zeiger auf das Objekt, für das die Schnittstelle geöffnet wird. Der  _lpunk-Parameter_ muss **null sein,** es sei denn, der Wert für den  _parameter hfrmreg_ erfordert einen Objektzeiger. 
    
 _lppfcnt_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formularcontainerobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Das von  _lpunk_ angezeigte Objekt unterstützt die erforderliche Schnittstelle nicht. 
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::OpenFormContainer-Methode** auf, um eine **IMAPIFormContainer-Schnittstelle** für einen bestimmten Formularcontainer zu öffnen. Diese Schnittstelle kann dann zum Installieren von Formularen in einem Formularcontainer und zum Entfernen von Formularen aus einem Formularcontainer verwendet werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Wert in _hfrmreg_ HFRMREG_FOLDER ist, muss der in _lpunk_ verwendete Schnittstellenbezeichner nicht null sein und [IUnknown::QueryInterface-Methodenaufrufe](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) an eine  [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) zulassen. 
  
Zum Öffnen des lokalen Formularcontainers müssen Sie einen Aufruf der **OpenFormContainer-Methode** oder der [MAPIOpenLocalFormContainer-Funktion](mapiopenlocalformcontainer.md) verwenden. Sie können die [IMAPIFormMgr::SelectFormContainer-Methode](imapiformmgr-selectformcontainer.md) nicht verwenden, um dem Benutzer die Auswahl des lokalen Formularcontainers zu ermöglichen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI verwendet die **IMAPIFormMgr::OpenFormContainer-Methode,** um einen Formularcontainer abzurufen, damit der Inhalt des Containers gerendert werden kann.  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI verwendet die **IMAPIFormMgr::OpenFormContainer-Methode,** um einen Formularcontainer für einen Ordner abzurufen, damit der Inhalt des Containers gerendert werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

