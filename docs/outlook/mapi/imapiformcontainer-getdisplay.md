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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0f9826dab72968055604c5bb9f8f537facc5618e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792160"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**Betrifft**: Outlook 
  
Gibt den Anzeigenamen eines Containers Formular zurück.
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der zurückgegebenen Zeichenfolge steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die zurückgegebene Zeichenfolge wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, wird die Zeichenfolge im ANSI-Format.
    
 _pszDisplayName_
  
> [out] Ein Zeiger auf eine Zeichenfolge, die den Anzeigenamen des Containers Formular enthält.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::CFormContainerDlg  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormContainer::GetDisplay** -Methode, um den Namen des Containers Formular abrufen, wenn CFormContainerDlg gerendert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

