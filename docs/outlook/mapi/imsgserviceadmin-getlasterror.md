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
ms.openlocfilehash: 302aebd0be78c833acf4f82d2bb815ba46ae6f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412142"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum letzten Fehler enthält, der für ein Nachrichtendienstverwaltungsobjekt aufgetreten ist. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein HRESULT-Datentyp, der den Fehlerwert enthält, der durch den vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _Parameter lppMAPIError_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Das MAPI_UNICODE wurde festgelegt, und das Verwaltungsobjekt des Nachrichtendiensts unterstützt Unicode nicht.
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::GetLastError-Methode** ruft Informationen zum letzten Fehler ab, der von einem [IMsgServiceAdmin-Methodenaufruf](imsgserviceadminiunknown.md) zurückgegeben wurde. Clients können ihren Benutzern detaillierte Informationen zum Fehler bereitstellen, indem sie diese Informationen in ein Dialogfeld eingeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur** verwenden, wenn MAPI eine angibt, auf die der  _lppMAPIError-Parameter_ verweist, nur, wenn **GetLastError** eine S_OK. Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden. In dieser Situation gibt **GetLastError** stattdessen einen Zeiger auf NULL in  _lppMAPIError_ zurück. 
  
Weitere Informationen zur **GetLastError-Methode** finden Sie unter [Using Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

