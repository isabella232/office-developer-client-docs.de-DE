---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 12e25a49cdb25e253ee0e7033214970c36b11732
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579747"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Zugriffsebene f�r das Objekt fest.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Parameter

 _ulAccess_
  
> [in] Eine Bitmaske aus Flags, die Zugriffsebene des Objekts angibt. Eine der folgenden Werte kann festgelegt werden:
    
IPROP_READONLY 
  
> Das Objekt Zugriffsebene festgelegt auf schreibgesch�tzt. 
    
IPROP_READWRITE 
  
> Legt die Zugriffsebene f�r das Objekt den Lese-/Schreibzugriff.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Zugriffsebene f�r das Objekt wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IPropData::HrSetObjAccess** -Methode wird die Zugriffsebene f�r das gesamte Objekt, statt die Daten f�r die einzelnen Eigenschaften. So �ndern Sie die Zugriffsebene festgelegt, wenn das Objekt erstellt wurde, kann **HrSetObjAccess** verwendet werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Zugriffsebene f�r eine Eigenschaft festzulegen, rufen Sie zuerst **HrSetObjAccess** mit dem IPROP_READWRITE-Flag, das im Parameter  _ulAccess_ auf das Objekt ge�ndert werden kann, festgelegt. Rufen Sie dann die [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) -Methode, die die Target-Eigenschaft im Array auf die durch den  _lpPropTagArray_ -Parameter angeben. 
  
Zum Erstellen eines Objekts mit Eigenschaften, die f�r Clients schreibgesch�tzt sein sollen, erstellen Sie ein Lese-Schreib-Objekt, f�gen Sie die erforderlichen Eigenschaften und rufen Sie dann **HrSetObjAccess**, um das Objekt Zugriff auf schreibgesch�tzte ge�ndert werden. 
  
Sie k�nnen auch **HrSetObjAccess** verwenden, um zu verhindern, dass Clients Erstellung neuer Eigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

