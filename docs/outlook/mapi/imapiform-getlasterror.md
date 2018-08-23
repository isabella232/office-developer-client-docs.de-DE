---
title: IMAPIFormGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetLastError
api_type:
- COM
ms.assetid: 81af8a0b-4ec2-459c-8ab2-29d28a8b680f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a83af0766c907f2868f7d5e116454e648d6f4463
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583771"
---
# <a name="imapiformgetlasterror"></a>IMAPIForm::GetLastError

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu den vorherigen von das Formularobjekt generierten Fehler enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden: 
    
PARAMETER MAPI_UNICODE 
  
> Wenn Unicode-Format festgelegt, die Zeichenfolgen in der **MAPIERROR** -Struktur, die im Parameter _LppMAPIError_ zurückgegeben werden. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. Dieser Parameter kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und **GetLastError** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **GetLastError** nur Unicode unterstützt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIForm::GetLastError** -Methode stellt Informationen zu einem Aufruf der vorherigen-Methode, die nicht zur Verfügung. Anrufer können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR** -Struktur, die auf das durch den Parameter _LppMAPIError_ Wenn MAPI bereitstellt, nur wenn **GetLastError** gibt S_OK zurück. In einigen Fällen kann nicht MAPI was letzten Fehler erkennen, oder es wurde keine weiteren zu dem Fehler melden. In diesem Fall wird ein Zeiger auf NULL stattdessen in _LppMAPIError_ zurückgegeben. 
  
Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Erweiterte Fehler verwenden](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

