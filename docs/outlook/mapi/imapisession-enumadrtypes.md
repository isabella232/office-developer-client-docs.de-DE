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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6bd13eb7180302a5ab770586cf36856ca5a22676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792302"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Betrifft**: Outlook 
  
Veraltet. Gibt die behandelt werden können Adresstypen aller Anbieter für den Transport in der Sitzung zurück. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die das Format für die zurückgegebene Adresstypen angibt. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Adresstypen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Adresstypen im ANSI-Format.
    
 _lpcAdrTypes_
  
> [out] Ein Zeiger auf eine Anzahl von-Adresstypen auf den durch den Parameter _LpppszAdrTypes_ verwiesen. 
    
 _lpppszAdrTypes_
  
> [out] Ein Zeiger auf ein Array von Zeigern für Adresstypen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Adresstypen wurden erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::EnumAdrTypes** -Methode gibt eine Liste der durch alle aktiven Transportanbieter behandelt werden kann Adresstypen in der Sitzung zurück. Die Adresstypen für Transportanbieter, die derzeit nicht geladen werden, sind nicht in der Liste enthalten. Transportanbieter registrieren, um eine oder mehrere Adresstypen behandeln, wenn MAPI ihre [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufruft. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) , um auf das durch den Parameter _LpppszAdrTypes_ Zeichenfolgenarrays freizugeben. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

