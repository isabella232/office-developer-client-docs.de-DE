---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 985b763ade9670c064c6c338953debf7beaa2783
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792771"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Betrifft**: Outlook 
  
Fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT auf das Objekt.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftentags, die angeben, die Eigenschaften hinzufügen.
    
 _lppProblems_
  
> [in, out] Klicken Sie auf Eingaben, einen gültigen Zeiger auf eine Struktur [SPropProblemArray](spropproblemarray.md) oder NULL. Klicken Sie auf Ausgabe, einen Zeiger auf einen Zeiger auf eine Struktur, die Informationen zu Eigenschaften enthält, die nicht hinzugefügt werden konnte, oder NULL. Nur, wenn ein gültiger Zeiger übergeben wird, wird ein Zeiger auf eine Eigenschaft Problem Array-Struktur zurückgegeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich hinzugefügt.
    
MAPI_E_INVALID_TYPE 
  
> Geben Sie eine Eigenschaft außer PT_OBJECT im Array übergeben wurde, die auf der _LpPropTagArray_ -Parameter verweist. 
    
MAPI_E_NO_ACCESS 
  
> Das Objekt wurde nicht für Lese-/Schreibberechtigung zulassen festgelegt.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Einige, jedoch nicht alle Eigenschaften wurden hinzugefügt.
    
## <a name="remarks"></a>Bemerkungen

Die **IPropData::HrAddObjProps** -Methode fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT auf das Objekt. **HrAddObjProps** stellt eine Alternative zur die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode für Objekteigenschaften, da Objekteigenschaften durch Aufrufen von **SetProps**nicht erstellt werden können. Hinzufügen einer Object-Eigenschaft führt das Eigenschafts-Tag eingeschlossen werden, in der Liste der Eigenschaftentags, die die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode zurückgibt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **HrAddObjProps** MAPI_W_PARTIAL_COMPLETION zurückgegeben, und Sie _LppProblems_ auf einen gültigen Zeiger festgelegt haben, überprüfen Sie die zurückgegebene [SPropProblemArray](spropproblemarray.md) -Struktur, um zu ermitteln, welche Eigenschaften nicht hinzugefügt wurden. In der Regel ist das einzige Problem, dass nicht genügend Speicherplatz verfügbar. Freigeben der Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, wenn Sie mit ihm fertig sind. 
  
Zum Hinzufügen einer Eigenschaft muss das Zielobjekt Lese-/Schreibberechtigung haben. Wenn **HrAddObjProps** MAPI_E_NO_ACCESS zurückgibt, können nicht Sie Eigenschaften für das Objekt hinzufügen, da diese Änderung nicht zulässig ist. Lese-/Schreibberechtigung für ein Objekt vor dem Aufrufen von **HrAddObjProps**zu erhalten, rufen Sie [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) , und legen Sie den Parameter _UlAccess_ auf IPROP_READWRITE. 
  
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

