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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338437"
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
  
> in Eine Bitmaske von Flags, die das Format für die zurückgegebenen Adresstypen angibt. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Adresstypen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Adresstypen im ANSI-Format.
    
 _lpcAdrTypes_
  
> Out Ein Zeiger auf die Anzahl von Adresstypen, auf die durch den _lpppszAdrTypes_ -Parameter verwiesen wird. 
    
 _lpppszAdrTypes_
  
> Out Ein Zeiger auf ein Array von Zeigern auf Adresstypen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Adresstypen wurden erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession:: EnumAdrTypes** -Methode gibt eine Liste der Adresstypen zurück, die von allen aktiven Transportanbietern in der Sitzung verarbeitet werden können. Die Adresstypen für Transportanbieter, die derzeit nicht geladen werden, sind nicht in der Liste enthalten. Transport Anbieter registrieren, um einen oder mehrere Adresstypen zu behandeln, wenn MAPI Ihre [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode aufruft. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie [mapifreebufferfreigegeben](mapifreebuffer.md) auf, um das Zeichenfolgenarray zu veröffentlichen, auf das durch den _lpppszAdrTypes_ -Parameter verwiesen wird. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

