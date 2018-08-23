---
title: IMsgServiceAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetLastError
api_type:
- COM
ms.assetid: 9e3c8d6e-74be-46a7-94ed-74a969caf165
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3c2db9284c0e014101bc3a3d2114a187d7cb3b4b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576627"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den letzten Fehler enthält, die für ein Objekt "Message" Service Administration aufgetreten sind. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein HRESULT-Datentyp, der den Fehlerwert durch den vorherigen Methodenaufruf von generiert enthält.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Die Option MAPI_UNICODE wurde festgelegt, und das Objekt "Message" Service Administration Unicode nicht unterstützt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::GetLastError** -Methode ruft Informationen über den letzten Fehler, der durch einen Aufruf der Methode [IMsgServiceAdmin](imsgserviceadminiunknown.md) zurückgegeben wurde. Clients können die Benutzer mit ausführlichen Informationen zu dem Fehler bereitstellen, indem Sie diese Informationen in einem Dialogfeld einschließlich. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können nutzen Sie die **MAPIERROR** Struktur, wenn MAPI bereitstellt, auf das durch den Parameter _LppMAPIError_ nur, wenn **GetLastError** gibt S_OK zurück. In einigen Fällen kann MAPI nicht ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde. In diesem Fall gibt **GetLastError** einen Zeiger auf NULL in _LppMAPIError_ stattdessen. 
  
Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Erweiterte Fehler verwenden](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

