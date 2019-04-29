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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435579"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Sitzungsfehler enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> in Ein Handle für den im vorherigen Methodenaufruf generierten Fehlerwert.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> Out Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Der Parameter _lppMAPIError_ kann auf NULL festgelegt werden, wenn MAPI keine geeigneten Informationen für eine **MAPIERROR** -Struktur bereitstellen kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Das MAPI_UNICODE-Flag wurde festgelegt, und die Sitzung unterstützt Unicode nicht.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession:: getlasterroraufzurufen** -Methode ruft Informationen zum letzten Fehler ab, der von einem Aufruf der **IMAPISession** -Methode zurückgegeben wurde. Clients können Ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem Sie diese Informationen in ein Dialogfeld einschließen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR** -Struktur verwenden, wenn MAPI eine bereitstellt, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, nur, wenn **getlasterroraufzurufen** S_OK zurückgibt. Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war, oder er hat nichts mehr über den Fehler zu berichten. In dieser Situation gibt **getlasterroraufzurufen** stattdessen einen Zeiger auf NULL in _lppMAPIError_ zurück. 
  
Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[Erweiterte MAPI-Fehler](mapi-extended-errors.md)

