---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1a72a65a1d53329a13eac38364b8af8de73a2c0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571927"
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

 _Hresult_
  
> [in] Ein Handle für den Fehlerwert, der im vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _Parameter lppMAPIError_ zurückgegeben werden, weisen das Unicode-Format auf. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn der Anbieter keine **MAPIERROR-Struktur** mit entsprechenden Informationen bereitstellen kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Kennzeichen festgelegt, und der Adressbuchanbieter unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Adressbuchanbieter implementieren die **GetLastError-Methode,** um Informationen zu einem vorherigen Fehlgeschlagenen Methodenaufruf zu liefern. Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld einschließen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur verwenden,** auf die durch den  _lppMAPIError-Parameter_ verwiesen wird, wenn der Adressbuchanbieter die Struktur bereitstellt und nur, wenn **GetLastError** S_OK zurückgibt. Manchmal kann der Adressbuchanbieter nicht ermitteln, was der letzte Fehler war, oder er kann nichts mehr über den Fehler berichten. In diesem Fall gibt der Adressbuchanbieter stattdessen einen Zeiger auf NULL in  _lppMAPIError_ zurück. 
  
Weitere Informationen zur **GetLastError** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

