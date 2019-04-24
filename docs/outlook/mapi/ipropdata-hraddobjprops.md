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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315533"
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
  
> in Ein Zeiger auf ein Array von Property-Tags, die die hinzuzufügenden Eigenschaften Kennzeichen.
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein gültiger Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur oder NULL. Bei der Ausgabe ein Zeiger auf einen Zeiger auf eine Struktur, die Informationen zu Eigenschaften enthält, die nicht hinzugefügt werden konnten, oder NULL. Ein Zeiger auf eine Eigenschaften Problem-Array Struktur wird nur zurückgegeben, wenn ein gültiger Zeiger übergeben wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich hinzugefügt.
    
MAPI_E_INVALID_TYPE 
  
> Ein anderer Eigenschaftentyp als PT_OBJECT wurde in dem Array übergeben, auf das der _lpPropTagArray_ -Parameter zeigt. 
    
MAPI_E_NO_ACCESS 
  
> Das Objekt wurde so festgelegt, dass die Berechtigung Lese-/Schreibzugriff nicht zulässig ist.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Einige, aber nicht alle Eigenschaften wurden hinzugefügt.
    
## <a name="remarks"></a>Bemerkungen

Die **IPropData:: HrAddObjProps** -Methode fügt dem Objekt eine oder mehrere Eigenschaften vom Typ PT_OBJECT hinzu. **HrAddObjProps** bietet eine Alternative zur [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode für Objekteigenschaften, da Objekteigenschaften nicht durch Aufrufen von **** SetProps erstellt werden können. Wenn Sie eine Objekteigenschaft hinzufügen, wird das Property-Tag in die Liste der Eigenschaftstags aufgenommen, die von der [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode zurückgegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **HRADDOBJPROPS** MAPI_W_PARTIAL_COMPLETION zurückgibt und Sie _lppProblems_ auf einen gültigen Zeiger festgelegt haben, überprüfen Sie die zurückgegebene [SPropProblemArray](spropproblemarray.md) -Struktur, um herauszufinden, welche Eigenschaften nicht hinzugefügt wurden. NormalerWeise ist das einzige Problem, das auftritt, mangelnder Arbeitsspeicher. Geben Sie die **SPropProblemArray** -Struktur frei, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen, wenn Sie damit fertig sind. 
  
Zum Hinzufügen einer Eigenschaft muss das Zielobjekt Lese-/Schreibzugriff besitzen. Wenn **HRADDOBJPROPS** MAPI_E_NO_ACCESS zurückgibt, können Sie dem Objekt keine Eigenschaften hinzufügen, da es keine Änderung zulässt. Wenn Sie vor dem Aufrufen von **HrAddObjProps**Lese-/Schreibzugriff auf ein Objekt erhalten möchten, rufen Sie [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) auf, und legen Sie den Parameter _ulAccess_ auf IPROP_READWRITE fest. 
  
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

