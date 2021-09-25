---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 13e90fdd80c6a41963dd0f3081739038b190abe5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596022"
---
# <a name="ipropdatahrsetpropaccess"></a>IPropData::HrSetPropAccess

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Zugriffsebene oder Status f�r eine oder mehrere der Eigenschaften des Objekts fest.
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftentags, die angeben, die Eigenschaften ge�ndert werden soll. 
    
 _rgulAccess_
  
> [in] Ein Array von Bitmasken Kennzeichnung. Jede Bitmaske gibt an, auf die Zugriffsebenen, Status oder beides f�r jede Eigenschaft im Array, dem der  _lpPropTagArray_ -Parameter verweist identifiziert. Die beiden Arrays sind mit fester Breite, dass die erste Bitmaske in  _rgulAccess_ die ersten-Eigenschaft, zeigt  _lpPropTagArray_ zu, und so weiter beschreibt. F�r jedes Eigenschaftentags kann ein Zugriffsebene Flag und ein Status-Flag festgelegt werden. Die folgende Tabelle zeigt die m�glichen Flags. 
    
|**Zugriffsebene flag**|**Status-flag**|
|:-----|:-----|
|IPROP_READONLY, die angibt, dass die Eigenschaft nicht ge�ndert werden kann  <br/> |IPROP_CLEAN, die angibt, dass die Eigenschaft nicht ge�ndert wurde.  <br/> |
|IPROP_READWRITE, die angibt, dass die Eigenschaft ge�ndert werden kann.  <br/> |IPROP_DIRTY, die angibt, dass die Eigenschaft ge�ndert wurde.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zugriffsebene und den Status Kennzeichen wurden erfolgreich festgelegt.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, eine Eigenschaft f�r ein schreibgesch�tztes Objekt oder ein Objekt f�r den Anrufer nicht �ber ausreichende Berechtigungen verf�gt festlegen.
    
MAPI_E_INVALID_PARAMETER 
  
> Der Parameter  _rgulAccess_ enth�lt eine ung�ltige Kombination von Flags, die wie IPROP_READONLY und IPROP_READWRITE. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IPropData::HrSetPropAccess** -Methode �ndert die Zugriffsebene und den Status f�r die Eigenschaften, die durch die Eigenschaftstags in der [SPropTagArray](sproptagarray.md) -Struktur, die auf die durch den Parameter  _lpPropTagArray_ identifiziert werden. F�r jede Eigenschaft ist vorhanden ein entsprechender Eintrag im  _rgulAccess_ -Array. Der Eintrag kann festgelegt werden, um ein Flag, das die Eigenschaft Zugriffsebene und ein weiteres angibt Flag, das den Status angibt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie **HrSetPropAccess**, um bei �nderung eines bestimmten-Eigenschaft ermitteln und die Zugriffsebene f�r eine oder mehrere der Eigenschaften eines Objekts zu �ndern. 
  
## <a name="see-also"></a>Siehe auch



[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

