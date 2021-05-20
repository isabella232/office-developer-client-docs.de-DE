---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435831"
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

 _hResult_
  
> [in] Ein Handle für den Fehlercode, der im vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Format für den in der **MAPIERROR-Struktur** zurückgegebenen Text angibt, auf den _lppMAPIError zeigt._ Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen sollten im Unicode-Format vorliegen. Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format vorliegen.
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine Fehlerinformationen zurückgegeben werden sollen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Fehlerinformationen wurden zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::GetLastError-Methode** stellt Informationen zu einem vorherigen Methodenaufruf zur Verfügung, der fehlgeschlagen ist. Clients können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld eingeben. 
  
Alle von MAPI bereitgestellten Implementierungen von **GetLastError** sind ANSI-Implementierungen, mit Ausnahme der [IAddrBook-Implementierung.](iaddrbookimapiprop.md) Die **getLastError-Methode,** die in **IAddrBook enthalten** ist, unterstützt Unicode. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Details der Implementierung dieser Methode durch einen Remote-Transport-Anbieter und die von dieser Methode zurückgegebenen Nachrichten liegen beim Transportanbieter, da die besonderen Fehlerbedingungen, die zu verschiedenen HRESULT-Werten führen, für unterschiedliche Transportanbieter unterschiedlich sind.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur** verwenden, auf die der  _lppMAPIError-Parameter_ verweist, wenn **GetLastError** einen Parameter anriert, nur wenn der Rückgabewert S_OK. Manchmal **kann GetLastError** nicht bestimmen, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden. In diesem Fall wird stattdessen ein Zeiger auf NULL in  _lppMAPIError_ zurückgegeben. 
  
Um den Arbeitsspeicher für die **MAPIERROR-Struktur frei** zu geben, rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf. 
  
Weitere Informationen zur **GetLastError-Methode** finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[ERWEITERTE MAPI-Fehler](mapi-extended-errors.md)

