---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b726369dff524feb509bcf9b9728184001da2f7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561390"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt dem Objekt eine oder mehrere Eigenschaften vom Typ PT_OBJECT hinzu.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftentags, die die hinzuzufügenden Eigenschaften angeben.
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein gültiger Zeiger auf eine [SPropProblemArray-Struktur](spropproblemarray.md) oder NULL. Bei der Ausgabe ein Zeiger auf einen Zeiger auf eine Struktur, die Informationen zu Eigenschaften enthält, die nicht hinzugefügt werden konnten, oder NULL. Ein Zeiger auf eine Arraystruktur mit Eigenschaftsproblem wird nur zurückgegeben, wenn ein gültiger Zeiger übergeben wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich hinzugefügt.
    
MAPI_E_INVALID_TYPE 
  
> Ein anderer Eigenschaftstyp als PT_OBJECT wurde in dem Array übergeben, auf das der  _Parameter lpPropTagArray_ zeigt. 
    
MAPI_E_NO_ACCESS 
  
> Das Objekt wurde so festgelegt, dass die Lese-/Schreibberechtigung nicht zulässig ist.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Einige, aber nicht alle Eigenschaften wurden hinzugefügt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IPropData::HrAddObjProps-Methode** fügt dem Objekt eine oder mehrere Eigenschaften vom Typ PT_OBJECT hinzu. **HrAddObjProps** stellt eine Alternative zur [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) für Objekteigenschaften bereit, da Objekteigenschaften nicht durch Aufrufen von **SetProps** erstellt werden können. Das Hinzufügen einer Objekteigenschaft führt dazu, dass das Eigenschaftstag in der Liste der Eigenschaftentags enthalten ist, die von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegeben werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added. In der Regel tritt das einzige Problem auf, wenn nicht genügend Arbeitsspeicher vorhanden ist. Geben Sie die **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen, wenn Sie damit fertig sind. 
  
Um eine Eigenschaft hinzuzufügen, muss das Zielobjekt über Lese-/Schreibberechtigungen verfügen. Wenn **HrAddObjProps** MAPI_E_NO_ACCESS zurückgibt, können Sie dem Objekt keine Eigenschaften hinzufügen, da es keine Änderung zulässt. Rufen Sie zum Abrufen der Lese-/Schreibberechtigung für ein Objekt vor dem Aufrufen von **HrAddObjProps** [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) auf, und legen Sie den  _ulAccess-Parameter_ auf IPROP_READWRITE fest. 
  
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

