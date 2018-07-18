---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bead72ab2b394634217c9ae219a03a98752ef27d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791958"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**Betrifft**: Outlook 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Address Book Anbieterfehler enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein Handle für den Fehlerwert in der vorherigen Aufruf-Methode generiert.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn der Anbieter eine **MAPIERROR** -Struktur mit den entsprechenden Informationen angegeben werden kann. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Adressbuchanbieter unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und die Adressbuchanbieter unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Von adressbuchanbietern implementierte implementieren die **GetLastError** -Methode, um Informationen zu einem vorherigen Methodenaufruf angeben, die nicht erfolgreich. Anrufer können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR** -Struktur, die auf den der _LppMAPIError_ -Parameter, wenn die Adressbuchanbieter die Struktur bereitstellt und **GetLastError** gibt S_OK zurück. In einigen Fällen kann die Adressbuchanbieter was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde nicht ermitteln. In diesem Fall gibt die Adressbuchanbieter einen Zeiger auf NULL in _LppMAPIError_ stattdessen. 
  
Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

