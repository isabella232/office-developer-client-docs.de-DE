---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9456f834ea606106b313949dfff863534bac2509
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556602"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _Hresult_
  
> [in] Ein Handle für den Fehlercode, der im vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Format für den Text angibt, der in der **MAPIERROR-Struktur** zurückgegeben wird, auf den durch  _lppMAPIError_ verwiesen wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen sollten im Unicode-Format vorliegen. Wenn das flag MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format vorliegen.
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine Fehlerinformationen zurückgegeben werden müssen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Fehlerinformationen wurden zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIProp::GetLastError-Methode** stellt Informationen zu einem vorherigen Methodenaufruf bereit, bei dem ein Fehler aufgetreten ist. Clients können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld einschließen. 
  
Alle von mapi bereitgestellten Implementierungen von **GetLastError** sind ANSI-Implementierungen, mit Ausnahme der [IAddrBook-Implementierung.](iaddrbookimapiprop.md) Die in **IAddrBook enthaltene** **GetLastError-Methode** unterstützt Unicode. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Details der Implementierung dieser Methode durch einen Remote-Transportanbieter und die von dieser Methode zurückgegebenen Meldungen liegen beim Transportanbieter, da die speziellen Fehlerbedingungen, die zu verschiedenen HRESULT-Werten führen, für verschiedene Transportanbieter unterschiedlich sind.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur** verwenden, auf die durch den  _lppMAPIError-Parameter_ verwiesen wird, wenn **GetLastError** eine bereitstellt, nur, wenn der Rückgabewert S_OK ist. Manchmal kann **GetLastError** nicht ermitteln, was der letzte Fehler war, oder über den Fehler kann nichts mehr gemeldet werden. In diesem Fall wird stattdessen ein Zeiger auf NULL in  _lppMAPIError_ zurückgegeben. 
  
Rufen Sie die [MAPIFreeBuffer-Funktion auf,](mapifreebuffer.md) um den Speicher für die **MAPIERROR-Struktur** freizugeben. 
  
Weitere Informationen zur **GetLastError** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI Extended Errors](mapi-extended-errors.md)

