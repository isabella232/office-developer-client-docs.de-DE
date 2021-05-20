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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428592"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Dialogfeld an, in dem der Benutzer einen Formularcontainer auswählen kann, und gibt eine Schnittstelle für das vom Benutzer ausgewählte Containerobjekt zurück.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des angezeigten Dialogfelds. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Formularbibliothek ausgewählt wird (d. h. wie der Formularcontainer ausgewählt wird). Die folgenden Kennzeichen können festgelegt werden:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Die Auswahl kann aus allen Containern vorgenommen werden. Dies ist der Standardauswahltyp. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Die Auswahl kann nur in Ordnercontainern vorgenommen werden.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Die Auswahl kann nur aus Containern vorgenommen werden, die ordnern nicht zugeordnet sind.
    
 _lppfcnt_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle. Diese Schnittstelle ist für das Containerobjekt, das vom Benutzer ausgewählt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularanzeigen rufen in der Regel die **IMAPIFormMgr::SelectFormContainer-Methode** auf, um einen Formularcontainer auszuwählen, in dem ein Formular installiert ist. **SelectFormContainer** kann nicht zum Auswählen des lokalen Formularcontainers verwendet werden, der den Wert HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI verwendet die **IMAPIFormMgr::SelectFormContainer-Methode,** um einen Formularcontainer auszuwählen, bevor der Inhalt gerendert wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

