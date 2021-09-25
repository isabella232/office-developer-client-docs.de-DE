---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 590f965d1e2e1155f3171f0888efda7613d4830e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592459"
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
  
> [in] Eine Bitmaske mit Flags, die das Format für die zurückgegebenen Adresstypen angibt. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Adresstypen haben das Unicode-Format. Wenn das MAPI_UNICODE Flag nicht festgelegt ist, haben die Adresstypen das ANSI-Format.
    
 _lpcAdrTypes_
  
> [out] Ein Zeiger auf eine Anzahl von Adresstypen, auf die der  _parameter lpppszAdrTypes_ verweist. 
    
 _lpppszAdrTypes_
  
> [out] Ein Zeiger auf ein Array von Zeigern für Adresstypen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Adresstypen wurden erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::EnumAdrTypes-Methode** gibt eine Liste der Adresstypen zurück, die von allen aktiven Transportanbietern in der Sitzung verarbeitet werden können. Die Adresstypen für Transportanbieter, die derzeit nicht geladen sind, sind nicht in der Liste enthalten. Transportanbieter registrieren sich, um einen oder mehrere Adresstypen zu verarbeiten, wenn MAPI ihre [IXPLogon::AddressTypes-Methode aufruft.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) auf, um das Zeichenfolgenarray freizugeben, auf das der  _Parameter lpppszAdrTypes_ verweist. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

