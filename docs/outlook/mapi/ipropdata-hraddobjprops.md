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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416384"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT objekt hinzu.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftstags, die die hinzuzufügenden Eigenschaften angeben.
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein gültiger Zeiger auf eine [SPropProblemArray-Struktur](spropproblemarray.md) oder NULL. Bei der Ausgabe ein Zeiger auf einen Zeiger auf eine Struktur, die Informationen zu Eigenschaften enthält, die nicht hinzugefügt werden konnten, oder NULL. Ein Zeiger auf eine Arraystruktur mit Eigenschaftenproblem wird nur zurückgegeben, wenn ein gültiger Zeiger übergeben wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich hinzugefügt.
    
MAPI_E_INVALID_TYPE 
  
> Ein anderer Eigenschaftstyp als PT_OBJECT in dem Array übergeben, auf das der  _lpPropTagArray-Parameter_ verweist. 
    
MAPI_E_NO_ACCESS 
  
> Das Objekt wurde so festgelegt, dass keine Lese-/Schreibberechtigung zulässig ist.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Einige, aber nicht alle Eigenschaften wurden hinzugefügt.
    
## <a name="remarks"></a>Hinweise

Die **IPropData::HrAddObjProps-Methode** fügt dem Objekt eine oder mehrere Eigenschaften vom Typ PT_OBJECT hinzu. **HrAddObjProps** stellt eine Alternative zur [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) für Objekteigenschaften dar, da Objekteigenschaften nicht durch Aufrufen von **SetProps erstellt werden können.** Das Hinzufügen einer Objekteigenschaft führt dazu, dass das Eigenschaftstag in die Liste der Eigenschaftstags aufgenommen wird, die von der [IMAPIProp::GetPropList-Methode zurückgegeben](imapiprop-getproplist.md) werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **HrAddObjProps** MAPI_W_PARTIAL_COMPLETION zurückgibt und Sie  _lppProblems_ auf einen gültigen Zeiger festgelegt haben, überprüfen Sie die zurückgegebene [SPropProblemArray-Struktur,](spropproblemarray.md) um herauszufinden, welche Eigenschaften nicht hinzugefügt wurden. In der Regel tritt das einzige Problem auf, das auftritt, ist fehlender Arbeitsspeicher. Geben Sie **die SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen, wenn Sie damit fertig sind. 
  
Zum Hinzufügen einer Eigenschaft muss das Zielobjekt über Lese-/Schreibberechtigungen verfügen. Wenn **HrAddObjProps** MAPI_E_NO_ACCESS zurückgibt, können Sie dem Objekt keine Eigenschaften hinzufügen, da es keine Änderung zulässt. Rufen Sie [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) auf, um lese-/schreibberechtigungen für ein Objekt zu erhalten, bevor **Sie HrAddObjProps** aufrufen, und legen Sie den _ulAccess-Parameter_ auf IPROP_READWRITE. 
  
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

