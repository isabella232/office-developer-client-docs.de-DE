---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 64b0c0501a6ef4471f97e82b231ef430681f1306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573390"
---
# <a name="ipropdatahrgetpropaccess"></a>IPropData::HrGetPropAccess

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft die Zugriffsebene und den Status f�r eine oder mehrere der Eigenschaften des Objekts an.
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a>Parameter

 _lppPropTagArray_
  
> [in, out] Bei Eingabe ein Array von Eigenschaftentags, die angeben, die Eigenschaften f�r die Zugriffsebenen und Status abgerufen. Anderenfalls einen Zeiger auf NULL, die angibt, **HrGetPropAccess** Zugriffsebenen und Statusinformationen f�r alle Eigenschaften abrufen soll. Bei der Ausgabe ein Array von Eigenschaftentags f�r welche Flags Zugriff und Status abgerufen wurden. Die Flags werden in das Array auf die durch den Parameter  _lprgulAccess_ gespeichert. 
    
 _lprgulAccess_
  
> [out] Ein Zeiger auf ein Array von Bitmasken Kennzeichnung. Jede Bitmaske gibt an, auf die Zugriffsebenen, Status oder beides f�r jede Eigenschaft im Array auf die durch den Parameter  _lpPropTagArray_ identifiziert. Die beiden Arrays sind mit fester Breite, dass die erste Bitmaske, dass  _lprgulAccess_ verweist auf die erste Eigenschaft beschreibt zu usw.,  _lpPropTagArray_ verweist. F�r jedes Eigenschaftentags k�nnen die folgenden Kennzeichen festgelegt werden: 
    
|**Zugriffsebene flag**|**Status-flag**|
|:-----|:-----|
|IPROP_READONLY, die angibt, dass die Eigenschaft nicht ge�ndert werden kann.  <br/> |IPROP_CLEAN, die angibt, dass die Eigenschaft nicht ge�ndert wurde.  <br/> |
|IPROP_READWRITE, die angibt, dass die Eigenschaft ge�ndert werden kann.  <br/> |IPROP_DIRTY, die angibt, dass die Eigenschaft ge�ndert wurde.  <br/> |
   
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Access-Ebene und den Status Kennzeichen f�r die Eigenschaften wurden erfolgreich zur�ckgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IPropData::HrGetPropAccess** -Methode ruft eine Reihe von Flags, die die Zugriffsebene und den Status f�r eine oder mehrere Eigenschaften angibt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer:

Sie k�nnen **HrGetPropAccess** f�r folgende Zwecke verwenden: 
  
- Um zu bestimmen, ob ein Client ge�ndert oder schreibbare Eigenschaft gel�scht.
    
- Um einen Client nicht �ndern oder L�schen einer Eigenschaft mithilfe der Methods [IMAPIProp](imapipropiunknown.md) zu verhindern. 
    
Wenn eine der Eigenschaften in die Array-Tag-Eigenschaft auf das  _lppPropTagArray_ gel�scht wurde, wird **HrGetPropAccess** den Arrayeintrag auf Ausgabe 0 festgelegt. Wenn Sie  _lppPropTagArray_ auf NULL festgelegt wurde und eine der Eigenschaften f�r das Objekt gel�scht wurde, wird die Eigenschaft deleted im Array zur�ckgegeben. 
  
Wenn eine Eigenschaft ge�ndert wurde, ist seine IPROP_DIRTY-Flag in den entsprechenden Eintrag im Array, zeigt  _lprgulAccess_ festgelegt. Weder IPROP_READONLY noch IPROP_READWRITE wird festgelegt. 
  
Wenn eine Eigenschaft nicht ge�ndert oder gel�scht wurde, wird nur das Flag IPROP_READONLY oder IPROP_READWRITE festgelegt werden. 
  
## <a name="see-also"></a>Siehe auch



[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

