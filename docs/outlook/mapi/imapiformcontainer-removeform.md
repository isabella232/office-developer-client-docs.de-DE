---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5fc586aba39ac6083e9327c83b13b158cf47ebd6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576016"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt ein bestimmtes Formular aus einem Formularcontainer.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Parameter

 _szMessageClass_
  
> [in] Eine Zeichenfolge, die die Nachrichtenklasse des Formulars benennt, das aus dem Formularcontainer entfernt werden soll. Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, niemals Unicode.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die im Parameter  _"szMessageClass"_ übergebene Nachrichtenklasse stimmt nicht mit der Nachrichtenklasse eines Formulars im Formularcontainer überein. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnDeleteSelectedItem  <br/> |MFCMAPI verwendet die **IMAPIFormContainer::RemoveForm-Methode,** um ein Formular aus einem Formularcontainer zu löschen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

