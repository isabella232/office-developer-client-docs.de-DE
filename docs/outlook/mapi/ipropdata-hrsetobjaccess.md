---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d7886d08c21e8fff9aceb3437ecb6bbbd970ed7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591422"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Zugriffsebene f�r das Objekt wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Hinweise

Die **IPropData::HrSetObjAccess** -Methode wird die Zugriffsebene f�r das gesamte Objekt, statt die Daten f�r die einzelnen Eigenschaften. So �ndern Sie die Zugriffsebene festgelegt, wenn das Objekt erstellt wurde, kann **HrSetObjAccess** verwendet werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Zugriffsebene f�r eine Eigenschaft festzulegen, rufen Sie zuerst **HrSetObjAccess** mit dem IPROP_READWRITE-Flag, das im Parameter  _ulAccess_ auf das Objekt ge�ndert werden kann, festgelegt. Rufen Sie dann die [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) -Methode, die die Target-Eigenschaft im Array auf die durch den  _lpPropTagArray_ -Parameter angeben. 
  
Zum Erstellen eines Objekts mit Eigenschaften, die f�r Clients schreibgesch�tzt sein sollen, erstellen Sie ein Lese-Schreib-Objekt, f�gen Sie die erforderlichen Eigenschaften und rufen Sie dann **HrSetObjAccess**, um das Objekt Zugriff auf schreibgesch�tzte ge�ndert werden. 
  
Sie k�nnen auch **HrSetObjAccess** verwenden, um zu verhindern, dass Clients Erstellung neuer Eigenschaften. 
  
## <a name="see-also"></a>Siehe auch



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

