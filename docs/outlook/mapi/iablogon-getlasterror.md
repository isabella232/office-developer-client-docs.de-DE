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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434249"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Adressbuchanbieterfehler enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein Handle zum Fehlerwert, der im vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn der Anbieter keine **MAPIERROR-Struktur** mit entsprechenden Informationen angeben kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Adressbuchanbieter implementieren die **GetLastError-Methode,** um Informationen zu einem vorherigen Methodenaufruf zu liefern, der fehlgeschlagen ist. Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld eingeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur verwenden,** auf die der  _lppMAPIError-Parameter_ verweist, wenn der Adressbuchanbieter die Struktur angibt und nur, wenn **GetLastError** S_OK. Manchmal kann der Adressbuchanbieter nicht ermitteln, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden. In diesem Fall gibt der Adressbuchanbieter stattdessen einen Zeiger auf NULL in  _lppMAPIError_ zurück. 
  
Weitere Informationen zur **GetLastError-Methode** finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

