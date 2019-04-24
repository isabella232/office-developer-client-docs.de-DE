---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279643"
---
# <a name="iprovideradmingetlasterror"></a>IProviderAdmin::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der für das Anbieter Verwaltungsobjekt aufgetreten ist. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> in Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** , die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** zurückgegeben werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **getlasterroraufzurufen** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **getlasterroraufzurufen** unterstützt nur Unicode. 
    
## <a name="remarks"></a>Bemerkungen

Die **IProviderAdmin:: getlasterroraufzurufen** -Methode liefert Informationen zu einem vorherigen Methodenaufruf, der fehlgeschlagen ist. Aufrufer können Ihren Benutzern detaillierte Informationen zum Fehler bereitstellen, indem Sie die Daten aus der **MAPIERROR** -Struktur in ein Dialogfeld einschließen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR** -Struktur verwenden, wenn MAPI eine bereitstellt, auf die der _lppMAPIError_ -Parameter nur verweist, wenn **getlasterroraufzurufen** S_OK zurückgibt. Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder nicht mehr über den Fehler berichtet hat. In dieser Situation wird stattdessen ein Zeiger auf NULL in _lppMAPIError_ zurückgegeben. 
  
Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [using Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

