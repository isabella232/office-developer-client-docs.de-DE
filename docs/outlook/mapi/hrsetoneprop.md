---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 50335f864001cd5698e93b1f2df50b9a6e2512c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561586"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt fest oder ändert den Wert einer einzelnen Eigenschaft auf einer Eigenschaftsschnittstelle, d. h. eine Schnittstelle, die von [IMAPIProp](imapipropiunknown.md)abgeleitet ist. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parameter

 _Pmp_
  
> [in] Zeiger auf eine [IMAPIProp-Schnittstelle,](imapipropiunknown.md) für die der Eigenschaftswert festgelegt oder geändert werden soll. 
    
 _pprop_
  
> [in] Zeiger auf die [SPropValue-Struktur,](spropvalue.md) die den für die  _pmp-Eigenschaft_ festzulegenden Wert definiert. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Im Gegensatz zur [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) gibt die **HrSetOneProp-Funktion** niemals Warnungen zurück. Da nur eine Eigenschaft festgelegt wird, ist sie entweder erfolgreich oder schlägt fehl. Zum Festlegen oder Ändern mehrerer Eigenschaften ist **SetProps** schneller. 
  
Sie können eine einzelne Eigenschaft mit der [HrGetOneProp-Funktion](hrgetoneprop.md) abrufen. 
  

