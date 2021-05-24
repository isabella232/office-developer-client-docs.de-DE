---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9fae06b9e9d5ef4885d798825659fa3486ec9e72
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589180"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt fest oder ändert den Wert einer einzelnen Eigenschaft auf einer Eigenschaftenschnittstelle, d. h. einer Schnittstelle, die von [IMAPIProp abgeleitet ist.](imapipropiunknown.md) 
  
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

 _pmp_
  
> [in] Zeiger auf eine [IMAPIProp-Schnittstelle,](imapipropiunknown.md) auf der der Eigenschaftswert festgelegt oder geändert werden soll. 
    
 _pprop_
  
> [in] Zeiger auf die [SPropValue-Struktur,](spropvalue.md) die den wert definiert, der für die  _pmp-Eigenschaft festgelegt werden_ soll. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Im Gegensatz zur [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) gibt die **HrSetOneProp-Funktion** keine Warnungen zurück. Da nur eine Eigenschaft definiert wird, ist sie einfach erfolgreich oder schlägt fehl. Zum Festlegen oder Ändern mehrerer Eigenschaften ist **SetProps** schneller. 
  
Sie können eine einzelne Eigenschaft mit der [HrGetOneProp-Funktion](hrgetoneprop.md) abrufen. 
  

