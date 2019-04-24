---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286621"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler der Schaltflächensteuerung enthält. 
  
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
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Dienstanbieter implementieren die **IMAPIControl:: getlasterroraufzurufen** -Methode, um Informationen zu einem fehlgeschlagenen Methodenaufruf bereitzustellen. MAPI kann Benutzern detaillierte Informationen zu dem Fehler geben, indem die Daten aus der **MAPIERROR** -Struktur in einer Nachricht oder einem Dialogfeld angezeigt werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Für jeden Fehler benötigen Sie keine Informationen, die in die **MAPIERROR** -Struktur eingeschlossen werden müssen. Möglicherweise ist es nicht möglich, den vorherigen Fehler zu ermitteln. Wenn Sie Informationen haben, geben Sie S_OK und die entsprechenden Daten in der **MAPIERROR** -Struktur zurück. Wenn keine Informationen verfügbar sind, geben Sie S_OK und einen Zeiger auf NULL für den _lppMAPIError_ -Parameter zurück. 
  
Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

