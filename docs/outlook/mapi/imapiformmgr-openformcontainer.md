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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321637"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine [IMAPIFormContainer](imapiformcontaineriunknown.md) -Schnittstelle für einen bestimmten Formular Container. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameter

 _hfrmreg_
  
> in Eine HFRMREG-Aufzählung, die die zu öffnende Formularbibliothek angibt (also den zu öffnenden Formular Container). Eine HFRMREG-Aufzählung ist eine für einen Formular Bibliotheks anbieterspezifische Enumeration. Zu den möglichen HFRMREG-Werten gehört Folgendes:
    
HFRMREG_DEFAULT 
  
> Ein bequemer Formular Container.
    
HFRMREG_FOLDER 
  
> Ein Ordner Container. 
    
HFRMREG_PERSONAL 
  
> Der Container für den Standardnachrichtenspeicher. 
    
HFRMREG_LOCAL 
  
> Ein lokaler Formular Container. 
    
 _lpUnk_
  
> in Ein Zeiger auf das Objekt, für das die Schnittstelle geöffnet wird. Der _lpUnk_ -Parameter muss **null** sein, es sei denn, der Wert für den _hfrmreg_ -Parameter erfordert einen Objektzeiger. 
    
 _lppfcnt_
  
> Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular Container-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Das Objekt, auf das durch _lpUnk_ verwiesen wird, unterstützt die erforderliche Schnittstelle nicht. 
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr:: OpenFormContainer** -Methode auf, um eine **IMAPIFormContainer** -Schnittstelle für einen bestimmten Formular Container zu öffnen. Diese Schnittstelle kann dann verwendet werden, um Formulare zu installieren und Formulare aus einem Formular Container zu entfernen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Wert in _HFRMREG_ HFRMREG_FOLDER ist, muss der in _lpUnk_ verwendete Schnittstellenbezeichner ungleich **null** sein und [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methodenaufrufe an eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle zulassen. 
  
Zum Öffnen des lokalen Formular Containers müssen Sie einen Aufruf der **OpenFormContainer** -Methode oder der [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) -Funktion verwenden. Sie können die [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) -Methode nicht verwenden, um dem Benutzer das Auswählen des lokalen Formular Containers zu ermöglichen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenFormContainer  <br/> |MFCMAPI verwendet die **IMAPIFormMgr:: OpenFormContainer** -Methode, um einen Formular Container abzurufen, damit der Inhalt des Containers gerendert werden kann.  <br/> |
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnOpenFormContainer  <br/> |MFCMAPI verwendet die **IMAPIFormMgr:: OpenFormContainer** -Methode, um einen Formular Container für einen Ordner abzurufen, damit der Inhalt des Containers gerendert werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

