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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2be5e40de6894b99d9de86423e99dd95a08bc04c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792066"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**Betrifft**: Outlook 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu dem Fehler der vorherigen Schaltfläche-Steuerelement enthält. 
  
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
  
> [in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolgen steuert zurückgegeben. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn der Anbieter eine **MAPIERROR** -Struktur mit den entsprechenden Informationen angegeben werden kann. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Dienstanbieter implementieren die **IMAPIControl::GetLastError** -Methode, um Informationen zu einem vorherigen Methodenaufruf angeben, die nicht erfolgreich. MAPI erhalten Benutzer detaillierte Informationen zu dem Fehler durch die Daten aus der **MAPIERROR** -Struktur in einer Nachricht oder Dialogfeld anzeigen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie müssen nicht die Informationen in der Struktur **MAPIERROR** für alle Fehler eingeschlossen haben. Es möglicherweise nicht möglich, zu bestimmen, welche vorherigen Fehler. Wenn Sie Informationen, kehren Sie S_OK und die entsprechenden Daten in der Struktur **MAPIERROR** . Wenn keine Informationen verfügbar sind, werden S_OK und einen Zeiger auf NULL für den Parameter _LppMAPIError_ zurück. 
  
Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

