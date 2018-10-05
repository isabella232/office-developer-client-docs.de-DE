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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393117"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine [IMAPIFormContainer](imapiformcontaineriunknown.md) -Schnittstelle für ein bestimmtes Formular Container. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameter

 _hfrmreg_
  
> [in] Eine HFRMREG-Enumeration, die zum Öffnen die Formularbibliothek angibt (d. h., die Container Formular öffnen). Eine Enumeration HFRMREG ist eine Enumeration, die zu einem Formular Bibliotheksanbieter spezifisch sind. Die folgenden: möglichen Werte für HFRMREG
    
HFRMREG_DEFAULT 
  
> Ein Container komfortable Formular.
    
HFRMREG_FOLDER 
  
> Ein Ordnercontainer. 
    
HFRMREG_PERSONAL 
  
> Der Container für Standard-Informationsspeicher. 
    
HFRMREG_LOCAL 
  
> Ein Container für lokale Formular. 
    
 _lpUnk_
  
> [in] Ein Zeiger auf das Objekt, für das die Schnittstelle geöffnet ist. Der Parameter _Lpunk_ muss **null** sein, es sei denn, der Wert für den Parameter _Hfrmreg_ einen Zeiger erforderlich ist. 
    
 _lppfcnt_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Form Container-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Das Objekt, das auf _Lpunk_ unterstützt nicht die erforderliche Schnittstelle. 
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormMgr::OpenFormContainer** -Methode, um eine **IMAPIFormContainer** -Schnittstelle für ein bestimmtes Formular Container zu öffnen. Diese Schnittstelle kann dann für die Installation in und Entfernen von Formularen aus einem Formular Container verwendet werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Wert in _Hfrmreg_ HFRMREG_FOLDER ist, der Schnittstellenbezeichner in _Lpunk_ verwendet muss ungleich **null** sein und muss [QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode Anrufe an eine Schnittstelle [IMAPIFolder](imapifolderimapicontainer.md) zulassen. 
  
Um den Container lokale Formular zu öffnen, müssen Sie einen Anruf an **OpenFormContainer** -Methode oder die [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) -Funktion verwenden. Sie können nicht die [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) -Methode verwenden, um die Benutzer auswählen den Container lokale Formular aktivieren. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormMgr::OpenFormContainer** -Methode, um ein Formular Container abrufen, damit der Inhalt des Containers gerendert werden können.  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI (engl.) wird die **IMAPIFormMgr::OpenFormContainer** -Methode verwendet, um ein Formular Container für einen Ordner abzurufen, damit der Inhalt des Containers gerendert werden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

