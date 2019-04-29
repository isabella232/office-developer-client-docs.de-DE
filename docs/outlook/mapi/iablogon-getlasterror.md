---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434249"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler des Adressbuch Anbieters enthält. 
  
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
  
> Out Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn der Anbieter keine **MAPIERROR** -Struktur mit den entsprechenden Informationen angeben kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Adressbuchanbieter implementieren die **getlasterroraufzurufen** -Methode, um Informationen zu einem zuvor fehlgeschlagenen Methodenaufruf bereitzustellen. Aufrufer können Ihren Benutzern detaillierte Informationen zum Fehler bereitstellen, indem Sie die Daten aus der **MAPIERROR** -Struktur in ein Dialogfeld einschließen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR** -Struktur, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, verwenden, wenn der Adressbuchanbieter die Struktur bereitstellt und nur dann, wenn **getlasterroraufzurufen** S_OK zurückgibt. Manchmal kann der Adressbuchanbieter nicht ermitteln, was der letzte Fehler aufweist oder nicht mehr über den Fehler berichtet. In dieser Situation gibt der Adressbuchanbieter stattdessen einen Zeiger auf NULL in _lppMAPIError_ zurück. 
  
Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

