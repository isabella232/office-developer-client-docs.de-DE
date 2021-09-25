---
title: IMsgServiceAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.GetLastError
api_type:
- COM
ms.assetid: 9e3c8d6e-74be-46a7-94ed-74a969caf165
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3189e5adedbcc04693b911315f0569916bba6321
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575631"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum letzten Fehler enthält, der für ein Nachrichtendienst-Verwaltungsobjekt aufgetreten ist. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _Hresult_
  
> [in] Ein HRESULT-Datentyp, der den Fehlerwert enthält, der durch den vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _Parameter lppMAPIError_ zurückgegeben werden, weisen das Unicode-Format auf. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Das MAPI_UNICODE Flag wurde festgelegt, und das Nachrichtendienst-Verwaltungsobjekt unterstützt unicode nicht.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::GetLastError-Methode** ruft Informationen zu dem letzten Fehler ab, der von einem [IMsgServiceAdmin-Methodenaufruf](imsgserviceadminiunknown.md) zurückgegeben wurde. Clients können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie diese Informationen in ein Dialogfeld einschließen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur** nur dann verwenden, wenn MAPI eine bereitstellt, auf die durch den  _Parameter lppMAPIError_ verwiesen wird, wenn **GetLastError** S_OK zurückgibt. Manchmal kann die MAPI nicht ermitteln, was der letzte Fehler war, oder sie kann nichts mehr über den Fehler melden. In diesem Fall gibt **GetLastError** stattdessen einen Zeiger auf NULL in  _lppMAPIError_ zurück. 
  
Weitere Informationen zur **GetLastError** -Methode finden Sie unter [Verwenden erweiterter Fehler.](mapi-extended-errors.md)
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

