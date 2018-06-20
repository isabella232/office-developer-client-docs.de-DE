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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792273"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Betrifft**: Outlook 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein Handle für den im vorherigen Methodenaufruf generierten Fehlercode.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die das Format für den Text in der **MAPIERROR** -Struktur, die auf den _LppMAPIError_zurückgegeben angibt. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen sollte im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgen in ANSI-Format.
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn keine Fehler Informationen zurückgeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Fehlerinformationen wurde zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::GetLastError** -Methode stellt Informationen zu einem Aufruf der vorherigen-Methode, die nicht zur Verfügung. Clients können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen. 
  
Alle Implementierungen der **GetLastError** von MAPI bereitgestellt sind ANSI Implementierungen, mit Ausnahme der [IAddrBook](iaddrbookimapiprop.md) -Implementierung. Die enthaltene **IAddrBook** **GetLastError** -Methode unterstützt Unicode. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Details eines Remote-transport-Implementierung dieser Methode und worauf Nachrichten von die dieser Methode zurückgegebenen bis zu der Adressbuchhierarchie des Anbieters, da die bestimmten fehlerbedingungen, die zu verschiedenen HRESULT-Werte für verschiedene Transport abweichen Anbieter.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR** -Struktur auf durch den Parameter _LppMAPIError_ zeigt, wenn **GetLastError** bereitstellt, nur, wenn S_OK zurückgegeben wird. In einigen Fällen kann **GetLastError** nicht ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde. In diesem Fall wird ein Zeiger auf NULL stattdessen in _LppMAPIError_ zurückgegeben. 
  
Um den Speicher für die Struktur **MAPIERROR** freizugeben, rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[Fehler Extended MAPI](mapi-extended-errors.md)

