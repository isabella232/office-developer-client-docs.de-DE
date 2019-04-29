---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416132"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Anzeigenamen eines Formular Containers zurück.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolge steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebene Zeichenfolge ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, wird die Zeichenfolge im ANSI-Format.
    
 _pszDisplayName_
  
> Out Ein Zeiger auf eine Zeichenfolge, die den Anzeigenamen des Formular Containers enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: CFormContainerDlg  <br/> |MFCMAPI verwendet die **IMAPIFormContainer:: getdisplay** -Methode, um den Namen des Formular Containers abzurufen, wenn er CFormContainerDlg rendert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

