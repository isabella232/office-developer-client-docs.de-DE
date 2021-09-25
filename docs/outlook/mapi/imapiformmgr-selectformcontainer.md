---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 91831f40d7adfed25b04a355b665c9582e885392
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567565"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt ein Dialogfeld dar, in dem der Benutzer einen Formularcontainer auswählen kann, und gibt eine Schnittstelle für das vom Benutzer ausgewählte Containerobjekt zurück.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des angezeigten Dialogfelds. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Formularbibliothek ausgewählt wird (d. b. wie der Formularcontainer ausgewählt wird). Die folgenden Flags können festgelegt werden:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Die Auswahl kann aus allen Containern erfolgen. Dies ist der Standardauswahltyp. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Die Auswahl kann nur aus Ordnercontainern getroffen werden.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Die Auswahl kann nur aus Containern getroffen werden, die nicht mit Ordnern verknüpft sind.
    
 _lppfcnt_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle. Diese Schnittstelle ist für das Containerobjekt vorgesehen, das vom Benutzer ausgewählt wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen in der Regel die **IMAPIFormMgr::SelectFormContainer-Methode** auf, um einen Formularcontainer auszuwählen, in dem ein Formular installiert ist. **SelectFormContainer** kann nicht zum Auswählen des lokalen Formularcontainers verwendet werden, der den Wert HFRMREG_LOCAL hat. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI verwendet die **IMAPIFormMgr::SelectFormContainer-Methode,** um einen Formularcontainer auszuwählen, bevor der Inhalt gerendert wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

