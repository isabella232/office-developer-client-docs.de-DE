---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ab4aab0fe555445b56e2c42fbe7bc00505e44b36
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596344"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum Fehler des vorherigen Schaltflächensteuerelements enthält. 
  
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
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Dienstanbieter implementieren die **IMAPIControl::GetLastError-Methode,** um Informationen zu einem vorherigen Methodenaufruf zu liefern, bei dem ein Fehler aufgetreten ist. MAPI kann Benutzern detaillierte Informationen zu dem Fehler liefern, indem die Daten aus der **MAPIERROR-Struktur** in einer Nachricht oder einem Dialogfeld angezeigt werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht über Informationen verfügen, die in die **MAPIERROR-Struktur** für jeden Fehler eingeschlossen werden müssen. Es ist möglicherweise nicht möglich, den vorherigen Fehler zu ermitteln. Wenn Sie über Informationen verfügen, geben Sie S_OK und die entsprechenden Daten in der **MAPIERROR-Struktur** zurück. Wenn keine Informationen verfügbar sind, geben Sie S_OK und einen Zeiger auf NULL für den  _Parameter lppMAPIError_ zurück. 
  
Weitere Informationen zur **GetLastError** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

