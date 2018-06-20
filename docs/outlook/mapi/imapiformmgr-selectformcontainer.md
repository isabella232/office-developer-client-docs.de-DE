---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ef9b99f06b62fd361bb780debb527ec2d7457589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792214"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Betrifft**: Outlook 
  
Zeigt ein Dialogfeld an, die ermöglicht dem Benutzer das Formular Container auswählen, und gibt eine Schnittstelle für das Containerobjekt der ausgewählten Benutzer an.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster im angezeigten Dialogfeld. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Formularbibliothek aktiviert ist (d. h., wie der Formular Container ausgewählt ist). Die folgenden Kennzeichen können festgelegt werden:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Auswahl kann von allen Containern vorgenommen werden. Dies ist der Standard-Auswahltyp. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Auswahl kann nur von Ordner Containern vorgenommen werden.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Auswahl kann nur aus den Containern vorgenommen werden, die keine Ordner zugeordnet sind.
    
 _lppfcnt_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle. Diese Schnittstelle ist für das Containerobjekt, das vom Benutzer ausgewählt ist.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formular Viewer aufrufen in der Regel die **IMAPIFormMgr::SelectFormContainer** -Methode, um ein Formular Container auszuwählen, in dem einem Formular installiert ist. **SelectFormContainer** kann nicht aus dem Container lokale Formular mit dem Wert HFRMREG_LOCAL verwendet werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormMgr::SelectFormContainer** -Methode, um ein Formular Container wählen Sie vor dem Rendern seinen Inhalt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

