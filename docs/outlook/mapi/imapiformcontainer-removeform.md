---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432198"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt ein bestimmtes Formular aus einem Formular Container.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Parameter

 _szMessageClass_
  
> in Eine Zeichenfolge, die die Nachrichtenklasse des Formulars benennt, das aus dem Formular Container entfernt werden soll. Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die Nachrichtenklasse, die im _szMessageClass_ -Parameter übergeben wird, stimmt nicht mit der Nachrichtenklasse eines beliebigen Formulars im Formular Container überein. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMAPIFormContainer:: RemoveForm** -Methode, um ein Formular aus einem Formular Container zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

