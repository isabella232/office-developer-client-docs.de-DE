---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439289"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Veraltet. Gibt die Adresstypen zurück, die von allen Transportanbietern in der Sitzung verarbeitet werden können. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Format für die zurückgegebenen Adresstypen angibt. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Adresstypen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Adresstypen im ANSI-Format.
    
 _lpcAdrTypes_
  
> [out] Ein Zeiger auf eine Anzahl von Adresstypen, auf die der _lpppszAdrTypes-Parameter verweist._ 
    
 _lpppszAdrTypes_
  
> [out] Ein Zeiger auf ein Array von Zeigern auf Adresstypen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Adresstypen wurden erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::EnumAdrTypes-Methode** gibt eine Liste der Adresstypen zurück, die von allen aktiven Transportanbietern in der Sitzung verarbeitet werden können. Die Adresstypen für Transportanbieter, die derzeit nicht geladen sind, sind nicht in der Liste enthalten. Transportanbieter registrieren sich, um einen oder mehrere Adresstypen zu behandeln, wenn MAPI ihre [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) aufruft. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen [Sie MAPIFreeBuffer auf,](mapifreebuffer.md) um das Zeichenfolgenarray frei zu lassen, auf das der  _lpppszAdrTypes-Parameter_ verweist. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

