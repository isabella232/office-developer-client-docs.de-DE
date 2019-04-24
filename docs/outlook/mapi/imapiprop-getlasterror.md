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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342049"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> in Ein Handle für den im vorherigen Methodenaufruf generierten Fehlercode.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Format für den Text angibt, der in der **MAPIERROR** -Struktur zurückgegeben wird, auf die durch _lppMAPIError_verwiesen wird. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen sollten im Unicode-Format vorliegen. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format sein.
    
 _lppMAPIError_
  
> Out Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Der Parameter _lppMAPIError_ kann auf NULL festgelegt werden, wenn keine Fehlerinformationen zurückgegeben werden sollen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Fehlerinformationen wurden zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp:: getlasterroraufzurufen** -Methode liefert Informationen zu einem vorherigen Methodenaufruf, der fehlgeschlagen ist. Clients können Ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem Sie die Daten aus der **MAPIERROR** -Struktur in ein Dialogfeld einschließen. 
  
Alle von MAPI bereitgestellten Implementierungen von **getlasterroraufzurufen** sind ANSI-Implementierungen, mit Ausnahme der [IAddrBook](iaddrbookimapiprop.md) -Implementierung. Die **getlasterroraufzurufen** -Methode, die in **IAddrBook** enthalten ist, unterstützt Unicode. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Details der Implementierung der Methode eines Remote Transportanbieters und der von dieser Methode zurückgegebenen Nachrichten sind für den Transportanbieter, da die besonderen Fehlerbedingungen, die zu verschiedenen HRESULT-Werten führen, für unterschiedliche Transportvorgänge unterschiedlich sind. Anbieter.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR** -Struktur, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, verwenden, wenn **getlasterroraufzurufen** eine bereitstellt, nur, wenn der Rückgabewert S_OK ist. Manchmal kann **getlasterroraufzurufen** nicht ermitteln, was der letzte Fehler war oder nicht mehr über den Fehler berichtet. In dieser Situation wird stattdessen ein Zeiger auf NULL in _lppMAPIError_ zurückgegeben. 
  
Zum Freigeben des Speichers für die **MAPIERROR** -Struktur rufen Sie die [Mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf. 
  
Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Erweiterte MAPI-Fehler](mapi-extended-errors.md)

