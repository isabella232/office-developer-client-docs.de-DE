---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 59b534a076aee6498be9146eabb69c62fca313ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792304"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**Betrifft**: Outlook 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Sitzungsfehler enthält. 
  
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
  
> [out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn MAPI entsprechenden Informationen für eine **MAPIERROR** Struktur angegeben werden kann. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Die Option MAPI_UNICODE wurde festgelegt, und die Sitzung Unicode nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::GetLastError** -Methode ruft Informationen über den letzten Fehler, der durch einen Aufruf der Methode **IMAPISession** zurückgegeben wurde. Clients können die Benutzer mit ausführlichen Informationen zu dem Fehler bereitstellen, indem Sie diese Informationen in einem Dialogfeld einschließlich. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Struktur **MAPIERROR** können MAPI, bereitstellt, auf die die _LppMAPIError_ Parameter nur, wenn **GetLastError** S_OK zurückgegeben. In einigen Fällen kann nicht MAPI was letzten Fehler erkennen, oder es wurde keine weiteren zu dem Fehler melden. In diesem Fall gibt **GetLastError** einen Zeiger auf NULL in _LppMAPIError_ stattdessen. 
  
Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Fehler Extended MAPI](mapi-extended-errors.md)

